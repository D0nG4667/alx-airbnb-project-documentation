# 📊 Data Flow Diagram (DFD)

## 🎯 Objective

The objective of this task is to **visualize the flow of data** within the Airbnb Clone backend using a **Data Flow Diagram (DFD)**.
This diagram helps understand how data moves between **users, system processes, and data stores** for key operations such as user registration, property management, bookings, payments, and reviews.

---

## 🧠 Description

The DFD illustrates:

* **Data Sources / Inputs:** Guest, Host, Admin interactions
* **Processes:** User authentication, property listing, booking creation, payment processing, review management
* **Data Stores:** Users, Properties, Bookings, Payments, Reviews
* **Outputs / Responses:** Confirmation messages, notifications, reports

This diagram serves as a blueprint for **API design, database interaction, and system logic**.

---

## 🗺️ Mermaid Data Flow Diagram

```mermaid
flowchart TD
    %% External entities
    Guest[Guest]
    Host[Host]
    Admin[Admin]

    %% Processes
    Auth[User Authentication]
    PropertyMgmt[Property Management]
    BookingProc[Booking Process]
    PaymentProc[Payment Processing]
    ReviewMgmt[Review & Rating Management]
    Notification[Notifications]

    %% Data stores
    Users[Users DB]
    Properties[Properties DB]
    Bookings[Bookings DB]
    Payments[Payments DB]
    Reviews[Reviews DB]

    %% Guest interactions
    Guest --> Auth
    Guest --> PropertyMgmt
    Guest --> BookingProc
    Guest --> PaymentProc
    Guest --> ReviewMgmt

    %% Host interactions
    Host --> Auth
    Host --> PropertyMgmt
    Host --> BookingProc
    Host --> Notification

    %% Admin interactions
    Admin --> Auth
    Admin --> PropertyMgmt
    Admin --> BookingProc
    Admin --> PaymentProc
    Admin --> ReviewMgmt

    %% Processes to data stores
    Auth --> Users
    PropertyMgmt --> Properties
    BookingProc --> Bookings
    PaymentProc --> Payments
    ReviewMgmt --> Reviews
    BookingProc --> Notification
    PaymentProc --> Notification
```

---

## ⚙️ Tools & Repository Structure

| Item           | Description                                                      |
| -------------- | ---------------------------------------------------------------- |
| **Tool**       | Mermaid.js (DFD rendering in Markdown)                           |
| **Repository** | `alx-airbnb-project-documentation`                               |
| **Directory**  | `data-flow-diagram/`                                             |
| **File**       | `data-flow.png` (exported from Mermaid or Draw.io for reference) |

---

## ✅ Summary

This DFD provides a **high-level visualization** of how data moves within the Airbnb Clone backend.
It ensures clarity for **backend logic, database interactions, and API workflows** for all system actors.
