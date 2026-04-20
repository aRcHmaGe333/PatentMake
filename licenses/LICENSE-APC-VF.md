# ALL RIGHTS RESERVED — AUTHORSHIP & PATENT CLAIM LICENSE
# with VALUEFLOW UNIVERSAL ACCESS

**APC-VF License v2.0 — February 2026**

---

## PREAMBLE

This license establishes two things simultaneously.

1. It claims complete ownership of this Work by right of first public disclosure, with cryptographic proof of authorship and date. 
2. It grants universal access to use the Work, on the condition that any profit generated from its use is shared with the Author.

The result is a Work that is fully owned and fully accessible. The Author is compensated. The world benefits. Nothing sits unused behind a locked door.
---

## PART ONE: AUTHORSHIP & PATENT CLAIM

### I. Declaration of Authorship

**Author:** [AUTHOR NAME OR ENTITY]

All files, ideas, methods, systems, processes, algorithms, architectures, designs, and functional content contained in this repository, project, or body of work (the "Work") are the original creation of the Author.

### II. Patent Claim by Public Record

This publication constitutes a public, timestamped, cryptographically verifiable patent claim over the Work as a whole.

| Proof Layer | Value |
|---|---|
| **Merkle Root Hash (SHA-512)** | `[INSERT ROOT HASH]` |
| **Git Tree Hash** (`HEAD^{tree}`) | `[INSERT TREE HASH]` |
| **RFC 3161 Timestamp Token** | `.timestamps/[HASH].tsr` |
| **Redundant Timestamp** | `.timestamps/[HASH].ots` |
| **Date of First Publication** | `[INSERT DATE UTC]` |

The Merkle root is a single cryptographic hash derived from the combined hashes of every file in this Work. A change to any file produces a different root. The root proves the integrity of the Work as an indivisible unit.

The Git tree hash identifies the exact tracked repository state used for publication. It is distinct from the Merkle root and should not be conflated with it.

The RFC 3161 timestamp token binds this root to a verified date and time, signed by an independent Time Stamping Authority. It is verifiable by anyone using OpenSSL. See `VERIFY.md` for instructions.

No prior public record of this Work exists. The Author published first.

### III. Scope of Claim

The Author is not a lawyer and does not employ researchers to search the world's archives for overlaps between this Work and prior claims.

Accordingly:

Every element of the Work that is patentable — under any jurisdiction, in any category, by any present or future standard — is claimed as the Author's patent by right of first public disclosure.

Every element of the Work that is not patentable — for any reason, under any law, in any jurisdiction — is not claimed as a patent. It remains the Author's original work, protected by copyright and by the authorship claim established in this license.

If any element that is not currently patentable becomes patentable in the future — through changes in law, the emergence of new jurisdictions, or the creation of new intellectual property categories — this disclosure constitutes a claim over that element as of the original publication date. The timestamp proves the Author disclosed it first. Future patentability does not alter who created it or when.

No prior art search was conducted. None was necessary. The Author created this Work, published it first, and claims everything the law permits.

### IV. Prior Art Defense

This publication establishes irrevocable prior art. Any third-party attempt to file a patent or intellectual property claim over any concept, method, or system described in this Work is subject to invalidation by this public record of prior disclosure.

### V. Duration

This license does not expire. There are no renewal fees, maintenance payments, or lapse conditions. The claim persists for as long as the public record is accessible.

---

## PART TWO: VALUEFLOW UNIVERSAL ACCESS

### VI. Grant of Use

Despite the all-rights-reserved status declared in Part One, the Author grants universal, worldwide, perpetual access to use, implement, manufacture, adapt, and build upon the Work, subject to the conditions in this Part.

Any party that generates profit from the use of the Work, or from any derivative of this Work, must compensate the Author according to the pricing model declared below.

### VII. Pricing Model

The Author declares the cost of using this Work by selecting one or more of the following models. Different use cases may carry different pricing.

#### Model A: Fixed Minimum Per Unit

The Author declares a minimum cost per unit produced, per instance deployed, or per transaction completed — as appropriate to the nature of the Work. There is no maximum. Compensation scales linearly with the number of units.

| Use Case | Minimum Per Unit |
|---|---|
| `[describe application]` | `[amount and currency]` |
| `[describe application]` | `[amount and currency]` |

The minimum is a floor. The user may pay above it. The Author does not negotiate it downward.

#### Model B: Profit Share

The Author declares a percentage of profit owed from each transaction, sale, subscription, or other income event derived from the Work or any derivative.

| Share | Percentage |
|---|---|
| Author | `[__]%` |
| User | `[__]%` |

If no percentage is declared, the default is 50/50.

Profit means the income remaining after the user's verified costs of production, materials, labor, distribution, and delivery are deducted from the total amount received. Taxes owed to governments are excluded, as they are not retained by either party.

The user's pre-use declaration (Section VIII) establishes the projected cost structure before production begins. This projection serves as the audit baseline. If the user's reported costs at settlement diverge materially from the declared projections without documented justification, the Author may treat the discrepancy as a breach of the declaration and pursue remedies under Section XV.

The Author may explicitly agree to alternative cost-accounting terms for a specific use case. Absent such agreement, the definition above applies.

#### Model C: Hybrid

The Author may assign different models to different use cases. Any combination of Model A and Model B is valid, including free access for specified categories (see Section XII).

---

### VIII. Pre-Use Declaration

Before manufacturing, deploying, or commercializing any product or service that incorporates this Work, the user must submit a written declaration stating:

1. Which APC-VF licensed works are incorporated, identified by repository URL or claim ID.
2. The intended use case, corresponding to an entry in the pricing table above.
3. The user's projected cost structure for the product or service: materials, labor, services, distribution, and intended unit price or service fee.

This declaration constitutes the contract between the user and the Author. It is completed and signed before production begins. The user is responsible for determining whether the product is commercially viable given the Author's stated terms.

---

## PART THREE: TERMS AND ENFORCEMENT

### XIII. Attribution

Every use of the Work or any derivative must include clear attribution to the Author:

1. The Author's name or designated identifier.
2. A link to the original repository or publication.
3. A statement that the work is used under APC-VF License v2.0.

Removal or concealment of attribution voids the grant of use under Part Two and converts continued use into infringement under Part One.

---

## HOW TO USE THIS LICENSE

1. Place this file as `LICENSE-APC-VF.md` or `LICENSE` in the root of your repository or project, but keep the filename consistent with your repo's references.
2. Fill in: Author name, hash values, publication date, and pricing model entries.
3. Add `VERIFY.md` for independent verification instructions.
4. Add `.github/workflows/timestamp.yml` for automated timestamping.
5. Commit and push. The claim is live.

See `VERIFY.md` for the manual timestamp process and automated workflow setup.

---

**© [AUTHOR NAME] — [YEAR]. All rights reserved.**
**Authorship & Patent Claim established by public record.**
**Universal access granted under ValueFlow profit sharing.**
