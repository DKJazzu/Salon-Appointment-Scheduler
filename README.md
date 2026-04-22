# Salon Appointment Scheduler

A high-precision Bash application that manages salon bookings using a PostgreSQL backend.

## Tech Stack
* **Scripting:** Bash (Bourne Again SHell)
* **Database:** PostgreSQL
* **CLI Tool:** `psql` (utilizing `--no-align` and `--tuples-only` for strict output formatting)

## Database Schema 

The system relies on a relational schema designed for data integrity and specific naming conventions (e.g., `table_name_id` primary keys).

### Tables
* **customers:** Tracks client names and unique phone numbers.
* **services:** A catalog of available salon treatments (cut, color, etc.).
* **appointments:** A junction table linking customers and services with a specific time.

## Installation & Setup

### 1. Database Initialization
To rebuild the database, log into your PostgreSQL instance and run:
```sql
CREATE DATABASE salon;
```
Then, import the schema:
```bash
psql -U postgres < salon.sql
```

### 2. Script Permissions
Before running the scheduler, ensure the script has execution permissions:
```bash
chmod +x salon.sh
```

### 3. Usage
Run the script from your terminal:
```bash
./salon.sh
```

---

## License

This project is licensed under the MIT License - see the LICENSE file for details.
