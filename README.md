# # Node.js MySQL Form Application

This is a simple Node.js application that interacts with a MySQL database. It provides a web form to insert, list, and delete student records. The backend is built with Express.js and connects to a MySQL database using the `mysql2` package.

## Features

- **Insert Data**: Add new student records via a web form.
- **List Data**: Display all student records.
- **Delete Data**: Remove student records by name.

## Project Structure
- `public/form.html`: HTML form for user interaction.
- `public/server.js`: The main server file.
- `.gitignore`: Git ignore file.
- `.dockerignore`: Docker ignore file.
- `README.md`: Project documentation.
- `package.json`: Project metadata and dependencies.
- `package-lock.json`: Dependency tree.

## Prerequisites

- Node.js
- MySQL

## Getting Started

### 1. Clone the repository
```sh
git clone https://github.com/yourusername/your-repo.git
cd your-repo
```

### 2. Install dependencies
```sh
npm install
```
### 3. Configure MySQL Database
Set up your MySQL database and update the connection configuration in server.js:
```js
    const db = mysql.createConnection({
    host: 'your-database-host',
    user: 'your-database-user',
    password: 'your-database-password',
    database: 'your-database-name',
});
```

### 4. Run the Application
```sh
node server.js
```
The server will start at `http://localhost:3000`.

## Docker
### Build the Docker image
```sh
docker build -t node-mysql-form .
```
### Run the Docker container
```sh
docker run -p 3000:3000 -d node-mysql-form
```

## Usage
- Open your browser and navigate to http://localhost:3000.
- Use the form to insert student records.
- View the list of all records.
- Delete records by name.

## Files Description
### server.js
This file contains the main server logic, including:
- Setting up the Express server.
- Connecting to the MySQL database.
- Creating the students table if it doesn't exist.
- Handling routes for inserting, listing, and deleting data.

### form.html
This file contains the HTML form for user interaction, including:
- Form fields for name, address, and phone number.
- JavaScript functions for handling form submissions and displaying results.





