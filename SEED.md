# How to Plant the Seed

A practical distribution guide for releasing The Open Framework into the wild.

The medium should match the message. This framework advocates decentralization, censorship resistance, and ownerlessness. It should be released through channels that embody those properties.

---

## Principles

1. **Simultaneity over sequence.** Drop across all channels within the same hour. By the time anyone asks "where did this come from," it is already everywhere.
2. **Permanence over virality.** Pin to storage that cannot be taken down before chasing engagement.
3. **Anonymity over attribution.** The ideas stand without a personality attached. No founder. No face.
4. **Multiplicity over monoculture.** Multiple languages, multiple platforms, multiple formats. No single point of failure.
5. **Obsolescence of distributors.** You are not a permanent maintainer. You plant. You walk away. Others tend what grows.

---

## Phase 1 — Make it permanent

Before anything is posted anywhere, the document must exist in forms that cannot be censored or removed.

### IPFS (InterPlanetary File System)

Pin the full repository (framework, translations, license) to IPFS.

```bash
# Install IPFS if not already installed
# https://docs.ipfs.tech/install/

ipfs add -r /path/to/Open-Framework-Seed
# Note the resulting CID (content identifier)

# Pin to multiple services for redundancy
# Free pinning services:
#   - Pinata (pinata.cloud)
#   - web3.storage
#   - nft.storage
#   - Filebase
```

The CID is the permanent address. Use it in every post.

### Arweave

Pay once. Stored forever. A few cents of AR tokens ensures the document persists for at least 200 years per the Arweave protocol.

```bash
# Install ardrive-cli or use web interface at ardrive.io
# https://docs.arweave.org/

# Upload via ArDrive
ardrive upload-file --local-path FRAMEWORK.md --parent-folder-id <folder>
```

Record the Arweave transaction ID. This is the permanent backup.

### Bitcoin Inscription

For maximum permanence and symbolic resonance — inscribe the document or its IPFS hash directly onto the Bitcoin blockchain via the Ordinals protocol.

- Use a service like ord.io, Unisat, or Ordinals Wallet
- A text inscription of the IPFS hash costs a few dollars in fees
- Once inscribed, the reference is part of the Bitcoin ledger forever

This creates a cryptographic timestamp that the framework existed at a specific moment — using the very infrastructure it advocates for.

### Filecoin, Radicle, Codeberg (optional redundancy)

Mirror the repository across alternative decentralized code-hosting networks. More copies = more resilience.

---

## Phase 2 — Make it forkable

### Anonymous GitHub repository

- Create a new GitHub account via Tor browser
- Use a throwaway ProtonMail or Tutanota email created over Tor
- No personal information. No reused handles.
- Initialize the repository with all files from `Open-Framework-Seed/`
- Set license to CC0 (already in repo)
- Enable Issues and Discussions for community engagement
- Do not configure branch protection — the fork is the primary contribution model

### GitLab mirror

- Duplicate the repository on GitLab (separate anonymous account)
- If GitHub ever censors the repo, GitLab persists
- Include prominent references to IPFS and Arweave in both READMEs

### Operational security checklist

- [ ] Tor Browser for all account creation
- [ ] Dedicated email address, never reused
- [ ] VPN + Tor for all commits (consider Tails OS for maximum isolation)
- [ ] Strip all metadata from uploaded files (use `exiftool` or similar)
- [ ] Do not use any commit message patterns or writing style from your normal work
- [ ] Do not log in to these accounts from your normal IP, ever
- [ ] Do not associate the distribution with any existing identity

---

## Phase 3 — Seed the channels

Within the same hour, post to the following channels. The simultaneity is critical.

### Reddit

See `posts/reddit.md` for the post template and target subreddits.

- Stagger posts across subreddits over a few hours to avoid anti-spam triggers
- Use a Reddit account with minimal karma, created over Tor
- Do not reply to comments from the same IP used to post

**Target subreddits:**
r/decentralization, r/dao, r/solarpunk, r/collapse, r/bitcoin, r/ethereum, r/cryptocurrency, r/futurology, r/anarchism, r/cryptogovernance, r/globalpolitics, r/basicincome, r/georgism

### Hacker News

See `posts/hn.md`. Post with a dry, factual title. HN rewards substance and penalizes marketing language.

### Twitter / X

See `posts/twitter.md` for the 15-tweet thread. Post via anonymous account created through Tor. Post the thread all at once (don't stagger within the thread) but spaced a few minutes apart from the main drop.

### Nostr

See `posts/nostr.md`. Publish as a NIP-23 long-form note. Connect to multiple relays for propagation.

**Recommended relays:**
- wss://relay.damus.io
- wss://nos.lol
- wss://relay.nostr.band
- wss://nostr.wine
- wss://relay.snort.social
- wss://purplepag.es

### DAO forums and Discord/Matrix servers

- Gitcoin Grants forums
- Aragon Forum
- Snapshot community board
- DAOhaus Discord
- Bankless DAO
- MetaGov (metagov.org)
- Radicle community
- Optimism Collective forums
- Relevant Matrix rooms (matrix.to)

Post a short, respectful introduction. Link to the document. Do not spam.

### Lemmy, Mastodon, Bluesky

Federated social networks with aligned communities:
- Lemmy: lemmy.ml, beehaw.org, lemmy.world — post in communities for decentralization, bitcoin, futurology
- Mastodon: mstdn.social, fosstodon.org, mas.to — use hashtags #decentralization #bitcoin #governance #CC0
- Bluesky: Same thread format as Twitter

---

## Phase 4 — Make it translate itself

The seed packet ships with initial translations: Spanish, Chinese, Arabic, French, Portuguese.

The goal is not to maintain these translations — it is to inspire others to produce more. Every language is a new ecosystem.

### Requested translations (invite via README)

Priority languages by speaker population and strategic reach:

- Hindi / Urdu
- Bengali
- Russian
- Japanese
- German
- Turkish
- Vietnamese
- Swahili
- Indonesian / Malay
- Persian / Farsi
- Korean
- Thai
- Tagalog
- Amharic
- Yoruba
- Hausa

A translation is among the highest-value contributions a single person can make.

---

## Phase 5 — Walk away

This is the hardest part.

Once the seed is planted, the distributor's job is finished. Do not:

- Appoint yourself as "community manager"
- Launch a token inspired by the framework
- Start a Discord server you control
- Create a personal brand around the ideas
- Accept speaking invitations to "represent" the framework
- Write follow-up manifestos signed with your name

Do:

- Read forks and note improvements you want to propagate back
- Respond to good-faith critique without defensiveness
- Amplify other anonymous voices building on the ideas
- Translate follow-up documents if you have the skills
- Move on to the next thing

The framework belongs to humanity. It does not belong to you.

---

## Long-term health signals

The seed is taking root if:

- Forks appear with substantive improvements
- Translations appear in languages you didn't provide
- Working groups self-organize around focus areas
- Developers begin building the infrastructure (smart contracts, interfaces, tools)
- Critique becomes more specific and technical
- The document begins being referenced in contexts you have no connection to
- Multiple versions diverge and cross-pollinate
- The "original" repository becomes irrelevant as better-maintained forks emerge

The seed has died if:

- It becomes associated with a single personality or brand
- Someone launches a token or sells access to "the official framework"
- A foundation forms claiming authority over the canonical version
- The ideas are domesticated into a startup pitch
- Enthusiasm outpaces building

---

## A final note

No one is coming to save us.

If you are reading this, you have the coordinates. You have the tools. You have the permission.

The only question is whether you act.

One humanity. One tribe. One planet.
