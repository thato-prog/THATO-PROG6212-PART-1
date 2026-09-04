# THATO-PROG6212-PART-1
# RaceDay System — README

## Project Overview
RaceDay is a web-based event management system designed to streamline marathon and race organisation. It enables organisers to create events, define categories and routes, track weather conditions, and manage contestant registrations and results. Contestants can register, view event details, and check outcomes after races.

## System Components
- **ERD**: Defines entities and relationships between organisers, events, categories, routes, weather, contestants, and registrations.
- **SQL Database Script**: Creates all tables, constraints, and inserts sample data for testing.
- **API Endpoint Plan**: Lists all backend endpoints for authentication, event management, registration, and results retrieval.
- **Documentation Folder (`/docs`)**: Contains the ERD diagram, API plan, SQL script, and README in PDF or Markdown format.



## Functional Requirements
The system supports:
- Authentication: Register and login endpoints for contestants.
- Event Management: Organisers can create, update, and view events.
- Category & Route Management: Each event includes multiple categories and routes.
- Weather Tracking: Weather data linked to each event.
- Registration: Contestants register for events and view their enrolments.
- Results: Publicly accessible race results per event.

---

## Database Schema Summary
Each table includes primary and foreign keys to maintain referential integrity.

- **Organiser**: Stores organiser details.
- **Event**: Links organisers to events with time and location.
- **Category**: Defines race types per event.
- **Route**: Describes event routes and distances.
- **Weather**: Records temperature and conditions for events.
- **Contestant**: Stores participant details.
- **Registration**: Connects contestants to events with status and date.

---

## API Overview
All endpoints follow REST conventions and start with `/api/`.

- **POST** `/api/auth/register` → Register a new contestant.
- **POST** `/api/auth/login` → Authenticate and return token.
- **GET** `/api/events` → Retrieve all events.
- **POST** `/api/events` → Create a new event (organiser only).
- **GET** `/api/categories` → List categories per event.
- **POST** `/api/registration` → Register contestant for event.
- **GET** `/api/results/{eventId}` → Retrieve event results.
- **GET** `/api/weather/{eventId}` → Retrieve weather conditions for an event.

---

## Testing Instructions
1. Run the SQL script in **SQL Server Management Studio (SSMS)**.
2. Verify table creation and sample inserts using:
   ```sql
   SELECT * FROM Event;
   SELECT * FROM Registration;

