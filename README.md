# Evenmate

An event planner app for **Software Engineering and Information Technologies** course at **Faculty of Technical Sciences**, Novi Sad, Serbia, 2024.

EventMate is a modern web and mobile application designed to streamline planning, organizing, and managing events of all types—including graduations, birthdays, weddings, conferences, team buildings, and more.

---

## Table of Contents
- [Project Overview](#project-overview)
- [Core Features](#core-features)
- [User Roles](#user-roles)
- [Main Functionalities](#main-functionalities)
- [Technology Stack](#technology-stack)
- [Non-Functional Requirements](#non-functional-requirements)
- [Development and Methodology](#development-and-methodology)
- [Testing](#testing)

---

## Project Overview

**EventMate** aims to offer an interactive platform for users to organize their events, discover and book services/products, manage budgets and agendas, and facilitate real-time communication among all involved parties.

---

## Core Features

- Event creation with flexible privacy (open/closed)
- Invite management and guest list tracking
- Calendar management and agenda scheduling
- Budget planning and automatic categorization
- Service and product listing, filtering, and booking/purchasing
- Real-time notifications and messaging
- Ratings, reviews, and administrator moderation
- Blocking/reporting system for improved safety

---

## User Roles

EventMate supports the following roles:

- **Unauthenticated User** (NK):  
  Can browse public events, services, and products. Limited access.  
- **Authenticated User** (AK):  
  Can manage profile, view and attend events, communicate with organizers.
- **Event Organizer** (OD):  
  Can create/manage events, budgets, agendas, guest lists, and interact with service providers and attendees.
- **Service/Product Provider** (PUP):  
  Can register businesses, manage service/product listings, handle reservations and orders, communicate with organizers.
- **Administrator** (A):  
  Manages categories, event types, reviews user reports, moderates comments, performs blocking/suspension.

---

## Main Functionalities

### User Management
- Registration and authentication (with email verification)
- Role-based profile and account control (including deactivation)
- Favorite events/services/products and calendar integration

### Event Management
- Custom event creation (type, name, description, privacy, location, date)
- Agenda and guest list planning
- Invitation system with rapid registration for invitees
- PDF export (agendas, guest lists, event details)

### Budget Planning
- Customizable budget tracking/meta-categorization of expenses
- Automatic updates on booking/purchase actions

### Service & Product Management
- Listing, filtering, and booking of services/products
- Provider-side CRUD operations with approval flow for new categories
- Visibility and availability management
- Price list management with PDF export

### Communication & Notifications
- Integrated chat (organizer-to-guest, organizer-to-provider)
- Real-time notifications with mute options
- Moderated commenting and rating
- Robust system for blocking/reporting users and handling disputes

---

## Technology Stack

**Frontend (Web):**
- Angular (TypeScript, HTML, CSS)
- Angular Material
- Figma for UI designs
- Leaflet for maps

**Backend:**
- Java & Spring Boot
- PostgreSQL
- SendGrid for email delivery 
- Notification persistence
- JasperReports for PDF generation

**Mobile:**
- Android (Java)
- Material Design 3

---

## Non-Functional Requirements

- Modular and maintainable Angular architecture (with AuthGuard, feature modules, linting, models)
- Secure JWT-based authentication and authorization
- Responsive UI with consistent styling
- Mapping and geolocation services across platforms
- Notifications stored for future reference
- Settings management via SharedPreferences
- Custom photo selection and uploads

---

## Development and Methodology

- Agile development (Sprints, Trello, retrospectives)
- Documentation and implementation in English
- Systematic filling of all methodology-related documentation

---

## Testing

- Java code: JUnit / TestNG
- Angular code: Jasmine
- E2E tests: Selenium

---

## Example: Event & Agenda

_Conference on Technology Innovations 2024_
- **Type:** Conference
- **Privacy:** Open
- **Location:** Belgrade, Serbia
- **Date:** November 1, 2024
- **Agenda:**
  - 09:00–09:30 – Registration
  - 09:30–10:00 – Opening Remarks
  - 10:00–11:00 – Lecture: Artificial Intelligence
  - ...and more

---


## Technical Installation & Run

### 1. Quick Start with Docker

- [Docker](https://docs.docker.com/engine/install/)
- [Docker Compose](https://docs.docker.com/compose/install/)
  
#### Step 1: Clone the repository

```bash
git clone https://github.com/zoricnadja/eventmate.git
cd eventmate
```

#### Step 2: Build & Start Containers

Rename, or create a copy of **.env.example** called **.env**

- `docker compose up -d` to start all containers
- `docker compose down` to remove all containers
  - use the `-v` flag to remove the volumes(data) as well

#### Step 3: Access the Application

Swagger 

If using IntelliJ IDEA:
- Go to Settings > Build, Execution, Deployment > Compiler > Enable **Build project automatically**
- Go to Advanced Settings > Enable **Allow auto-make to start even if developed application is currently running**

Routes
- **Frontend** at **http://localhost:4200**
- **Backend** at **http://localhost:8080**
  - **Swagger** at **http://localhost:8080/swagger-ui/index.html**
- **pgAdmin** at **http://localhost:5050**
  
---

### 2. Troubleshooting & Tips

- Rebuild containers if you change code:  
  `docker-compose up --build`
- Check container logs:  
  `docker-compose logs {service-name}`
- To run migrations or seed DB, mount scripts or customize Dockerfiles as needed.
- Make sure ports specified in `docker-compose.yml` do not conflict with other running services.

---

### 3. Mobile App (Android - Manual)

1. Open the mobile source (usually in `eventmate-mobile/`) in Android Studio.
2. Ensure backend container is running (`http://localhost:8080` reachable).
3. Edit any API URL settings if running on physical device vs. emulator.
4. Build and run on your emulator or device.

---

### 4. Advanced Configuration

- Modify `docker-compose.yml` to suit your dev/production environment.
- For environment-specific variables, use `.env` files supported by Docker Compose.
- Optional extras may require custom setup inside containers.

---

