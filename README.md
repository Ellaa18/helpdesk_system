# ITIL-Based Helpdesk Ticketing System

A full-stack IT Service Management system built on the ITIL v4 framework. This web-based helpdesk system streamlines incident resolution, service requests, and knowledge sharing through modern technologies and best practices.

---

##  Live Demo

(Coming Soon – link to deployed version if available)

---

##  Key Features

-  **Ticket Management**: Users can create, view, and track incidents and service requests.
-  **Role-Based Access**: Custom dashboards for End Users, Technicians, and Administrators.
-  **Knowledge Base**: Searchable repository of solutions and IT articles.
-  **Reporting & Analytics**: Real-time dashboard and exportable reports.
-  **Notifications**: Email alerts for ticket updates and system events.
-  **API-First Design**: RESTful API for frontend/backend integration.

---

##  ITIL Integration

Built following **ITIL v4** best practices:
-  Incident & Problem Management
-  Service Request Management
-  Knowledge Management
-  Change Control (Planned)

Supports the **Four Dimensions of Service Management** and the **Service Value System**.

---

##  Tech Stack

### Frontend
- React.js 18.3.1
- Tailwind CSS 3.4.1
- TypeScript 5.5.3
- Vite 5.4.2

### Backend
- Node.js 20.x LTS
- Express.js 4.18.x
- JWT (Authentication)
- Nodemailer (Email Notifications)

### Database
- MySQL 8.0

---

## 👥 User Roles & Permissions

| Role        | Capabilities                                                                 |
|-------------|-------------------------------------------------------------------------------|
| **End User**   | Register, create/view tickets, comment, browse knowledge base              |
| **Technician** | Manage assigned tickets, update status, communicate with users, contribute articles |
| **Admin**      | Full access: manage users, assign roles, configure system, generate reports |

---

##  Database Overview

- `users`: user info & roles
- `tickets`: service requests and incidents
- `categories`: SLA and issue classification
- `comments`: ticket communication logs
- `audit_log`: system-wide tracking of data changes

Supports foreign key constraints and optimized with indexes for performance.

---

##  Security Features

- Bcrypt password hashing
- JWT-based auth with refresh tokens
- Role-Based Access Control (RBAC)
- CSRF/XSS/SQLi protections
- TLS 1.3 (data-in-transit), DB field encryption (data-at-rest)
- Audit logging and activity tracking

---

##  REST API Overview

### Auth Endpoints
- `POST /api/auth/register`
- `POST /api/auth/login`
- `POST /api/auth/logout`
- `POST /api/auth/refresh`

### Tickets
- `GET /api/tickets`
- `POST /api/tickets`
- `GET /api/tickets/:id`
- `PUT /api/tickets/:id`
- `POST /api/tickets/:id/comments`

### Users (Admin only)
- `GET /api/users`
- `GET /api/users/:id`
- `PUT /api/users/:id`
- `POST /api/users/:id/deactivate`

---

##  Installation

### Prerequisites
- Node.js v18+
- MySQL v8.0+
- npm
- Git

### Clone the Repo
```bash
git clone https://github.com/Ellaa18/helpdesk_system.git
cd helpdesk_system
