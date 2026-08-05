# Verifying the Seed Packet

This packet ships with `CHECKSUMS.sha256` — a SHA-256 integrity manifest of every file. Verify before trusting the contents.

Run in Tails (or any clean environment) from the packet root:

```bash
shasum -a 256 -c CHECKSUMS.sha256
```

Every listed file must return `OK`. Any mismatch or warning means a file was altered in transit — **do not use a corrupted or tampered packet**. Re-download from a separate source over a different network and re-verify.

## What's covered

The manifest covers **file content only**. Filesystem metadata — timestamps, extended attributes, macOS `.DS_Store`, Windows `Zone.Identifier` streams — is expected to vary across machines and does not affect checksum verification.

If you are re-distributing, strip such metadata in a clean Linux environment (e.g. inside Tails) before publishing, to avoid leaking source-machine fingerprints:

```bash
find . -type f -exec setfattr -x 'user.*' {} + 2>/dev/null
find . -name '*:Zone.Identifier' -delete
find . -exec touch -d '2000-01-01' {} +
shasum -a 256 -c CHECKSUMS.sha256   # confirm content still OK
```

## Regenerating the manifest

If you intentionally modify a file (e.g. translating), rebuild the manifest so downstream verifiers can validate your version:

```bash
grep -oE './\S+' CHECKSUMS.sha256 | sort -u | xargs shasum -a 256 > CHECKSUMS.sha256.new
mv CHECKSUMS.sha256.new CHECKSUMS.sha256
```

Add new files (e.g. a new translation) to the list before regenerating.
