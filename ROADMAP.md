# Jeerah Roadmap

> Public product and engineering roadmap for **Jeerah**, a smart trip-pooling delivery platform for remote communities.

---

## Repository Notice

This document is part of the public showcase repository for Jeerah. It describes the roadmap at a high level only and does not disclose private source code, database schema, Supabase configuration, Edge Functions, pricing logic, payment provider implementation, trip-pooling algorithm, driver earnings model, deployment secrets, or sensitive business rules.

Jeerah is a commercial product under active development. This roadmap is intended for product presentation, portfolio review, and technical discussion.

---

## Table of Contents

- [Roadmap Overview](#roadmap-overview)
- [Roadmap Philosophy](#roadmap-philosophy)
- [Status Legend](#status-legend)
- [Current Product Direction](#current-product-direction)
- [Phase 0 — Product Discovery](#phase-0--product-discovery)
- [Phase 1 — Foundation](#phase-1--foundation)
- [Phase 2 — Authentication](#phase-2--authentication)
- [Phase 3 — Database Foundation](#phase-3--database-foundation)
- [Phase 4 — Driver Workflow Foundation](#phase-4--driver-workflow-foundation)
- [Phase 5 — Invoice Submission Workflow](#phase-5--invoice-submission-workflow)
- [Phase 6 — Customer Final Payment Workflow](#phase-6--customer-final-payment-workflow)
- [Phase 7 — Delivery Completion Workflow](#phase-7--delivery-completion-workflow)
- [Phase 8 — Notifications](#phase-8--notifications)
- [Phase 9 — Admin Dashboard](#phase-9--admin-dashboard)
- [Phase 10 — Analytics and Operations](#phase-10--analytics-and-operations)
- [Phase 11 — Production Hardening](#phase-11--production-hardening)
- [Phase 12 — Controlled Beta Launch](#phase-12--controlled-beta-launch)
- [Future Expansion](#future-expansion)
- [What Is Not Publicly Roadmapped](#what-is-not-publicly-roadmapped)
- [Summary](#summary)

---

## Roadmap Overview

Jeerah is being developed as a commercial delivery platform, not a simple demo application. The roadmap is organized around practical product milestones that move the platform from concept to operational MVP.

The platform includes multiple product surfaces and workflows:

- Customer mobile application
- Driver mobile application
- Admin dashboard
- Supabase backend foundation
- PostgreSQL state management
- Phone OTP authentication
- Shared trip lifecycle
- Invoice submission
- Final customer payment selection
- Delivery completion
- Operations and analytics

The roadmap intentionally separates public milestone descriptions from private implementation details.

---

## Roadmap Philosophy

Jeerah follows an incremental milestone-based development approach. Each phase is designed to be functional, testable, and valuable before moving to the next layer of complexity.

Each milestone should:

- Deliver a clear functional improvement.
- Be testable manually.
- Reduce technical uncertainty.
- Build on the previous foundation.
- Protect sensitive business logic.
- Move the project closer to MVP launch readiness.

The roadmap prioritizes lifecycle correctness first, then operational visibility, then production hardening and scale.

---

## Status Legend

| Status | Meaning |
|---|---|
| Completed | Functional foundation implemented and manually validated |
| In Progress | Actively being built or refined |
| Planned | Intended for upcoming development |
| Future | Long-term expansion candidate |
| Private | Internally defined but not publicly documented |

---

## Current Product Direction

Jeerah is currently moving from core lifecycle implementation toward delivery completion, operational readiness, and MVP preparation.

Current focus areas:

- Complete the order-to-delivery lifecycle.
- Finalize trip closing behavior.
- Improve customer status visibility.
- Prepare notification infrastructure.
- Strengthen admin monitoring.
- Prepare for controlled beta testing.
- Keep commercial logic private.

---

## Phase 0 — Product Discovery

### Goal

Define the core problem and validate the product direction.

### Scope

- Identify delivery challenges in remote communities.
- Define the shared-trip delivery model.
- Identify primary actors: customer, driver, admin.
- Define MVP boundaries.
- Identify commercial risks and technical constraints.
- Define success criteria.

### Status

Completed

### Deliverables

| Deliverable | Status |
|---|---|
| Problem definition | Completed |
| Product concept | Completed |
| High-level delivery model | Completed |
| Actor definition | Completed |
| MVP direction | Completed |
| Initial feature scope | Completed |

### Outcome

Jeerah's product direction was established around smart trip pooling for low-density delivery markets.

---

## Phase 1 — Foundation

### Goal

Build the initial project foundation across mobile, backend, and product documentation.

### Scope

- Establish Flutter application foundation.
- Define initial app navigation direction.
- Create early customer and driver app foundations.
- Set up project structure.
- Define private development workflow.
- Prepare public showcase strategy.

### Status

Completed

### Deliverables

| Deliverable | Status |
|---|---|
| Mobile foundation | Completed |
| Initial project structure | Completed |
| Development workflow | Completed |
| Product documentation foundation | Completed |
| Git workflow foundation | Completed |

### Key Decisions

- Flutter is used for mobile application development.
- Supabase is used as the backend foundation.
- Production source code remains private.
- A separate public showcase repository is used for portfolio presentation.

---

## Phase 2 — Authentication

### Goal

Implement a simple, mobile-first authentication model.

### Scope

- Phone number login.
- OTP verification.
- Session handling.
- Role-aware access foundation.
- Authenticated backend interactions.

### Status

Completed

### Deliverables

| Deliverable | Status |
|---|---|
| Phone OTP login | Completed |
| OTP verification flow | Completed |
| Session persistence foundation | Completed |
| Authenticated user context | Completed |
| Customer/driver access foundation | Completed |

### Rationale

Phone OTP authentication reduces onboarding friction and fits local mobile delivery usage better than traditional email/password registration.

---

## Phase 3 — Database Foundation

### Goal

Establish the data foundation required for users, orders, trips, payments, invoices, and operational lifecycle states.

### Scope

- PostgreSQL foundation.
- Core entity relationship design.
- Order lifecycle foundation.
- Trip lifecycle foundation.
- Payment state foundation.
- Role-aware access concept.
- Server-side workflow support.

### Status

Completed

### Deliverables

| Deliverable | Status |
|---|---|
| PostgreSQL foundation | Completed |
| Core lifecycle structure | Completed |
| Order state foundation | Completed |
| Trip state foundation | Completed |
| Payment state foundation | Completed |
| Driver workflow data foundation | Completed |
| Admin data foundation | Completed |

### Public Note

The actual database schema, table names, columns, SQL migrations, RLS policies, and internal relationships are private and are not included in this showcase repository.

---

## Phase 4 — Driver Workflow Foundation

### Goal

Allow drivers to interact with shared trips and progress through early delivery workflow stages.

### Scope

- Available trips view.
- Shared trip acceptance.
- Trip assignment.
- Driver active trip state.
- Arrival at store/merchant.
- Multi-order trip handling foundation.
- Pickup workflow foundation.

### Status

Completed

### Deliverables

| Deliverable | Status |
|---|---|
| Available shared trips | Completed |
| Driver trip acceptance | Completed |
| Driver active trip view | Completed |
| Merchant arrival action | Completed |
| Multi-order trip foundation | Completed |
| Pickup workflow foundation | Completed |

### Outcome

The driver can accept a shared trip and progress into the pickup and invoice stage.

---

## Phase 5 — Invoice Submission Workflow

### Goal

Allow drivers to submit merchant invoice details for each order in a shared trip.

### Scope

- Per-order invoice input.
- Amount-only invoice submission.
- Optional invoice image support.
- Final customer amount workflow trigger.
- Order state progression after invoice submission.
- Driver workflow continuation.

### Status

Completed

### Deliverables

| Deliverable | Status |
|---|---|
| Invoice amount input | Completed |
| Per-order invoice cards | Completed |
| Amount-only submission | Completed |
| Optional invoice image | Completed |
| Final amount update workflow | Completed |
| Order progression to payment requirement | Completed |

### Product Value

This milestone supports a real-world delivery scenario where the final merchant amount may only be known after the driver reaches the merchant or store.

### Private Details

The exact final amount calculation, fee logic, pricing rules, and payment conditions are private.

---

## Phase 6 — Customer Final Payment Workflow

### Goal

Allow the customer to select the final payment method after the invoice amount becomes available.

### Scope

- Final payment screen.
- Final payable amount display.
- Online payment path foundation.
- Cash payment path foundation.
- Payment state update.
- Order progression after payment selection.
- Driver workflow continuation after payment readiness.

### Status

Completed

### Deliverables

| Deliverable | Status |
|---|---|
| Final payment selection | Completed |
| Online payment selection | Completed |
| Cash payment selection | Completed |
| Payment state progression | Completed |
| Driver continuation after payment | Completed |
| Price lock concept | Completed |

### Outcome

The customer payment flow supports final payment selection and allows the driver workflow to continue after the required payment state is satisfied.

---

## Phase 7 — Delivery Completion Workflow

### Goal

Complete the full delivery lifecycle from pickup to final delivery confirmation.

### Scope

- Pickup confirmation refinement.
- Start delivery workflow.
- Out-for-delivery state.
- Delivery confirmation.
- Trip completion.
- Order completion.
- Driver earnings finalization concept.
- Admin completion visibility.

### Status

In Progress

### Deliverables

| Deliverable | Status |
|---|---|
| Pickup confirmation | Completed |
| Start delivery workflow | Completed |
| Out-for-delivery state | In Progress |
| Delivery confirmation | In Progress |
| Order completion | Planned |
| Trip completion | Planned |
| Driver earnings finalization | Planned |
| Admin completion visibility | Planned |

### Completion Criteria

This phase is complete when:

- Driver can complete delivery.
- All linked orders reach final completed state.
- Trip reaches completed state.
- Customer sees delivery completed.
- Admin can review completed trip/order state.
- Final operational records are ready for analytics.

---

## Phase 8 — Notifications

### Goal

Notify customers, drivers, and admins about important lifecycle events.

### Scope

- Order status notifications.
- Final payment required notification.
- Driver trip action notifications.
- Pickup notifications.
- Delivery notifications.
- Admin exception alerts.
- Notification preference foundation.

### Status

Planned

### Deliverables

| Deliverable | Status |
|---|---|
| Notification architecture | Planned |
| Customer order notifications | Planned |
| Payment required notifications | Planned |
| Driver action notifications | Planned |
| Delivery notifications | Planned |
| Admin alerts | Planned |

---

## Phase 9 — Admin Dashboard

### Goal

Build a stronger operational dashboard for monitoring orders, trips, drivers, customers, and platform health.

### Scope

- Orders overview.
- Trips overview.
- Driver management foundation.
- Customer management foundation.
- Payment state monitoring.
- Invoice review concept.
- Exception detection.
- Support workflow foundation.

### Status

In Progress / Planned

### Deliverables

| Deliverable | Status |
|---|---|
| Basic admin foundation | Completed |
| Orders monitoring | In Progress |
| Trips monitoring | In Progress |
| Driver monitoring | Planned |
| Customer monitoring | Planned |
| Payment state monitoring | Planned |
| Invoice review | Planned |
| Exception handling | Planned |

---

## Phase 10 — Analytics and Operations

### Goal

Add analytics and reporting features that help Jeerah operate as a real business.

### Scope

- Order metrics.
- Trip metrics.
- Driver metrics.
- Payment method metrics.
- Delivery performance metrics.
- Regional demand insights.
- Customer retention insights.
- Operational bottleneck detection.

### Status

Planned

### Deliverables

| Deliverable | Status |
|---|---|
| Order analytics | Planned |
| Trip analytics | Planned |
| Driver analytics | Planned |
| Payment analytics | Planned |
| Regional analytics | Planned |
| Admin reporting views | Planned |
| Exportable reports | Future |

---

## Phase 11 — Production Hardening

### Goal

Prepare Jeerah for real users, production traffic, and operational reliability.

### Scope

- Security review.
- Error handling improvements.
- Performance testing.
- Database optimization.
- Backup strategy.
- Monitoring and logging.
- Environment separation.
- Payment flow review.
- Edge case handling.
- Production deployment preparation.

### Status

Planned

### Deliverables

| Deliverable | Status |
|---|---|
| Security review | Planned |
| Performance review | Planned |
| Error monitoring | Planned |
| Logging improvements | Planned |
| Backup strategy | Planned |
| Production environment preparation | Planned |
| QA checklist | Planned |
| Deployment checklist | Planned |

---

## Phase 12 — Controlled Beta Launch

### Goal

Launch a controlled beta version with limited users and operational oversight.

### Scope

- Limited customer group.
- Limited driver group.
- Controlled delivery area.
- Manual support readiness.
- Admin monitoring.
- Payment validation.
- Driver feedback collection.
- Customer feedback collection.
- Iteration based on real usage.

### Status

Planned

### Deliverables

| Deliverable | Status |
|---|---|
| Beta area selection | Planned |
| Beta driver onboarding | Planned |
| Beta customer onboarding | Planned |
| Support process | Planned |
| Admin monitoring process | Planned |
| Feedback collection | Planned |
| Beta success metrics | Planned |

---

## Future Expansion

### Product Expansion

- Saved addresses.
- Ratings and reviews.
- Customer support chat.
- Driver wallet.
- Earnings dashboard.
- Promotions and coupons.
- Referral system.
- Merchant profiles.
- Regional delivery settings.
- Multi-language support.
- Live tracking.
- Better route guidance.

### Operational Expansion

- Multi-region management.
- Driver onboarding workflow.
- Driver document verification.
- Admin role permissions.
- Support ticketing.
- Incident management.
- Payment reconciliation.
- Refund management.
- Business intelligence dashboards.

### Technical Expansion

- CI/CD pipeline.
- Automated testing.
- Background jobs.
- Push notification service.
- Observability stack.
- Error monitoring.
- Analytics warehouse.
- Audit logs.
- Rate limiting.
- Better caching.
- Advanced search/filtering.
- More robust storage rules.

---

## What Is Not Publicly Roadmapped

Some areas are intentionally not described in detail:

- Trip-pooling algorithm.
- Matching logic.
- Pricing model.
- Delivery fee calculation.
- Driver earnings calculation.
- Payment provider details.
- Fraud prevention strategy.
- Admin permission matrix.
- Database schema roadmap.
- Internal technical milestones.
- Commercial launch strategy.
- Investor/business plans.
- Deployment infrastructure details.

---

## Summary

Jeerah's roadmap is focused on building a real commercial delivery platform step by step.

The project has already completed major foundations around authentication, database foundation, driver workflow, invoice submission, customer final payment selection, and shared trip lifecycle foundation.

The next major priority is completing the delivery lifecycle, followed by notifications, stronger admin tooling, analytics, production hardening, and a controlled beta launch.

---

## Related Documents

- [`README.md`](README.md)
- [`FEATURES.md`](FEATURES.md)
- [`ARCHITECTURE.md`](ARCHITECTURE.md)
- [`SYSTEM_DESIGN.md`](SYSTEM_DESIGN.md)
- [`SECURITY.md`](SECURITY.md)
- [`FAQ.md`](FAQ.md)
- [`NOTICE.md`](NOTICE.md)
- [`LICENSE.md`](LICENSE.md)

---

<div align="center">

**Jeerah Roadmap**

*From smart trip-pooling MVP to scalable remote-community delivery infrastructure.*

</div>
