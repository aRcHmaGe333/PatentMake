# IPClaim

**IPClaim is a meta-proof. Your work is its own witness.**

This repository proves the system by instantiating it: the claim, the terms, the verification method, and the timestamped evidence are all present here as part of the work itself.

IPClaim is for anyone who wants to publish a public, timestamped, independently verifiable claim to the original intellectual property contained in their work.

## Quick Start / Step-by-Step Usage

Use IPClaim on an existing Git repository to attach:

- an APC license
- a verification document
- a GitHub Actions timestamp workflow
- cryptographic proof files tied to the repository contents

### Requirements

- A Git repository
- At least one commit already made
- A GitHub remote configured if you want automatic timestamping on push

### Command

```bash
./stamp.sh <target-repo-path> [author-name] [apc|apc-vf]
```

Example:

```bash
./stamp.sh ~/projects/myrepo "Jane Doe" apc
```

### License Options

- `apc` — All rights reserved (`LICENSE-APC.md`)
- `apc-vf` — All rights reserved + ValueFlow profit sharing (`LICENSE-APC-VF.md`)

### What the script does

1. Verifies the target repository exists and already has at least one commit.
2. Computes the current Git tree hash for the repository contents.
3. Copies in the selected APC license.
4. Adds `VERIFY.md`.
5. Adds `.github/workflows/timestamp.yml`.
6. Replaces placeholders in the license with author and hash information.
7. Commits the result.
8. Optionally pushes so GitHub Actions can generate timestamp proof files.

### Result

After running the script and pushing, your repository becomes a public, timestamped claim record for the work it contains.

### Verification

Anyone can verify the claim by following the instructions in `VERIFY.md`.

## Default Exclusion of Prior IP

This claim does not extend to intellectual property that was already owned, already claimed, or already publicly disclosed by another party.

The author is not required to identify in advance every protectable part of the work or to fully investigate all possible prior claims before publication.

Such information may be unavailable, unclear, difficult to access, or unreasonably costly to obtain.

The claim therefore applies by default only to the author's original contribution, to the extent that it was not previously owned, claimed, or publicly disclosed by another party.

If prior ownership or prior disclosure is later found, those parts are excluded from the claim by default.

---

**Intellectual Property Claim for an Era of Progress**

IPClaim is a repo toolkit and proof model for publishing authorship claims as public, timestamped, independently verifiable records. IPClaim provides both the proof system and the specimen: it shows how a work can stand as its own evidence.

## The statement:

> **Universal, Evidence-Based IP Claim**
>
> I claim, as my intellectual property, whatever can be claimed and has not been previously claimed as IP by another. I do not need to specify in advance which parts of my work qualify as IP, nor under which category they fall. The act of publication, tied to timestamped and independently verifiable evidence, is sufficient to establish my claim over the original work disclosed here.

## IPClaim: Meta-Proof - Your work is its own witness

IPClaim replaces traditional paperwork and gatekeeping with cryptographic certainty.  
Your work is its own ID, stands as its own testament — timestamped, verifiable, and enduring.

- Proof embedded in your code, blueprint, disclosure
- Authorship verifiable by anyone, anywhere
- Ownership based on evidence

One system is based on evidence. The other is based on permission.

---

## You Claim What You Made
## Show it to the World
