# IPClaim — Developer Quickstart

This page is the minimal, practical path for a developer who wants to add IPClaim-style timestamped authorship proofs to their own repository.

If you only want the short version:

1. Use the canonical APC `LICENSE` and copy it to your repo as `LICENSE`.
2. Copy `VERIFY.md` into your repo root.
3. (Optional) Add the timestamping workflow from `VERIFY.md` into `.github/workflows/timestamp.yml`.
4. Commit and push. The workflow will create `.timestamps/<TREE_HASH>.tsr` or you can follow the manual steps in `VERIFY.md`.

Notes on choosing a license
- `LICENSE` (APC — canonical): "All Rights Reserved — Authorship & Patent Claim". Use this when you want to publish a timestamped, cryptographically verifiable claim and retain full rights. This is the recommended default.

If you are unsure, pick the canonical `LICENSE` for maximum clarity and change later deliberately.

Step-by-step (POSIX)

```sh
# From your project root (example assumes IPClaim repo is a sibling directory)
cp ../IPClaim/LICENSE ./LICENSE
cp ../IPClaim/VERIFY.md ./VERIFY.md
mkdir -p .github/workflows
# Copy the timestamp workflow snippet from IPClaim's VERIFY.md into .github/workflows/timestamp.yml
git add LICENSE VERIFY.md .github/workflows/timestamp.yml
git commit -m "Add APC license and timestamp workflow"
git push
```

Step-by-step (Windows PowerShell)

```powershell
# From your project root (example assumes IPClaim repo is a sibling directory)
Copy-Item ..\IPClaim\LICENSE -Destination .\LICENSE
Copy-Item ..\IPClaim\VERIFY.md -Destination .\VERIFY.md
New-Item -ItemType Directory -Path .github\workflows -Force
# Create .github\workflows\timestamp.yml by copying the YAML snippet from VERIFY.md
git add LICENSE VERIFY.md .github\workflows\timestamp.yml
git commit -m "Add APC license and timestamp workflow"
git push
```

Verify (quick)

1. After the workflow runs you will see `.timestamps/<TREE_HASH>.tsr` committed.
2. Follow the `VERIFY.md` instructions to run `openssl ts -verify` or the `ots verify` step for `.ots` proof files.


Common pitfalls and how to avoid confusion

- Do NOT keep both an APC `LICENSE` and the APC-VF variant as active license files in your project root. Keep one as `LICENSE` and, if you need to retain the other for reference, place it in a `licenses/` subfolder.
- Avoid copying multiple copies of IPClaim materials from other folders into the same repo; duplicate `README`, `LICENSE`, or `VERIFY.md` files will confuse integrators and automation.
- If you see copies of IPClaim in other workspace folders (e.g., `HopOn/IPClaim`, `codex-linker/IPClaim`, `internal_quarantine/.../IPClaim`), treat those as templates or archived copies. Use the canonical `IPClaim` root in this workspace as the authoritative source unless you have a reason to pick a different copy.


If you'd like, I can:

- Create a minimal PR in this repo that adds `QUICKSTART.md` (this file) and the README pointer (done).
- Consolidate the two license variants into an explicit `LICENSE_CHOICES.md` that explains differences and recommended defaults (done).
- Remove or relocate duplicate copies into an `examples/` or `archive/` folder to avoid accidental merging.

Tell me which of the above you'd like me to do next.

## ValueFlow (optional & archived)

The APC-VF (ValueFlow) license is intentionally separated from the default integration flow. It is archived in `licenses/LICENSE-APC-VF.md` and referenced here only for those who explicitly want to evaluate ValueFlow's profit-sharing model. Do not present it as the default; only adopt it after careful evaluation and community support.

