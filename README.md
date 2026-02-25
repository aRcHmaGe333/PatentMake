# PatentMake

**Public authorship infrastructure for the post-patent era.**

You made something. You need the world to know you made it, when you made it, and that nobody made it before you.

The answer: publish it, hash it, timestamp it, done.

PatentMake contains the licensing templates and the GitHub Actions workflow that turn any repository into a continuously self-proving record of authorship. Every push is automatically hashed, timestamped via RFC 3161, and committed back to the repo. The proof lives in the math, not in a service.

## Contents

- `STAMPED-whitepaper.md` — the full case for why this works and why the patent system doesn't
- `LICENSE-APC.md` — all-rights-reserved template with authorship and patent claim
- `LICENSE-APC-VF.md` — same, with ValueFlow revenue-sharing terms added
- `VERIFY.md` — instructions for independent verification with free tools
- `.github/workflows/timestamp.yml` — drop this into any repo for automatic timestamping on every push

## The short version

One system is based on evidence. The other is based on permission.
