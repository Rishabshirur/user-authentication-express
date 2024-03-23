This repository contains a basic Express server with user sign-up, login functionality, and middleware for authentication. Users can register with their first name, last name, email address, and password. Upon successful registration, passwords are hashed using bcrypt before being stored in the database. Registered users can then log in, and their credentials are validated against the stored hashed passwords.

## Usage
The application provides the following routes:

GET / - Root route, redirects users based on authentication and role.
GET /login - Renders a login form.
POST /login - Authenticates user login credentials.
GET /register - Renders a sign-up form.
POST /register - Registers a new user.
GET /protected - Route accessible only to authenticated users.
GET /admin - Route accessible only to authenticated users with admin role.
GET /logout - Logs out the user and redirects to the root route.
GET /error - Renders an error page.

## Client-Side Validation
Client-side validation is implemented using JavaScript to ensure that form inputs meet the specified criteria before submission. Errors are displayed to users if input data is invalid.

## Dependencies
express
express-session
bcrypt
body-parser
