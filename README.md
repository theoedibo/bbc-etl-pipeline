# Project Description

This project is a modular ETL (Extract, Transform, Load) pipeline that automatically scrapes news headlines from the BBC News website, cleans and structures the data using pandas, and stores the results in a SQLite database and CSV file.

The pipeline is designed using production-style principles including modular architecture, logging, error handling, timestamping, and append-based data storage to maintain historical records.

The pipeline executes successfully and logs execution details for monitoring and debugging purposes.

# Objectives

Automate web data extraction

Implement structured ETL architecture

Ensure data traceability using timestamps

Enable historical data storage via append logic

Introduce logging for monitoring and reliability

# Technologies Used

Python

pandas

BeautifulSoup (bs4)

requests

SQLite (sqlite3)

Python logging module

Windows Task Scheduler

# Pipeline Features

Modular structure (Extract, Transform, Load separated)

Centralized logging (pipeline.log)

Error handling across stages

Timestamp column (scraped_at)

Append-based database loading (historical tracking)

CSV export

Automated execution

# Future Enhancements

Add incremental loading (avoid duplicate ingestion)

Migrate from SQLite to PostgreSQL

Add unit testing

Containerize using Docker

Replace Windows Scheduler with workflow orchestration tool

Deploy on cloud (AWS/GCP)

# Contact

For collaborations or questions, reach out on www.linkedin.com/in/theophilus-edibo-7b857935a or edibotheophilus@gmail.com.

