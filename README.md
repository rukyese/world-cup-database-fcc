# World Cup Database

This repository contains a PostgreSQL database for storing and querying World Cup game data. The database is structured with tables and relationships to represent World Cup tournaments, teams, and their match results.

## Files

- **`games.csv`**: CSV file containing World Cup game data, including year, round, winner, opponent, and goals scored.
- **`insert_data.sh`**: Shell script to insert data from `games.csv` into the PostgreSQL database.
- **`queries.sh`**: Shell script containing SQL queries to retrieve specific statistics from the database.
- **`worldcup.sql`** (optional): SQL dump of the `worldcup` database, containing schema and data.

## How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/rukyese/world-cup-database-fcc.git
   cd world-cup-database-fcc
   ```

2. Create the database schema by running the following commands in the `psql` interactive terminal:
   ```bash
   psql --username=your_username --dbname=postgres
   CREATE DATABASE worldcup;
   \c worldcup
   ```
   
3. Run the `insert_data.sh` script to insert data into the `teams` and `games` tables:
   ```bash
   chmod +x insert_data.sh
   ./insert_data.sh
   ```

4. Run the `queries.sh` script to execute queries and get specific statistics:
   ```bash
   chmod +x queries.sh
   ./queries.sh
   ```

5. (Optional) To restore the database from a dump, run:
   ```bash
   psql -U your_username -d worldcup < worldcup.sql
   ```
