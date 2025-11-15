🌍 World Capitals Quiz – Node.js + Express + PostgreSQL
A simple yet interactive geography quiz application where users guess the capital cities of different countries. Built with Express.js and PostgreSQL, this project demonstrates backend programming, database connectivity, and dynamic rendering using EJS.

🚀 How It Works

1. Database Setup (PostgreSQL)
A capitals table stores countries and their capital cities.
When the server starts, it fetches all the data and stores it in memory (quiz array).

2. Random Question Generation
Every time the user visits the home route (/), the app:
Resets the score.
Picks a random question from the quiz array.
Renders it on the page using EJS.

3. Answer Submission
When the user submits an answer:
The server checks if it matches the stored capital (case-insensitive).
Updates the score if correct.
Loads the next random question immediately.
Shows feedback (Correct / Wrong) on the page.

4. Continuous Quiz Flow
The quiz continues smoothly with each new question.

🧰 Frameworks & Technologies Used
Backend
Node.js – runtime environment for the server.
Express.js – handles routes, form submissions, and rendering responses.

Database
PostgreSQL – stores country-capital data.
pg (node-postgres) – used to connect and query the database.

Frontend / Rendering
EJS (Embedded JavaScript Templates) – renders dynamic content inside HTML.
CSS + Public folder – serves static files.

Middleware
body-parser – parses form data from user submissions.
express.static – serves CSS, images, and other assets.

⭐ Specialties of This Project
✔ Super lightweight architecture — only uses essential Node modules.
✔ Real database interaction using PostgreSQL (not static JSON).
✔ Smooth quiz experience with instant feedback for each answer.
✔ Randomization logic ensures unique questions each time.
✔ Clean separation of concerns:

DB logic

Quiz logic

Routing

Rendering

✔ Beginner-friendly project to learn:
Express routing
EJS templating
Database connectivity
Form handling

✔ Easy to expand — add scores, levels, user accounts, REST APIs, etc.

Installation Steps — World Capitals Quiz
Follow these exact, step-by-step instructions to set up the World Capitals Quiz repository locally.

1. Create the PostgreSQL database
Open a terminal (or PowerShell) and run: createdb world
If createdb isn't available, open psql and run:CREATE DATABASE world;

2. Create the capitals table in the world database
   psql -U postgres -d world -W
Then run these SQL commands in the psql prompt:
CREATE TABLE capitals (
  id SERIAL PRIMARY KEY,
  country VARCHAR(255),
  capital VARCHAR(255)
);

3. Import data from capitals.csv into the capitals table
\copy capitals(country, capital) FROM 'C:\full\path\to\capitals.csv' WITH CSV HEADER;

5. Update PostgreSQL credentials in your project
Open your project file (e.g. index.js or wherever you instantiate pg.Client) and set the correct user and password:
const db = new pg.Client({
  user: "postgres",         // your postgres username
  host: "localhost",
  database: "world",
  password: "your_password", // <-- set your password here
  port: 5432,
});
6. Open project directory in terminal
  cd '.\WORLD CAPITAL QUIZ'

8. Install Node dependencies
   run:npm install
   
9. Start the server
Run:node index.js
Open the app in your browser
http://localhost:3000







.
