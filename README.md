# Blood Bank and Donor Management System

A database-driven application designed to manage blood donors, donation records, blood inventory, recipients, and blood requests using Python, Flask, and MySQL.

## Overview

The Blood Bank and Donor Management System aims to simplify the organization of blood bank information through a centralized application.

The system is designed to maintain donor records, track available blood units, organize recipient information, and support blood request management.

This project demonstrates the application of Python web development, relational database design, SQL operations, and backend integration in a healthcare-related use case.

## Objectives

- Organize blood donor information.
- Maintain donation records.
- Manage blood inventory and availability.
- Store recipient information.
- Record and manage blood requests.
- Support blood-group compatibility checks.
- Generate useful inventory and administrative reports.

## Features

The following features should be considered implemented only if they are present and working in the source code.

- Donor registration and record management
- Donation record tracking
- Blood inventory management
- Recipient management
- Blood request management
- Blood-group compatibility checking
- Blood allocation workflows
- Administrative dashboard
- Database-driven reports

## Technology Stack

| Component | Technology |
|---|---|
| Backend | Python, Flask |
| Database | MySQL |
| Database queries | SQL |
| Frontend | HTML, CSS |
| Additional frontend functionality | JavaScript, if implemented |

## Project Structure

The following is an example structure. Adjust it to match the actual repository.

```text
blood-bank-management-system/
├── app.py
├── requirements.txt
├── .env.example
├── .gitignore
├── README.md
├── database/
│   ├── schema.sql
│   ├── sample_data.sql
│   ├── routines.sql
│   └── views_queries.sql
├── templates/
├── static/
│   ├── css/
│   ├── js/
│   └── images/
├── tests/
└── screenshots/
```

## Prerequisites

Before running the application, install:

- Python 3
- MySQL Server
- pip
- Git (optional, for cloning the repository)

The required Python version and MySQL version should be confirmed against the project dependencies.

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/blood-bank-management-system.git
cd blood-bank-management-system
```

Replace `YOUR_USERNAME` with your GitHub username.

### 2. Create a virtual environment

On Windows:

```bash
python -m venv venv
venv\Scripts\activate
```

On macOS or Linux:

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

The `requirements.txt` file must contain the actual dependencies used by the application.

### 4. Configure MySQL

Start MySQL Server and create a database using the project's schema.

For example, if the schema file creates the database itself:

```bash
mysql -u YOUR_MYSQL_USER -p < database/schema.sql
```

Enter your MySQL password when prompted.

If the schema does not create the database, create the database first and adjust the command accordingly.

### 5. Load sample data

If a sample-data script is available:

```bash
mysql -u YOUR_MYSQL_USER -p blood_bank_db < database/sample_data.sql
```

Use the actual database name defined in the schema.

Only use synthetic sample data in the public repository.

### 6. Install database routines

If the application requires stored procedures, functions, or views, execute the corresponding SQL scripts in the correct order.

For example:

```bash
mysql -u YOUR_MYSQL_USER -p blood_bank_db < database/routines.sql
mysql -u YOUR_MYSQL_USER -p blood_bank_db < database/views_queries.sql
```

These commands assume that the files and database name match the example structure.

**Important:** The database setup is incomplete until all required tables, functions, procedures, and views have been created successfully.

### 7. Configure environment variables

Create a local `.env` file using `.env.example` as a template, if the application supports environment-based configuration.

For example:

```env
DB_HOST=localhost
DB_PORT=3306
DB_NAME=blood_bank_db
DB_USER=your_mysql_user
DB_PASSWORD=your_local_password
```

These variable names are illustrative. Use the names expected by the actual application.

Never commit your real `.env` file or database passwords to GitHub.

### 8. Run the application

If `app.py` is the actual entry point:

```bash
python app.py
```

Open the local address printed by Flask in your terminal.

The default address is often:

```text
http://127.0.0.1:5000
```

The actual address and port depend on the application configuration.

## Database Design

The database is intended to support the following entities, subject to the actual schema:

- Donors
- Donations
- Blood inventory
- Recipients
- Blood requests
- Donation camps

Relational constraints and relationships should be documented according to the implemented schema.

## Testing and Verification

Before considering the project ready for demonstration, verify:

- The application starts without errors.
- The database connection succeeds.
- Donor records can be created and retrieved.
- Donation records are saved correctly.
- Inventory changes are handled correctly.
- Recipient and blood request operations work.
- Compatibility checks return expected results.
- Required SQL routines and views exist.
- Invalid inputs are handled appropriately.

Document the actual results of these tests before publishing.

## Known Limitations

List any incomplete or untested functionality here.

Potential areas requiring verification include:

- Database stored procedure and function availability
- API and database integration
- Blood inventory consistency
- Blood allocation and request processing
- Input validation and error handling
- Authentication and authorization

Do not describe an issue as resolved until it has been tested.

## Screenshots

Add genuine screenshots of the application to the `screenshots/` directory.

For example:

```markdown
![Dashboard](screenshots/dashboard.png)
```

Use the actual screenshot filename. Do not include screenshots that expose passwords, personal information, or confidential database records.

## Security Considerations

- Use environment variables for database credentials.
- Do not commit real donor or recipient information.
- Use synthetic data for demonstrations.
- Validate user input.
- Use parameterized SQL queries where applicable.
- Restrict access to administrative functions.
- Do not expose sensitive information in logs or error messages.

## Future Improvements

Potential improvements include:

- Automated inventory alerts
- Improved reporting and analytics
- Enhanced input validation
- Automated tests for database operations
- Improved authentication and access controls

These are potential improvements, not claims about implemented functionality.

## Author

Piyush Harish Chaudhari

## License

Specify the license under which this project is distributed.

If you choose the MIT License, add a corresponding `LICENSE` file and ensure its terms are appropriate for your intended use.
