# IPClaim Developer Quickstart

This is the minimal path for adding IPClaim-style timestamped authorship proof to an existing Git repository.

## Short Version

1. Use the canonical APC license from `LICENSE`.
2. Copy `VERIFY.md`.
3. Copy `.github/workflows/timestamp.yml`.
4. Commit and push.
5. Verify the generated `.timestamps/<TREE_HASH>.tsr` proof.

The helper script automates those steps:

```bash
./stamp.sh <target-repo-path> [author-name] [apc|apc-vf]
```

Example:

```bash
./stamp.sh ~/projects/myrepo "Jane Doe" apc
```

## Default Choice

Use `apc` unless you have a clear reason to adopt the ValueFlow variant.

- `apc` copies the canonical APC license into the target repo as `LICENSE`.
- `apc-vf` copies the optional APC-VF variant into the target repo as `LICENSE`.

Only one active license should exist in the target repo root.

## Manual Setup

From your project root, assuming IPClaim is a sibling repository:

```bash
cp ../IPClaim/LICENSE ./LICENSE
cp ../IPClaim/VERIFY.md ./VERIFY.md
mkdir -p .github/workflows
cp ../IPClaim/.github/workflows/timestamp.yml ./.github/workflows/timestamp.yml
git add LICENSE VERIFY.md .github/workflows/timestamp.yml
git commit -m "Add APC license and timestamp workflow"
git push
```

Windows PowerShell equivalent:

```powershell
Copy-Item ..\IPClaim\LICENSE -Destination .\LICENSE
Copy-Item ..\IPClaim\VERIFY.md -Destination .\VERIFY.md
New-Item -ItemType Directory -Path .github\workflows -Force
Copy-Item ..\IPClaim\.github\workflows\timestamp.yml -Destination .github\workflows\timestamp.yml
git add LICENSE VERIFY.md .github\workflows\timestamp.yml
git commit -m "Add APC license and timestamp workflow"
git push
```

## What Happens On Push

The GitHub Actions workflow:

1. Computes the repository Git tree hash.
2. Requests an RFC 3161 timestamp token from FreeTSA.
3. Verifies the token immediately.
4. Commits the proof under `.timestamps/`.

The result is a public proof file tied to the exact repository contents.

## Verification

After the workflow runs, follow [VERIFY.md](VERIFY.md) to recompute the tree hash and verify the matching `.tsr` file with OpenSSL.

## Common Pitfalls

- Do not keep both APC and APC-VF as active root licenses.
- Do not copy staging folders or unrelated workspace material into the target repo.
- Do not treat commit dates as the proof. The proof target is the Git tree hash plus the timestamp token.
- If you choose APC-VF, do it deliberately and document that choice.

