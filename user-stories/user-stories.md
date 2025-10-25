# User Stories

This document captures user stories derived from the project's use case diagram. Each story follows the format: _As a [role], I want [feature] so that [benefit]._ These cover core interactions for the Airbnb Clone backend.

## Core User Stories

1. **User Registration & Authentication**  
   - As a **guest or host**, I want to register an account and log in using email/password or OAuth so that I can access personalized features and secure my account.

2. **Property Listing Management**  
   - As a **host**, I want to create, update, and remove property listings (including images and amenities) so that I can manage the availability and presentation of my listings.

3. **Search & Booking**  
   - As a **guest**, I want to search and filter properties by location, price, dates, and amenities so that I can find suitable accommodations and make bookings.

4. **Booking Lifecycle**  
   - As a **guest**, I want to make a booking for specific dates and receive a booking confirmation so that my reservation is recorded and protected from double-booking.

5. **Payment Processing**  
   - As a **guest**, I want to securely pay for my confirmed booking using a chosen payment method so that the transaction is processed and the host is notified.

6. **Reviews & Ratings**  
   - As a **guest**, I want to leave a review and rating after my stay so that future guests can benefit from my feedback and hosts can improve their offerings.

7. **Messaging**  
   - As a **guest or host**, I want to send and receive messages related to a booking or property so that I can coordinate details and ask questions.

8. **Notifications**  
   - As a **user**, I want to receive email and in-app notifications for booking confirmations, cancellations, and payment updates so that I stay informed about important changes.

9. **Admin Management**  
   - As an **admin**, I want to view and manage users, listings, bookings, and payments so that I can enforce policies and maintain platform health.

10. **Host Payouts & Financials**  
    - As a **host**, I want to view payouts, earnings reports, and transaction history so that I can reconcile earnings and manage my finances.

## Acceptance Criteria (examples)

- Registration returns a user object and a JWT token on success.  
- Property creation requires host authentication and returns the created property with an ID.  
- Booking creation fails if dates overlap with existing confirmed bookings for the same property.  
- Payments are tokenized; sensitive payment data is not stored on the platform.  
- Reviews can only be created for bookings with status `completed`.
