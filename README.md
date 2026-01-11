# Introduction to BigQuery

## Overview
This project is a hands-on activity from the Google Data Analytics course. It focuses on exploring **BigQuery**, writing basic SQL queries, and analyzing public datasets. The main dataset used is `london_bicycles` from the `bigquery-public-data` project. Through this project, I gained practical experience in querying large datasets using **SELECT**, **FROM**, and **WHERE** clauses.

---

## Project Objectives
- Explore the BigQuery interface and its main components.
- Access and preview public datasets.
- Write and execute basic SQL queries.
- Filter and aggregate data to answer analytical questions.
- Document query results for reference and verification.

---

## Project Structure
BigQuery_Intro_Project/
├─ README.md
├─ queries/
│ ├─ query_1.sql
│ ├─ query_2.sql
│ ├─ query_3.sql
│ ├─ query_4.sql
│ └─ query_5.sql
├─ screenshots/
│ ├─ query_1.png
│ ├─ query_2.png
│ ├─ query_3.png
│ ├─ query_4.png
│ └─ query_5.png


- **queries/**: Contains SQL files for each step of the project.  
- **screenshots/**: Contains screenshots of query results.  
- **README.md**: This documentation file.

---

## Steps Completed

### Step 1: Create BigQuery Account
- Created a Google BigQuery account.
- Accessed the BigQuery interface via Google Cloud Console.

### Step 2: Explore the Interface
- Navigated through **Explorer**, **Query Editor**, and **Job History**.
- Learned to locate datasets and tables, and to use the preview feature.

### Step 3: Access Public Dataset
- Searched for `London Bicycle` dataset.
- Selected `london_bicycles` dataset containing two tables: `cycle_hire` and `cycle_stations`.
- Previewed the `cycle_hire` table to understand its schema.

### Step 4: Basic SQL Queries
- **Query 1 (`query_1.sql`)**: Retrieve `end_station_name`.

SELECT
  end_station_name
FROM
  `bigquery-public-data.london_bicycles.cycle_hire`;
Query 2 (query_2.sql): Practice SELECT-FROM with the same column.

Query 3 (query_3.sql): Trips with duration >= 20 minutes.

SELECT
  duration,
  start_station_name
FROM
  `bigquery-public-data.london_bicycles.cycle_hire`
WHERE
  duration >= 1200;
Query 4 (query_4.sql): Optional query — station name for start_station_id = 111.

SELECT
  start_station_name
FROM
  `bigquery-public-data.london_bicycles.cycle_hire`
WHERE
  start_station_id = 111;
Query 5 (query_5.sql): Optional query — retrieve rental_id and station info for bike_id = 1710.

SELECT
  rental_id,
  start_station_id,
  start_station_name
FROM
  `bigquery-public-data.london_bicycles.cycle_hire`
WHERE
  bike_id = 1710;
Note: A sixth optional query for bike_model (bike_id = 58782) can be added separately if needed.

Step 5: Verify Results
Compared query outputs with the Introduction to BigQuery Solutions document.

Ensured all queries returned expected results.

Results
Successfully retrieved data from the london_bicycles.cycle_hire table.

Filtered trips based on duration and specific bike or station IDs.

Documented screenshots of all query results in the screenshots/ folder.

Conclusion
This project provided practical experience with BigQuery, public datasets, and SQL queries. It enhanced my ability to explore data, write queries, filter results, and interpret outputs — essential skills for a data analyst career.

Author
Mohammed Muteb Alzahrani
