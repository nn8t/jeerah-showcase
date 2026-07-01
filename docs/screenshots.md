# Jeerah Screenshots

> Public screenshot guide for the Jeerah showcase repository.

---

## Purpose

This file defines how screenshots should be added to the public Jeerah repository safely.

Screenshots help recruiters, interviewers, and reviewers understand the product without exposing private data or sensitive implementation.

---

## Planned Screenshot Sections

### Customer App

Recommended screenshots:

- Login screen
- OTP verification
- Customer home
- Create order
- Active order tracking
- Final payment selection
- Delivery progress
- Order completed

Suggested folder:

```text
assets/customer-app/
```

---

### Driver App

Recommended screenshots:

- Driver login
- Available trips
- Trip details
- Active trip
- Merchant arrival
- Invoice submission
- Pickup confirmation
- Delivery progress
- Trip completion

Suggested folder:

```text
assets/driver-app/
```

---

### Admin Dashboard

Recommended screenshots:

- Dashboard overview
- Orders table
- Trips table
- Driver monitoring
- Customer monitoring
- Payment states
- Analytics preview

Suggested folder:

```text
assets/admin-dashboard/
```

---

## Screenshot Privacy Rules

Do not show:

- Real customer names
- Real driver names
- Real phone numbers
- Real addresses
- Payment details
- Internal IDs
- API responses
- Production URLs
- Admin secrets
- Database names
- Real invoice images

Use demo data only.

---

## Screenshot Naming Convention

Use clear lowercase filenames:

```text
customer-home.png
customer-payment-selection.png
driver-active-trip.png
driver-invoice-submission.png
admin-orders-overview.png
```

---

## Markdown Example

```md
![Customer Home](../assets/customer-app/customer-home.png)
```

---

## Future Improvements

- Add GIF walkthroughs
- Add annotated screenshots
- Add mobile mockups
- Add architecture images
- Add before/after workflow visuals

---

<div align="center">

**Jeerah Screenshots**

*Show the product. Protect the data.*

</div>
