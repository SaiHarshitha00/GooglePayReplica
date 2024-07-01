# GooglePayReplica
Overview
Google Pay Replica is a web application that simulates the functionalities of Google Pay, allowing users to manage transactions, pay bills, and check their balance. The application features user registration and login, a dashboard with various financial services, and a sidebar for profile management, help, and settings.

Features
Home Page: Provides buttons for user login and signup.
Registration Page: Allows users to register with their details.
Login Page: Users can log in using their credentials.
Dashboard:
Send Money: Users can send money to others via email.
Pay Bills: Users can pay bills by selecting the bill type and providing the service number.
Transaction History: Users can view a list of their past transactions.
Check Balance: Users can check their current account balance.
Sidebar:
Profile: Users can view and update their personal and bank details.
Help: Provides references and guidelines for using the website.
Settings: Allows users to change their password and update other settings.
Logout: Users can log out from the application.
Technologies Used
Front-End: HTML, CSS, JavaScript
Back-End: Node.js, Express.js
Database: MySQL
Authentication: JWT (JSON Web Tokens)
Email Service: Nodemailer for sending OTP and password reset emails
Installation
Prerequisites
Make sure you have the following installed:

Node.js (v14 or later)
MySQL (v8 or later)
Install Dependencies
bash
Copy code
npm install
Set Up the Database
Create a MySQL database and import the SQL schema.

sql
Copy code
CREATE DATABASE google_pay_replica;
USE google_pay_replica;

-- Add your SQL schema here
Update the database connection details in app.js with your MySQL credentials.

javascript
Copy code
const db = mysql.createConnection({
    host: 'localhost',
    user: 'your_mysql_username',
    password: 'your_mysql_password',
    database: 'google_pay_replica'
});
Start the Server
bash
Copy code
npm start
The server will start on http://localhost:3000.

API Endpoints
Authentication
POST /register: Register a new user.
POST /login: User login and JWT generation.
User Operations
GET /user: Get user details.
GET /api/get-pin: Get the user's PIN.
POST /api/verify-pin: Verify the user's PIN.
POST /api/update-user-settings: Update user settings like username, email, and phone.
POST /change-password: Change the user's password.
Transactions
POST /api/send-money: Send money to another user via email.
POST /api/pay-bills: Pay bills for a given bill type and account number.
GET /transactions: Get a list of the user's transactions.
GET /api/balance: Check the user's account balance.
Profile and Settings
GET /api/check-bank-details: Check if the user's bank details are set.
POST /api/bank-details: Update the user's bank details.
GET /dashboard: Get the user's name for the dashboard view.
POST /forgot-password: Request a password reset.
POST /reset-password/
: Reset the password using a reset token.
OTP and Help
POST /send-otp: Send an OTP to the recipient's email.
POST /verify-otp: Verify the OTP.
GET /help: Get help and references for using the website.
Usage
Navigate to the Home Page:

Click on Login or Signup to proceed to the registration or login page.
Register or Log In:

Fill in the required details and follow the instructions to register or log in.
Access the Dashboard:

Once logged in, you will be redirected to the dashboard where you can perform various actions such as sending money, paying bills, and checking your balance.
Use the Sidebar:

Profile: View and update personal and bank details.
Help: Check for references and guidelines.
Settings: Change your password and update settings.
Logout: Log out of your account.
