# Jeerah FAQ

> Frequently asked questions about **Jeerah**, the smart trip-pooling delivery platform for remote communities.

---

## Repository Notice

This FAQ is part of the public showcase repository for Jeerah. It answers common product, technical, architecture, security, and commercial questions at a high level. It does not disclose private source code, backend implementation, database schema, trip-pooling algorithm, pricing logic, payment details, admin permissions, or sensitive business rules.

Jeerah is a commercial product under active development.

---

## Table of Contents

- [General Questions](#general-questions)
- [Product Questions](#product-questions)
- [Technical Questions](#technical-questions)
- [Architecture Questions](#architecture-questions)
- [Trip-Pooling Questions](#trip-pooling-questions)
- [Customer App Questions](#customer-app-questions)
- [Driver App Questions](#driver-app-questions)
- [Admin Dashboard Questions](#admin-dashboard-questions)
- [Payment Questions](#payment-questions)
- [Security Questions](#security-questions)
- [Repository Questions](#repository-questions)
- [Recruiter / Interview Questions](#recruiter--interview-questions)
- [Commercial Questions](#commercial-questions)
- [Future Plans](#future-plans)
- [Summary](#summary)

---

# General Questions

## What is Jeerah?

Jeerah is a smart trip-pooling delivery platform designed for remote communities, villages, and low-density areas where traditional delivery models are often too expensive or inefficient.

Instead of assigning one driver to one order, Jeerah is designed to group compatible orders into shared trips, making delivery more affordable for customers and more profitable for drivers.

---

## Is Jeerah a real project?

Yes.

Jeerah is an active commercial software project under development. This repository is a public showcase intended to present the project concept, architecture, feature scope, and engineering approach without exposing private implementation details.

---

## Is Jeerah open source?

No.

Jeerah is a private commercial product. The public repository is only a showcase and does not include executable source code.

---

## Why is the source code private?

The source code is private because Jeerah contains commercial business logic, delivery workflows, payment handling, pricing logic, trip-pooling concepts, and backend implementation details that are part of the project's intellectual property.

---

## Can I run Jeerah locally from this repository?

No.

This showcase repository does not include the application source code, database schema, Supabase configuration, Edge Functions, environment variables, or deployment files required to run the platform.

---

# Product Questions

## What problem does Jeerah solve?

Jeerah solves the problem of expensive and inefficient delivery in remote or low-density communities.

Traditional delivery platforms work best in dense cities. In villages and remote areas, each delivery may require a long trip, making it costly for the customer and unattractive for the driver.

Jeerah improves this model by supporting shared trips.

---

## Who is Jeerah built for?

Jeerah is built for:

- Customers in villages and remote communities.
- Drivers who want more valuable trips.
- Local delivery operations.
- Underserved regions.
- Future merchants and stores.
- Admin teams managing logistics operations.

---

## What makes Jeerah different from traditional delivery apps?

Traditional delivery apps often follow a one-order-one-driver model.

Jeerah is designed around a shared-trip model where multiple compatible orders can be grouped into a single driver trip. This improves trip value and reduces delivery cost per customer.

---

## Is Jeerah only for restaurants?

No.

Jeerah can support delivery from restaurants, groceries, pharmacies, stores, and other local merchants depending on business configuration and future expansion.

---

# Technical Questions

## What technologies are used?

Jeerah uses:

- Flutter
- Dart
- Supabase
- PostgreSQL
- TypeScript
- Deno
- Edge Functions
- Phone OTP authentication
- Git / GitHub
- Figma

---

## Why Flutter?

Flutter allows fast cross-platform mobile development with a single codebase. It is suitable for building both customer and driver applications with consistent UI and fast iteration.

---

## Why Supabase?

Supabase provides a strong backend foundation for an MVP and early commercial product. It includes PostgreSQL, authentication, storage, realtime capabilities, and Edge Functions.

---

## Why PostgreSQL?

PostgreSQL is suitable because Jeerah depends on structured relationships between users, orders, trips, invoices, payments, and delivery events.

---

## Does Jeerah use a backend?

Yes.

Jeerah uses backend services to validate workflows, manage state transitions, protect sensitive business logic, and coordinate order, trip, and payment actions.

---

# Architecture Questions

## What is the main architecture style?

Jeerah follows a mobile-first, cloud-backed, state-driven architecture.

The system uses customer and driver apps connected to backend workflows and a PostgreSQL database, with admin monitoring and future analytics.

---

## What does state-driven mean?

State-driven means that orders and trips move through controlled lifecycle states.

For example, an order may move from created to waiting for trip, then invoice submitted, payment due, picked up, out for delivery, and delivered.

This prevents invalid workflow jumps.

---

## Why are order and trip separated?

An order represents a customer request.

A trip represents a driver journey.

One trip may contain multiple orders. This separation is important because Jeerah is built around shared trips.

---

# Trip-Pooling Questions

## What is trip pooling?

Trip pooling means grouping multiple compatible orders into one shared driver trip.

Instead of:

```text
Order A → Driver A
Order B → Driver B
Order C → Driver C
```

Jeerah aims for:

```text
Order A
Order B  → Shared Trip → One Driver
Order C
```

---

## Why is trip pooling useful?

Trip pooling helps lower delivery cost, increase driver earnings, improve route efficiency, reduce wasted trips, and make delivery viable in remote areas.

---

## Is the trip-pooling algorithm published?

No.

The trip-pooling algorithm, matching criteria, pricing influence, capacity rules, and distance logic are private.

---

# Customer App Questions

## What can customers do?

Customers can login with phone OTP, create delivery orders, track order status, view final amount, select payment method, receive delivery updates, and view order history in future versions.

---

## Can customers pay online?

The platform includes an online payment workflow foundation. Payment provider implementation details are private.

---

## Can customers pay cash?

Yes. Jeerah supports a cash payment path concept as part of the customer final payment selection workflow.

---

## Why does payment happen after invoice submission?

In some delivery scenarios, the final merchant amount is only known after the driver reaches the merchant or store and receives the invoice amount. Jeerah supports this real-world flow.

---

# Driver App Questions

## What can drivers do?

Drivers can login, view available shared trips, accept shared trips, mark arrival at pickup location, submit invoice amount, optionally attach invoice image, confirm pickup, start delivery, and complete delivery workflow.

---

## Can one driver handle multiple orders?

Yes.

That is one of the main ideas behind Jeerah. A shared trip may include multiple compatible orders.

---

## Can drivers upload invoice images?

The platform supports optional invoice image submission as part of the invoice workflow.

---

## Are driver earnings shown publicly?

No.

Driver earnings logic and formulas are private commercial details.

---

# Admin Dashboard Questions

## What is the admin dashboard for?

The admin dashboard is intended to monitor and manage platform operations.

It can support order monitoring, trip monitoring, driver review, customer review, payment state monitoring, support workflows, and future analytics.

---

## Is the admin dashboard included in this repository?

No.

Only public documentation is included. Admin source code and internal operational tooling are private.

---

# Payment Questions

## Does Jeerah include payment workflows?

Yes.

Jeerah includes a final customer payment selection workflow after invoice-related steps.

---

## What payment methods are supported?

The public documentation describes online and cash payment paths at a high level. Actual provider details and implementation are private.

---

## Is payment code included?

No.

Payment code is not included in the public repository for security and commercial reasons.

---

## Is the pricing logic public?

No.

Pricing logic, final amount calculation, delivery fee rules, driver earnings, and payment calculations are private.

---

# Security Questions

## How does Jeerah handle authentication?

Jeerah uses phone OTP authentication. The actual provider configuration and implementation are private.

---

## How is user data protected?

At a high level, Jeerah is designed around authenticated access, role separation, backend validation, and database access controls.

---

## Are RLS policies included?

No.

Row Level Security policies are security-sensitive and are not included in the public repository.

---

## Are API keys included?

No.

The public repository must never include API keys, environment variables, service-role keys, payment keys, database URLs, or production secrets.

---

## Does the repository include real user data?

No.

Public showcase materials should never include real customer data, driver data, payment details, phone numbers, addresses, or production logs.

---

# Repository Questions

## What is included in the public repository?

The showcase repository may include:

- README.md
- FEATURES.md
- ARCHITECTURE.md
- SYSTEM_DESIGN.md
- ROADMAP.md
- SECURITY.md
- FAQ.md
- LICENSE.md
- NOTICE.md
- Public diagrams
- Sanitized screenshots
- High-level product documentation

---

## What is not included?

The repository does not include source code, database schema, Supabase configuration, Edge Functions, payment implementation, trip-pooling algorithm, pricing logic, driver earnings formula, production environment variables, admin source code, or real user data.

---

## Why have a public repository if the code is private?

A public showcase repository helps present the project professionally to recruiters, hiring managers, investors, technical interviewers, potential collaborators, and portfolio reviewers.

It allows the project to be discussed without exposing sensitive implementation.

---

# Recruiter / Interview Questions

## Can this project be discussed in interviews?

Yes.

The architecture, engineering decisions, product reasoning, technology choices, and development process can be discussed at a high level.

---

## What does Jeerah demonstrate technically?

Jeerah demonstrates experience with:

- Flutter mobile development.
- Supabase backend development.
- PostgreSQL data modeling.
- Authentication workflows.
- State-driven systems.
- Multi-actor workflows.
- Delivery lifecycle modeling.
- Payment workflow design.
- Driver/customer/admin product design.
- Security-aware architecture.
- Commercial product thinking.

---

## Is Jeerah suitable for a software engineering portfolio?

Yes.

Jeerah is especially strong as a portfolio project because it demonstrates a real business problem, multi-user workflows, backend state management, and commercial product design.

---

# Commercial Questions

## Is Jeerah a commercial product?

Yes.

Jeerah is being built as a commercial product, not an open-source demo.

---

## Can others copy or reuse Jeerah?

No.

The project is proprietary. Copying, redistributing, modifying, reverse engineering, or commercially using Jeerah without permission is not allowed.

---

## Can someone contribute code?

Not currently.

Jeerah is closed-source. External code contributions are not accepted at this stage.

---

# Future Plans

## What is the next major milestone?

The next major milestone is completing the delivery lifecycle, including final delivery confirmation, trip completion, and stronger operational visibility.

---

## What features are planned?

Planned features include push notifications, stronger admin dashboard, driver earnings dashboard, analytics, customer support tools, better delivery tracking, production hardening, and controlled beta launch.

---

## Will Jeerah support more regions?

The long-term vision includes regional expansion after MVP validation and operational readiness.

---

## Will Jeerah support merchants directly?

Merchant integration is a future possibility, but details are not publicly roadmapped.

---

# Summary

Jeerah is a private commercial delivery platform designed to make delivery viable in remote communities through smart shared trips.

This FAQ explains the project at a high level while protecting the implementation details that make Jeerah commercially valuable.

---

## Related Documents

- [`README.md`](README.md)
- [`FEATURES.md`](FEATURES.md)
- [`ARCHITECTURE.md`](ARCHITECTURE.md)
- [`SYSTEM_DESIGN.md`](SYSTEM_DESIGN.md)
- [`ROADMAP.md`](ROADMAP.md)
- [`SECURITY.md`](SECURITY.md)
- [`NOTICE.md`](NOTICE.md)
- [`LICENSE.md`](LICENSE.md)

---

<div align="center">

**Jeerah FAQ**

*Clear answers. Private implementation. Public product showcase.*

</div>
