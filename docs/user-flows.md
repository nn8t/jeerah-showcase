# Jeerah User Flows

> Public user flow documentation for Jeerah.

---

## Overview

Jeerah includes three major user flow categories:

- Customer flows
- Driver flows
- Admin flows

These flows are simplified for public documentation and do not reveal internal validation rules or private business logic.

---

## Customer Flow

```mermaid
flowchart TD
    A["Open App"] --> B["Phone OTP Login"]
    B --> C["Create Order"]
    C --> D["Wait for Trip"]
    D --> E["Driver Accepts Trip"]
    E --> F["Invoice Submitted"]
    F --> G["Final Payment Required"]
    G --> H["Select Payment Method"]
    H --> I["Track Delivery"]
    I --> J["Receive Order"]
```

---

## Driver Flow

```mermaid
flowchart TD
    A["Open Driver App"] --> B["Login"]
    B --> C["View Available Trips"]
    C --> D["Accept Shared Trip"]
    D --> E["Arrive at Store"]
    E --> F["Submit Invoice"]
    F --> G["Confirm Pickup"]
    G --> H["Start Delivery"]
    H --> I["Complete Delivery"]
```

---

## Admin Flow

```mermaid
flowchart TD
    A["Open Dashboard"] --> B["View Overview"]
    B --> C["Monitor Orders"]
    B --> D["Monitor Trips"]
    B --> E["Review Drivers"]
    B --> F["Review Customers"]
    C --> G["Detect Exceptions"]
    D --> G
    G --> H["Support Operations"]
```

---

## Cross-Role Flow

```mermaid
sequenceDiagram
    participant Customer
    participant Driver
    participant Backend
    participant Admin

    Customer->>Backend: Create order
    Driver->>Backend: Accept shared trip
    Driver->>Backend: Submit invoice
    Backend-->>Customer: Final payment required
    Customer->>Backend: Select payment method
    Driver->>Backend: Pick up and deliver
    Admin->>Backend: Monitor progress
```

---

## Notes

These flows are simplified and public-safe.

Private details not included:

- Exact state names
- Database logic
- Pricing rules
- Payment implementation
- Trip-pooling rules
- Admin permission model

---

<div align="center">

**Jeerah User Flows**

*Simple public flows for a private commercial product.*

</div>
