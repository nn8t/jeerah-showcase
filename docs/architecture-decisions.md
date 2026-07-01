# Jeerah Architecture Decisions

> Public architecture decision records for Jeerah.

---

## Overview

This file documents public-safe architecture decisions made during the development of Jeerah.

It does not disclose private implementation details.

---

# ADR-001: Use Flutter for Mobile Apps

## Status

Accepted

## Context

Jeerah needs customer and driver mobile applications. Building separate native apps would increase development time and maintenance effort.

## Decision

Use Flutter for mobile app development.

## Rationale

- Cross-platform support
- Fast UI iteration
- Strong mobile performance
- Suitable for MVP and commercial startup development
- One development workflow for customer and driver apps

## Consequences

- Faster development
- Shared UI patterns
- Requires Dart/Flutter expertise
- Native integrations may need additional care

---

# ADR-002: Use Supabase as Backend Foundation

## Status

Accepted

## Context

Jeerah requires authentication, database, storage, realtime updates, and server-side workflows.

## Decision

Use Supabase as the backend platform.

## Rationale

- PostgreSQL foundation
- Built-in authentication
- Realtime support
- Storage support
- Edge Functions
- Good speed for MVP development

## Consequences

- Fast backend development
- Strong fit for early product development
- Requires careful security configuration
- Production hardening is still required

---

# ADR-003: Use PostgreSQL for Core Data

## Status

Accepted

## Context

Jeerah has relational data involving users, orders, trips, invoices, payments, and delivery events.

## Decision

Use PostgreSQL as the core database.

## Rationale

- Strong relational modeling
- Data consistency
- Mature ecosystem
- Good fit for lifecycle-driven systems
- Works well with Supabase

## Consequences

- Strong data structure
- Requires good schema design
- Requires careful access control

---

# ADR-004: Use State-Driven Workflows

## Status

Accepted

## Context

Orders and trips must move through predictable delivery stages.

## Decision

Model orders and trips using controlled lifecycle states.

## Rationale

- Easier to reason about
- Prevents invalid workflow jumps
- Improves admin monitoring
- Supports analytics
- Supports customer/driver clarity

## Consequences

- More upfront workflow design
- Requires validation for transitions
- Easier long-term maintenance

---

# ADR-005: Keep Sensitive Logic Private

## Status

Accepted

## Context

Jeerah includes commercially sensitive logic such as pricing, trip pooling, payments, driver earnings, and backend validation.

## Decision

Keep sensitive implementation private and publish only high-level documentation.

## Rationale

- Protect intellectual property
- Reduce security risk
- Preserve commercial advantage
- Still allow portfolio presentation

## Consequences

- Public repository cannot be run locally
- Reviewers see architecture instead of code
- Private demos or interviews may explain more at a high level

---

# ADR-006: Separate Public Showcase from Private Source

## Status

Accepted

## Context

The project needs to be visible for portfolio and professional review without exposing source code.

## Decision

Create a public showcase repository separate from the private production repository.

## Rationale

- Professional GitHub presence
- Protects source code
- Allows recruiters to understand the project
- Documents architecture and product direction

## Consequences

- Requires maintaining documentation
- Public files must be reviewed for sensitive data
- Production implementation remains private

---

## Future ADRs

Future decisions may document:

- Notification system design
- Payment provider strategy
- Admin permission model
- Production deployment approach
- Analytics architecture
- Monitoring strategy
- Beta launch architecture

---

<div align="center">

**Jeerah Architecture Decisions**

*Public decisions. Private implementation.*

</div>
