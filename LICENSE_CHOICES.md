# Choosing An IPClaim License

IPClaim has one normal default and one optional variant.

## Default: APC

Use [LICENSE](LICENSE) for ordinary IPClaim integrations.

APC is the canonical default because it keeps the claim simple:

- publish the work
- attach the APC terms
- record the verification method
- timestamp the repository state
- keep all rights reserved unless permission is granted separately

This is the clearest path for authorship proof and public disclosure without mixing in a revenue-sharing model.

## Optional: APC-VF

APC-VF is the ValueFlow variant. It is archived at [licenses/LICENSE-APC-VF.md](licenses/LICENSE-APC-VF.md) for deliberate evaluation.

Use it only when the project is intentionally adopting ValueFlow-style revenue sharing. Do not present it as the default IPClaim path.

## Practical Rule

1. Use APC by default.
2. Use APC-VF only when the project explicitly needs ValueFlow terms.
3. Keep only one active `LICENSE` file in the target repository root.
4. Keep non-active variants under `licenses/`, `archive/`, or another clearly non-authoritative location.

The goal is to avoid accidental policy mixing. A reader should know immediately which terms govern the work.
