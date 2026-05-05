# IPClaim

**Public authorship proof for useful work.**

IPClaim makes authorship evidence cheap, immediate, public, and verifiable. It gives work a clear record from day one, excludes work already owned, claimed, or disclosed by others by default, reduces avoidable ownership disputes, and leaves more time, money, and trust for implementation.

The point is not to turn every idea into a fight. The point is to make proof ordinary enough that useful solutions, methods, parts, systems, and technologies can be shown, trusted, adopted, and improved with less friction.

IPClaim is also a specimen of itself: the claim, terms, verification method, and timestamped evidence are present in this repository.

## What It Does

IPClaim attaches four things to a body of work:

- an APC license
- a verification document
- a GitHub Actions timestamp workflow
- cryptographic proof files tied to repository contents

The normal proof target is the Git tree hash, which identifies the exact file contents of a repository state without relying on author dates, commit messages, or GitHub metadata.

## Quick Start

Use IPClaim on an existing Git repository:

```bash
./stamp.sh <target-repo-path> [author-name] [apc|apc-vf]
```

Example:

```bash
./stamp.sh ~/projects/myrepo "Jane Doe" apc
```

For the full integration path, see [QUICKSTART.md](QUICKSTART.md).

## Default Exclusion Of Already-Owned Or Disclosed Work

The claim does not extend to intellectual property that was already owned, already claimed, or already publicly disclosed by another party.

The author is not required to identify in advance every protectable part of the work or to fully investigate every possible existing claim before publication. Some information may be unavailable, unclear, hard to access, or unreasonably costly to obtain.

The claim therefore applies by default only to the author's original contribution, to the extent that it is not already owned, claimed, or publicly disclosed by another party.

If already existing ownership, claim, or public disclosure is later found, those parts are excluded from the claim by default.

## License Model

The canonical default is the APC license in [LICENSE](LICENSE).

APC-VF, the ValueFlow variant, is intentionally separated under [licenses/LICENSE-APC-VF.md](licenses/LICENSE-APC-VF.md). It is preserved for explicit evaluation only and should not be treated as the default IPClaim integration path.

For the decision rule and integration notes, see [LICENSE_CHOICES.md](LICENSE_CHOICES.md).

## Verification

Anyone can verify an IPClaim proof by recomputing the Git tree hash and checking the matching RFC 3161 timestamp token in `.timestamps/`.

See [VERIFY.md](VERIFY.md) for the exact OpenSSL commands and verification model.

## Core Claim

> **Universal, Evidence-Based IP Claim**
>
> I claim, as my intellectual property, whatever can be claimed and is not already owned, claimed, or publicly disclosed by another. I do not need to specify in advance which parts of my work qualify as IP, nor under which category they fall. The act of publication, tied to timestamped and independently verifiable evidence, is sufficient to establish my claim over the original work disclosed here.

## Repository Map

- [stamp.sh](stamp.sh) - helper script for adding APC/IPClaim materials to another Git repository
- [LICENSE](LICENSE) - canonical APC license
- [VERIFY.md](VERIFY.md) - independent verification instructions
- [QUICKSTART.md](QUICKSTART.md) - developer integration guide
- [LICENSE_CHOICES.md](LICENSE_CHOICES.md) - APC vs APC-VF decision notes
- [.github/workflows/timestamp.yml](.github/workflows/timestamp.yml) - timestamp automation
- [.timestamps/](.timestamps/) - committed timestamp proof files

## Support

If this project is useful to you, you can support ongoing independent development:

[![Ko-fi](https://img.shields.io/badge/Ko--fi-Support%20this%20work-ff5e5b?logo=ko-fi&logoColor=white)](https://ko-fi.com/earthcraft)
