# Flag Quiz App

A web-based quiz application that tests your knowledge of world flags. The app displays flags and asks users to identify the corresponding country names.

## Features

- Interactive flag quiz game
- PostgreSQL database integration for storing flag data
- Real-time scoring
- Responsive web interface using EJS templates
- Express.js backend

## Prerequisites

- Node.js (version 14 or higher)
- PostgreSQL database
- npm or yarn package manager

## Installation

1. Clone the repository or download the project files.

2. Navigate to the project directory:
   ```
   cd "8.2 Postgres Read"
   ```

3. Install dependencies:
   ```
   npm install
   ```

## Database Setup

1. Ensure PostgreSQL is installed and running on your system.

2. Create a database named `flags`:
   ```
   createdb flags
   ```

3. Import the flag data from `flags.csv` into your PostgreSQL database. You can use a tool like pgAdmin or the command line:
   ```
   psql -d flags -c "\COPY flags FROM 'flags.csv' CSV HEADER"
   ```

4. Update the database connection details in `index.js` if necessary (default: user=postgres, host=localhost, database=flags, password=anup@1902, port=5432).

## Usage

1. Start the application:
   ```
   node index.js
   ```

2. Open your web browser and navigate to `http://localhost:3000`.

3. The quiz will start, displaying flags one by one. Enter the country name in the input field and submit.

4. Your score will be tracked, and the game ends when you submit an incorrect answer.

## Project Structure

- `index.js`: Main application file with Express server and database logic
- `solution.js`: Additional solution or utility file
- `views/index.ejs`: EJS template for the quiz interface
- `public/styles/main.css`: CSS styles for the application
- `public/images/`: Directory for flag images
- `flags.csv`: CSV file containing flag data
- `package.json`: Node.js dependencies and scripts

## Dependencies

- express: Web framework for Node.js
- pg: PostgreSQL client for Node.js
- ejs: Templating engine
- body-parser: Middleware for parsing request bodies
- axios: HTTP client (may be used for additional features)

