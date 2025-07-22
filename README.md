# Public Health Resource Tracker

## Overview

The Public Health Resource Tracker is a multi-functional platform designed to connect individuals in urgent need of critical medical resources—such as blood, oxygen cylinders, and medicines—with verified donors and volunteers. Additionally, it provides real-time updates on hospital capacity and doctor availability to enable informed healthcare decisions during emergencies and public health crises.

---

## Core Features

- **Resource Listings & Requests**  
  Users can post offers (donations) or requests for medical resources including blood, oxygen, and medicines.

- **Search & Filtering**  
  Browse and filter listings by resource type, blood group, location, and urgency.

- **User Roles & Permissions**  
  Supports general users, verified donors, requesters, and admins with role-based access to features.

- **Matching & Notifications**  
  Verified donors receive real-time alerts when matching urgent requests are posted nearby.

- **Flagging System & Moderation**  
  Users can flag inaccurate or outdated listings. Admins review flags and moderate content to maintain trust.

- **Automatic Listing Expiry**  
  Listings auto-expire or become inactive after a predefined period (e.g., 48 hours) to keep information fresh.

- **Verification Process**  
  Donors and vendors submit identity or license documents which admins verify before granting access to sensitive features such as medicine listings.

---

## Additional Features

- **Hospital Status Updates**  
  Displays real-time information on hospital emergency capacity, available beds, ICU slots, and critical equipment.

- **Doctor Availability & Appointment Booking**  
  Shows doctors' specialties, consultation schedules, and enables booking for in-person or telemedicine consultations.

- **Integrated Emergency Support**  
  Combines resource availability with hospital and doctor data to provide holistic emergency assistance.

---

## Fraud Prevention & Safety Controls

- Only **verified donors and vendors** may post listings for sensitive items, especially medicines.

- Admins perform **document verification** and ongoing activity monitoring.

- Users are **warned about accepting medicines only from trusted sources** and listings are clearly tagged with verification status.

- A **flagging mechanism** allows community-driven reporting of suspicious or outdated listings.

- Listings have **automatic expiry** to reduce the risk of stale or inaccurate information.

---

## Technology Stack

- Backend: Node.js, Express.js  
- Database: MySQL  
- Frontend: HTML, CSS, JavaScript

---

## Database Overview

### Key Tables

| Table            | Description                                         |
| ---------------- | ------------------------------------------------- |
| `users`          | User information including roles and contacts.   |
| `donors`         | Donor-specific data such as blood type, location, availability. |
| `listings`       | Posted medical resource offers with status and timestamps. |
| `requests`       | Emergency resource needs posted by users.         |
| `flags`          | User-submitted reports on listings for moderation.|
| `admins`         | Admin user credentials and permissions.           |
| `hospitals`      | Hospital details and contacts.                      |
| `hospital_status`| Real-time hospital capacity and equipment availability. |
| `doctors`        | Doctor profiles, specialties, and schedules.       |
| `appointments`   | Booking records linking users and doctors.         |

---

## Example Usage Flow

1. A patient in Mirpur urgently needs an oxygen cylinder and posts a request specifying the type, location, and urgency.

2. Verified donors with oxygen available in Mirpur receive an alert and can respond to the request.

3. The system also shows nearby hospitals’ bed availability and doctors specializing in respiratory care.

4. The patient or helper chooses the best option — contacting donors, hospitals, or doctors as needed.

5. Users can flag listings if they become outdated or inaccurate; admins review these flags to maintain data integrity.

---

## Getting Started

### Installation

1. Clone the repository  
2. Set up the MySQL database using the provided schema  
3. Configure environment variables for database and email notifications  
4. Run the Node.js server  
5. Access the web interface to start using the platform

---

