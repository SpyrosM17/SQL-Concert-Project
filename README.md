# 🎸 RecordCompany Database Project

## 📝 Description
This project involves the design and development of a comprehensive relational database system for a record label. The system manages critical industry information, including artists, bands, producers, album releases, and the scheduling of live concerts at various venues.

## 🛠️ Tech Stack
* **Database:** MySQL (Relational Schema)
* **Backend:** Java (JDBC) for database connectivity and logic
* **Frontend:** Java Swing (GUI) for a desktop-based user interface

## 📂 Database Structure
The schema is designed to cover the full spectrum of music industry operations, organized into the following modules:
* **Personnel & Talent:** `person`, `band`, `artist`, `bandmember`.
* **Production:** `album`, `track`, `producer`, `recordcompany`.
* **Live Events:** `concert`, `venue`, `concert_history`.
* **Administration & Logs:** `dba`, `dbalog`, `action_log`.

## ⚙️ SQL Functionality

### Stored Procedures
* **`getscore`**: Calculates a venue's performance score based on capacity and historical experience.
* **`PlanConcert`**: Automates the scheduling, cancellation, or rescheduling of concert events.
* **`GetVenueData`**: Utilizes a **Cursor** to identify the optimal venue for a specific concert based on predefined criteria.

### Triggers
* **Constraint Enforcement:** Ensures business rules are met (e.g., preventing an artist from exceeding a maximum number of scheduled concerts).
* **Audit Logging:** Automatically records all `INSERT`, `UPDATE`, and `DELETE` actions in the `action_log` for the tables: `person`, `band`, `album`, `concert`, and `venue`.
* **Venue Management:** Automatically updates venue availability upon the completion of a concert.

## 🖥️ User Interface (GUI)
The Java Swing application provides an intuitive environment for:
* **Data Visualization:** Browse and view the contents of any table within the database.
* **CRUD Operations:** Seamlessly perform **Insert, Update, and Delete** actions via specialized popup modals.
* **Smart Scheduling:** A dedicated tool to find the most suitable venue for a concert based on the required capacity and artist needs.

