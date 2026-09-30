# Fingerprint-Based ATM System

A Flask-based ATM Management System that provides user registration, login, fingerprint-based authentication, deposits, withdrawals, and balance/transaction management using a MySQL database.

## Features

- User Registration
- User Login
- Fingerprint-based authentication
- Deposit money
- Withdraw money
- View account balance
- Transaction management
- MySQL database integration
- Flask web interface
- User fingerprint image storage for authentication

## Technologies Used

- Python
- Flask
- PyMySQL
- MySQL
- HTML
- CSS
- XAMPP
- phpMyAdmin

## Project Structure

```text
FingerprintATM-Github/
│
├── static/
│   ├── users/
│   └── ...
│
├── templates/
│   ├── index.html
│   ├── Login.html
│   ├── Signup.html
│   ├── UserScreen.html
│   ├── Deposit.html
│   ├── Withdraw.html
│   └── ViewBalance.html
│
├── Main.py
├── requirements.txt
├── .gitignore
├── README.md
└── DB.txt
```

## Database

This project uses MySQL with a database named:

```text
atm
```

The database contains the following tables:

### Users Table

Stores user registration information such as:

- Username
- Password
- Contact number
- Email
- Address
- Gender

### Transaction Table

Stores:

- Username
- Transaction amount
- Transaction type
- Transaction date
- Total balance

## Database Setup

### Using phpMyAdmin

1. Start **MySQL** from the XAMPP Control Panel.
2. Open your browser.
3. Go to:

```text
http://localhost/phpmyadmin
```

4. Create a database named:

```text
atm
```

5. Select the `atm` database.
6. Execute the SQL commands provided in `DB.txt`.

## Installation

### 1. Install Python

Make sure Python is installed on your computer.

Check the Python version:

```bash
python --version
```

### 2. Install the Required Packages

Open PowerShell or Command Prompt in the project folder:

```bash
pip install -r requirements.txt
```

## Configuration

The application requires a running MySQL server.

Make sure MySQL is running before starting the Flask application.

The Flask application connects to MySQL using:

```text
Host: 127.0.0.1
Port: 3306
Database: atm
```

Make sure your local MySQL configuration matches the settings used in `Main.py`.

## How to Run

### 1. Start MySQL

Open the **XAMPP Control Panel** and click **Start** next to MySQL.

### 2. Start the Flask Application

Open PowerShell in the project folder and run:

```bash
python Main.py
```

### 3. Open the Application

After Flask starts, open your browser and visit:

```text
http://127.0.0.1:5000
```

## Application Workflow

```text
User
 │
 ▼
Registration
 │
 ▼
User Details + Fingerprint Image
 │
 ▼
Account Created
 │
 ▼
Login + Fingerprint Verification
 │
 ▼
User Dashboard
 ├── Deposit
 ├── Withdraw
 └── View Balance
```

### Fingerprint Testing

To test the fingerprint authentication:

1. Open the **Signup** page.
2. Enter the required user details.
3. Upload a fingerprint image.
4. Complete the registration.
5. The uploaded fingerprint image is automatically saved in:

```text
static/users/
```

6. Go to the **Login** page.
7. Enter the registered username and password.
8. Upload the corresponding fingerprint image.
9. The application verifies the uploaded fingerprint against the fingerprint saved during registration.

> **Note:** The project uses fingerprint image files for demonstration and testing. It does not directly connect to a physical fingerprint scanner.

## Security Note

This project is developed for educational and demonstration purposes.

Do not upload personal or sensitive fingerprint/biometric data to a public GitHub repository.

Sensitive information such as database passwords, API keys, and personal user data should not be committed to the repository.

## Future Improvements

- Use secure password hashing instead of storing plain-text passwords
- Use parameterized SQL queries
- Implement proper session management
- Store database credentials securely using environment variables
- Add stronger fingerprint/biometric verification
- Improve the user interface
- Add transaction history and reporting
- Deploy the application using a production-ready database and web server

## Disclaimer

This project is intended for educational purposes and demonstrates the integration of Flask, MySQL, and fingerprint-based authentication concepts in an ATM-style application.