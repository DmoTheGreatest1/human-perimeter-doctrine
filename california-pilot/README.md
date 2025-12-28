# California Broadband Pilot (Illustrative Case Study)

This directory documents how HPD could be applied to California
broadband subsidy administration.

This is not an active partnership.
No agreement exists.
No commitment is implied.

The purpose is demonstration only.

SPDX-License-Identifier: HPD-SPEECH-FREE-USE-BOUNDARY

=====================================================================
California Broadband Pilot — HPD Reference Implementation
=====================================================================

Status: Illustrative Pilot · Documentation-Only
Audience: ISP CTOs, Network Operations, Infrastructure Finance,
          State Technical Review
Posture: Non-Proprietary · Non-Enforcing · Non-Punitive

---------------------------------------------------------------------
1. Purpose (Plain English)
---------------------------------------------------------------------

This pilot demonstrates how the Human Perimeter Doctrine (HPD) can be
used as a neutral reconciliation and settlement framework for
California broadband programs.

The goal is not punishment, enforcement, or regulation.

The goal is to:

- improve accounting accuracy
- reduce audit friction
- accelerate settlement timelines
- recapture civic revenue lost to inefficiency
- surface energy and capacity waste as a secondary effect

HPD does not replace ISP billing systems, network operations, or
regulatory authority. It provides an evidence-based reconciliation
layer for programs involving public funds or performance claims.

---------------------------------------------------------------------
2. The Problem Being Addressed
---------------------------------------------------------------------

California broadband programs rely on reported coverage, capacity, and
performance claims to release subsidies and justify funding.

Current challenges include:

- retrospective and manual verification
- slow and adversarial audits
- clawback risk months after payment
- limited real-time visibility into settlement accuracy

This is not primarily a fraud problem.
It is an accounting and reconciliation problem.

---------------------------------------------------------------------
3. What HPD Changes / What It Does Not
---------------------------------------------------------------------

What HPD Changes:

- Introduces triple-source reconciliation for settlement decisions
- Links settlement velocity to data consistency
- Preserves human judgment in rare, bounded cases
- Makes inefficiency visible without accusation

What HPD Does Not Change:

- No packet inspection
- No routing changes
- No production agents
- No billing system replacement
- No enforcement actions
- No fines or penalties
- No vendor certification

HPD is observational and reconciliatory, not supervisory.

---------------------------------------------------------------------
4. Where HPD Sits in the Stack
---------------------------------------------------------------------

HPD operates out-of-band.

It observes settlement-relevant facts only and does not interfere with
production systems.

[ Network Operations ]     (unchanged)
[ Billing Systems ]        (unchanged)
[ Customer Management ]    (unchanged)

          ↓ periodic summaries

[ HPD Reconciliation Layer ]
          |
          ↓
[ Settlement Visibility ]

---------------------------------------------------------------------
5. Core Mechanism (Triple-Entry Reconciliation)
---------------------------------------------------------------------

Each settlement period produces an Evidence Pack consisting of:

Source A — Vendor Claim
  Cryptographic summary of service delivered.

Source B — Counterparty Receipt
  Signed acknowledgment of service receipt.

Source C — Independent Telemetry
  Infrastructure or third-party measurements bounding reality.

If all three reconcile, settlement proceeds automatically.
If they diverge, settlement pauses into escrow.

Only unresolved cases require human review.

---------------------------------------------------------------------
6. Ring-0 Human Review (Rare by Design)
---------------------------------------------------------------------

Ring-0 is a Finalization Terminal, not a dashboard.

Characteristics:

- Binary outcomes (ratify or reject)
- Mandatory written rationale
- Append-only record
- No negotiation
- No partial settlements

Most operators never encounter Ring-0 once consistency is established.

---------------------------------------------------------------------
7. Non-Punitive Posture
---------------------------------------------------------------------

HPD does not impose penalties.

Instead:

- clean data accelerates settlement
- inconsistent data slows settlement
- unresolved discrepancies remain visible

There are no retroactive clawbacks or fines initiated by HPD.

---------------------------------------------------------------------
8. Civic Revenue Recapture and Energy Efficiency
---------------------------------------------------------------------

A secondary effect of reconciliation is visibility into:

- over-provisioned capacity
- under-utilized infrastructure
- energy spent delivering unacknowledged service

This enables better subsidy sizing and planning.

Energy savings emerge as a windfall, not a mandate.

---------------------------------------------------------------------
9. Minimal Pilot Integration
---------------------------------------------------------------------

The pilot requires:

- batch hashes (not raw logs)
- local retention of raw logs
- a submission endpoint or manual upload
- no new hardware
- no production agents

The pilot can be scoped to non-critical traffic or a limited region.

---------------------------------------------------------------------
10. Funding Boundary
---------------------------------------------------------------------

HPD is free to read, cite, fork, and critique.

Operational reliance on HPD outputs for settlement decisions requires
institution-resolved funding for:

- internal oversight
- stewardship of the framework

HPD does not set prices, collect fees, negotiate terms, or enforce
payment.

Visibility is the only accountability mechanism.

---------------------------------------------------------------------
11. Success Criteria
---------------------------------------------------------------------

A successful pilot results in:

- faster settlement for clean operators
- fewer audits
- clearer accounting
- reduced political friction
- better long-term planning data

---------------------------------------------------------------------
12. Scope Disclaimer
---------------------------------------------------------------------

This repository provides documentation only.

It is not a service, product, compliance tool, or enforcement system.

---------------------------------------------------------------------
Summary
---------------------------------------------------------------------

This pilot shows how California broadband programs can reconcile money,
performance, and reality more efficiently without punishment,
surveillance, or operational disruption.

=====================================================================
END OF DOCUMENT
=====================================================================
