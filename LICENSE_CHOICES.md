# Choosing a License for IPClaim Integrations

This repository presents a single, canonical license for everyday use and preserves the ValueFlow variant as an archived, optional reference. The purpose of this document is to make that explicit and avoid accidental mixing of policies.

Why this exists

- A clear, single default prevents integrators from guessing or merging conflicting license text. APC is the canonical default and is supplied at `LICENSE` in the repo root. The ValueFlow variant (APC-VF) is archived in `licenses/LICENSE-APC-VF.md` for explicit, deliberate evaluation only.

The canonical choice

- `LICENSE` (APC v1.1): "All Rights Reserved — Authorship & Patent Claim". Use this when you want to publish a timestamped, cryptographically verifiable claim and retain full rights. This is the recommended default for most projects.

ValueFlow (optional & archived)

The APC-VF (APC with ValueFlow) license is preserved only as `licenses/LICENSE-APC-VF.md`. It is intentionally separated from the canonical flow so integrators are not nudged toward adopting it. Review and adopt APC-VF only after careful consideration and community or legal agreement.

Decision rule (practical)

1. Use the canonical `LICENSE` (APC) unless you have a clear, documented reason to adopt ValueFlow.
2. If you decide to adopt ValueFlow, move `licenses/LICENSE-APC-VF.md` into your repo root as `LICENSE` and fill in pricing/contract placeholders before publishing.

Integration steps (canonical)

1. Copy `LICENSE` from the IPClaim root into your project root as `LICENSE`.
2. Edit the placeholders (Author name, date, hashes).
3. Copy `VERIFY.md` into your repo and add the timestamp workflow from `VERIFY.md` to `.github/workflows/timestamp.yml` (optional automation).
4. Commit and push.

Rules to avoid confusion

- Never keep both `LICENSE` (APC) and the APC-VF variant as active files in your repository root. Keep the non-active variant in `licenses/` or `archive/` for reference.
- Document your choice in `README.md` (short sentence) so integrators do not infer a fusion of rules.

If you want, I can move non-authoritative copies into an `examples/` or `archive/` folder and open a PR with those changes.
