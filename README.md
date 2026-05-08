# Movie Search & Analytics System (Python + SQL + NoSQL)

## Project Overview
A professional console application that integrates relational (MySQL) and document-oriented (MongoDB) databases to provide a seamless movie search experience. Users can search for films from the Sakila database while all search activities are logged for real-time analytics.

## Key Features
* **Hybrid Search Engine:**
    * Search by keyword in movie titles (MySQL).
    * Search by genre and custom release year ranges (MySQL).
* **Search Analytics (MongoDB):**
    * Aggregated Top-5 popular keywords.
    * Popularity analysis by genres and time periods.
    * History of the last 5 unique search queries with timestamps.
* **Smart UI:** Pagination system (10 results per page) for comfortable reading in the console.

## Technical Stack
* **Language:** Python 3.12
* **Relational DB:** MySQL (Library: `pymysql`)
* **NoSQL DB:** MongoDB (Library: `pymongo`)
* **Security:** `python-dotenv` for environment variables management.

## Project Structure
* `movie_search_app.ipynb` — Main application logic and UI.
* `.env.example` — Template for required credentials (Host, User, Password).
* `requirements.txt` — List of Python dependencies.

## Business Logic
The application uses a **logging decorator-like approach** where every successful search triggers a `log_write()` function. This data is later processed using **MongoDB Aggregation Pipelines** to provide business insights into user preferences.
