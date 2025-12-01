# Lahman Baseball Database: SQL Analytics & Engineering

## Project Overview

This repository documents a series of advanced SQL engineering projects designed to analyze, restructure, and automate data workflows within the Lahman Baseball Database.

The projects demonstrate a comprehensive understanding of the full data lifecycle, progressing from complex relational analytics to backend database architecture. It showcases the ability to design scalable schemas, implement event-driven database logic, and ensure strict ACID compliance through transaction management in a Python/SQLite environment.

## Technical Competencies

* **Database Languages:** SQL (SQLite), Python (sqlite3)
* **Architectural Concepts:** Relational Database Design, Schema Normalization, Event-Driven Architecture
* **Data Integrity:** ACID Transactions, Error Handling, Atomic Operations
* **Advanced SQL:** Triggers, Views, Common Table Expressions (CTEs), Window Functions
* **ETL Processes:** Bulk Data Ingestion, Schema Evolution, Data Pruning

## Project Breakdown

### Project 6: Relational Analytics & Complex Joins
Focused on leveraging relational algebra to derive business insights from disparate datasets. This project moved beyond simple querying to perform multi-table joins and aggregations.

* **Complex Data Correlation:** Executed multi-table joins to analyze the relationship between player physical attributes and financial compensation, identifying significant correlations between weight classes and average salary.
* **Historical Performance Analysis:** Constructed comprehensive leaderboards for critical metrics (Runs, Hits) by aggregating career data across decades, identifying cross-generational performance outliers.
* **Pipeline Analysis:** Mapped amateur draft data to professional performance stats to evaluate the output quality of specific collegiate programs.

### Project 8: Database Architecture & ETL Pipelines
Simulated a production environment migration to practice Data Definition Language (DDL) and schema engineering.

* **Production Simulation:** Utilized Python's backup API to clone read-only production databases into writable local instances, creating a safe sandbox for schema modification.
* **Schema Evolution:** Designed and implemented custom tables with strict constraints (Primary Keys). Executed schema evolution strategies (ALTER TABLE) to accommodate changing data requirements without downtime.
* **Bulk ETL Operations:** Optimized data insertion workflows using INSERT INTO ... SELECT patterns to populate custom tables with thousands of processed records efficiently.

### Project 9: Automated Logic & Transaction Management
Implemented high-level database logic to automate maintenance tasks and enforce data consistency.

* **Event-Driven Automation:** Developed SQL Triggers (AFTER INSERT) to automatically synchronize data between related tables (e.g., syncing death records to biographical profiles), reducing the need for manual application-level updates.
* **Virtual Table Architecture:** Created SQL Views to abstract complex filtering logic, providing simplified access layers for reporting tools and reducing query complexity.
* **ACID Transaction Compliance:** Implemented robust transaction management using SAVEPOINT and ROLLBACK commands. This ensured that batch operations remained atomic, preventing partial data writes during simulated failure scenarios.

## Execution

1.  Ensure Python 3.x and the sqlite3 library are installed.
2.  The notebooks require access to the standard Lahman SQL database file.
3.  Execute the files in the order of complexity: `Project 6` -> `Project 8` -> `Project 9`.
