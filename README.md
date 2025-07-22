# Public Health Resource Tracker

## Overview

The Public Health Resource Tracker is a web platform designed to help individuals, donors, volunteers, and healthcare seekers connect in emergencies by sharing and requesting essential medical resources such as blood, oxygen cylinders, and medicines. It aims to streamline resource availability during health crises like dengue outbreaks, COVID-19 surges, and other urgent situations.

---

## Features

### User Roles & Capabilities

#### General Users (Unregistered or Logged-in)
- Browse and search available resources by item type, blood group, location, and posting time.
- Post resource offers (e.g., “Available O+ blood”).
- Post urgent resource requests (e.g., “Need oxygen cylinder urgently”).
- Flag inaccurate or outdated listings.

#### Verified Donors/Volunteers
- Create and manage donor profiles including blood type and availability.
- View matching urgent requests within their area.
- Respond to requests and offer help.

#### Requesters (Patients or Helpers)
- Submit detailed emergency requests with urgency indicators.
- Receive alerts when matching donors post resources nearby.

#### Admins
- Monitor flagged listings for accuracy and appropriateness.
- Approve, reject, or mark listings as outdated.
- Manage abuse reports and maintain system integrity.

---

## How It Works

- **Homepage:** Displays urgent resource listings and requests nearby.
- **Search & Filter:** Users search by item, blood group, location, and urgency.
- **Posting:** Users submit offers or requests via simple forms.
- **Matching & Alerts:** Verified donors receive notifications of matching needs.
- **Moderation:** Admin panel for quality control and abuse management.
- **Auto-Expire:** Listings expire or get archived after 48 hours to keep data current.

---

## Technology Stack

- **Backend:** Node.js with Express framework
- **Database:** MySQL for relational data storage
- **Frontend:** HTML, CSS for user interface
- **Additional Tools:** Cron jobs or MySQL events for auto-expiration of listings

---

## Database Structure (Suggested Tables)

| Table      | Purpose                                      |
| ---------- | -------------------------------------------- |
| `users`    | Stores user details and roles                |
| `donors`   | Donor-specific data like blood type, area   |
| `listings` | Available resource postings (oxygen, blood, meds) |
| `requests` | Emergency resource needs                      |
| `flags`    | Reports of inaccurate or outdated listings   |
| `admins`   | Admin credentials and permissions             |

---

## API Endpoints (Example)

| Method | Endpoint            | Description                           |
| ------ | ------------------- | --------------------------------      |
| GET    | `/listings`         | Fetch available resource listings     |
| POST   | `/request`          | Submit a new emergency request        |
| POST   | `/donate`           | Post a resource offer                 |
| POST   | `/flag`             | Flag a listing                        |
| POST   | `/register-donor`   | Register as a verified donor          |
| GET    | `/matching-requests`| Get requests matching donor profile   |
| GET    | `/admin/flags`      | Admin view of flagged listings        |
| PUT    | `/admin/listings/approve` | Approve or reject listings      |

---

