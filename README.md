# Objective

This project is a modular ETL (Extract, Transform, Load) pipeline that automatically scrapes news headlines from the BBC News website, cleans and structures the data using pandas, and stores the results in a SQLite database and CSV file.

The pipeline is designed using production-style principles including modular architecture, logging, error handling, timestamping, and append-based data storage to maintain historical records.

The pipeline executes successfully and logs execution details for monitoring and debugging purposes.

---

# Objectives

* Automate web data extraction
* Implement structured ETL architecture
* Ensure data traceability using timestamps
* Enable historical data storage via append logic
* Introduce logging for monitoring and reliability

---

# Architecture Overview

```
Windows Task Scheduler
          ↓
        main.py
          ↓
   ┌───────────────┐
   │  Extract Layer │
   └───────────────┘
          ↓
   ┌───────────────┐
   │ Transform Layer│
   └───────────────┘
          ↓
   ┌───────────────┐
   │   Load Layer   │
   └───────────────┘
          ↓
 SQLite DB + CSV Output
```

---

# Technologies Used

* Python
* pandas
* BeautifulSoup (bs4)
* requests
* SQLite (sqlite3)
* Python logging module
* Windows Task Scheduler

---

# Pipeline Features

✔ Modular structure (Extract, Transform, Load separated)
✔ Centralized logging (`pipeline.log`)
✔ Error handling across stages
✔ Timestamp column (`scraped_at`)
✔ Append-based database loading (historical tracking)
✔ CSV export
✔ Automated execution

---

# Project Structure

```
bbc-etl-pipeline/
│
├── logs/
│   └── pipeline.log
│
├── src/
│   ├── extract.py
│   ├── transform.py
│   ├── load.py
│   └── main.py
│
├── news.db
├── bbc_news.csv
├── requirements.txt
└── README.md
```

---

# Database Design

Table: `news_titles`

| Column     | Description                 |
| ---------- | --------------------------- |
| S/N        | Serial number               |
| Title      | Headline text               |
| scraped_at | Timestamp of data ingestion |

The table uses append logic to preserve historical data across runs.

---

# What This Project Demonstrates

* Understanding of ETL architecture
* Modular software design
* Production-style logging
* Data lineage through timestamps
* Reliable repeated execution
* Clean project structuring

---

# Future Enhancements

* Add incremental loading (avoid duplicate ingestion)
* Migrate from SQLite to PostgreSQL
* Add unit testing
* Containerize using Docker
* Replace Windows Scheduler with workflow orchestration tool
* Deploy on cloud (AWS/GCP)




* I can help you write a LinkedIn project showcase post
* Or design your next advanced ETL (crypto or health API based)
* Or help you turn this into a CV bullet that passes ATS

You’re moving fast now 💪🔥
