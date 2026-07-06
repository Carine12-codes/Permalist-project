# Permalist-project
A full-stack daily planner and to-do list web application created as part of The Complete Web Development Bootcamp on Udemy by Dr. Angela Yu. This project demonstrates how to transition from a volatile, memory-based data store to a persistent database management system by integrating a Node.js/Express backend with a PostgreSQL relational database.

🚀 Features
Full CRUD Functionality: Seamlessly add new items, read current list entries, and delete items from the checklist once completed.

Database Persistence: List items are securely stored and fetched from a local PostgreSQL database, ensuring data is retained even if the application server restarts.

Dynamic Server-Side Rendering: Utilizes Embedded JavaScript (EJS) templates to render dynamic HTML structures based on database records.

Responsive User Interface: Clean, aesthetic UI styled with responsive layout containers and standard custom styles.

🛠️ Tech Stack
Frontend: HTML5, CSS3, EJS (Embedded JavaScript Templates)

Backend: Node.js, Express.js

Database: PostgreSQL

Packages used: pg (PostgreSQL Client), dotenv, body-parser

⚙️ Installation & Setup
Follow these steps to set up and run the project locally:
```

1. Prerequisites
Ensure you have the following installed on your machine:

Node.js (v16 or higher recommended)

PostgreSQL

2. Database Setup
Open your PostgreSQL terminal (psql) or a GUI client like pgAdmin.

Create a new database named permalist:

SQL
CREATE DATABASE permalist;
Connect to your database and execute the following query to create the items table and add initial seed data:

SQL
CREATE TABLE items (
  id SERIAL PRIMARY KEY,
  title VARCHAR(255) NOT NULL
);

INSERT INTO items (title) VALUES ('Buy milk'), ('Finish coding challenge'), ('Work out');
3. Clone and Install Dependencies
Open your terminal, navigate into the project directory, and run:

Bash
npm install
4. Configure Environment Variables
```
Create a file named .env in the root directory of the project (make sure it is listed in your .gitignore so it stays secure!) and specify your database credentials:

Code snippet
```
PORT=3000
DB_USER=your_postgres_username
DB_HOST=localhost
DB_DATABASE=permalist
DB_PASSWORD=your_postgres_password
DB_PORT=5432
5. Running the Application
```
Start the development server using nodemon or standard Node:
```

Bash
npm start
or

Bash
nodemon index.js
```
Open your browser and navigate to http://localhost:3000 to interact with the app!
