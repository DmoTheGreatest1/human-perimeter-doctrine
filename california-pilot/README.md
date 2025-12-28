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
SPDX-License-Identifier: HPD-SPEECH-FREE-USE-BOUNDARY

=====================================================================
CALIFORNIA BROADBAND PILOT — WHAT CHANGES / WHAT DOESN'T
=====================================================================

Audience: Governor’s office, Agency heads, Procurement, Legal, IT Security, Finance
Purpose: One-page clarity insert for packets and executive review decks
Status: Informative (Policy-facing) — Non-operational. Not a deployment spec.

---------------------------------------------------------------------
WHAT CHANGES
---------------------------------------------------------------------

1) OVERSIGHT MOVES UPSTREAM (VERIFY & RELEASE)
- Payments and settlements are gated by pre-payment reconciliation.
- Goal: reduce "pay & chase" (clawbacks, audits months later) by preventing
  mismatches before disbursement.

2) ACCOUNTING BECOMES MECHANICAL (TRIPLE-ENTRY RECONCILIATION)
- Vendor claim (A), counterparty receipt (B), and physical/telemetry meter (C)
  are compared deterministically.
- Mismatches become discrete, auditable events — not narrative disputes.

3) DISPUTES BECOME RARE AND BOUNDED (RING-0 BACKSTOP)
- When automation cannot reconcile, the case freezes (escrow lock).
- A named Responsible Officer resolves a binary question:
  RATIFY (true) or SLASH (false), with typed attestation.
- The decision and rationale are append-only, hash-linked, and reviewable.

4) CIVIC REVENUE RECAPTURE IS POSSIBLE (NON-PUNITIVE WINDFALL)
- Reduction in overpayment, duplicated claims, and disputed settlement overhead
  creates measurable savings.
- Those savings can be treated as an efficiency dividend (a windfall), enabling:
  - more buildout per dollar
  - faster program cycles
  - improved public trust via clearer records

5) ENERGY AND OPERATIONS EFFICIENCY IMPROVES
- Better reconciliation reduces repeated investigations, data pulls, and manual
  back-and-forth workflows.
- The system prefers aggregation + proofs, reducing unnecessary data movement
  and operational churn.

---------------------------------------------------------------------
WHAT DOESN'T CHANGE
---------------------------------------------------------------------

1) NO NEW LAWS REQUIRED
- The pilot is an administrative integrity mechanism, not a statutory rewrite.
- Existing eligibility rules and program definitions remain intact.

2) THE STATE DOES NOT CEDE CONTROL
- California retains full control of program design, procurement, budget,
  vendor requirements, and decision authority.
- HPD is a framework; it is not an operator.

3) NO SUBSCRIBER DATA REQUIRED
- No subscriber-level PII is required for settlement integrity.
- The pilot prefers aggregates, headers, and cryptographic proofs over raw logs.

4) NO VENDOR LOCK-IN
- The approach is vendor-neutral: it is a reconciliation method, not a platform
  takeover.
- Integration can be sidecar / read-only where feasible.

5) NO “AI AUTOPILOT” FOR RIGHTS OR MONEY
- Automation detects and flags reconciliation failures.
- Final money-touching judgment is never delegated to AI.
- Human sovereignty is preserved at Ring-0.

6) THIS IS NOT PUNITIVE ENFORCEMENT
- The objective is accounting correctness and program integrity.
- The system reduces disputes by making claims provable, not by creating new
  penalties.

---------------------------------------------------------------------
FUNDING BOUNDARY (SPEECH VS USE)
---------------------------------------------------------------------

- Speech is free: reading, citing, discussing, critiquing, and forking HPD.
- Operational reliance is funded: integrating HPD into decision-bearing
  workflows (settlement/allocation/adjudication) requires institutional funding,
  resolved solely through California’s existing procurement/budget processes
  (including any privately mediated arrangements it elects to use).
- HPD does not set prices, invoice, collect, negotiate, supervise, audit, or
  enforce.

---------------------------------------------------------------------
ONE-SENTENCE CLOSE
---------------------------------------------------------------------

This pilot does not add bureaucracy; it replaces dispute-prone accounting with
verifiable settlement, producing measurable fraud reduction and an efficiency
dividend without punitive posture or vendor lock-in.
=====================================================================

=====================================================================
END OF DOCUMENT
=====================================================================
