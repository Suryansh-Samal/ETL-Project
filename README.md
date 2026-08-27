# ETL Project

An ETL (Extract, Transform, Load) project built using Python, Pandas, SQLAlchemy, and SQL Server.

The project demonstrates how messy nested JSON data can be extracted, transformed into structured datasets, and loaded into a SQL Server database.

## Project Overview

The pipeline currently follows this workflow:

```text
orders_ETL.json
      │
      ▼
   Extract
      │
      ▼
   Python
   + JSON
      │
      ▼
  Transform
      │
      ▼
   Pandas
      │
      ▼
     Load
      │
      ▼
 SQL Server
```

The source data contains nested customer and product information. Because of the structure of the JSON data, it is first loaded and processed using Python before being converted into structured Pandas DataFrames.

## Technologies Used

* Python
* Pandas
* SQLAlchemy
* pyodbc
* SQL Server
* Jupyter Notebook
* Git & GitHub

## ETL Process

### 1. Extract

The pipeline reads the source data from `orders_ETL.json` using Python's built-in `json` module.

### 2. Transform

The nested JSON data is processed using Python and Pandas.

The transformation process includes:

* Extracting customer information
* Extracting product information
* Flattening nested data
* Creating structured datasets
* Cleaning and transforming columns
* Preparing the data for database loading

### 3. Load

The transformed data is loaded into SQL Server using SQLAlchemy and `pyodbc`.

## Project Structure

```text
ETL-Project/
│
├── ETL_Project.ipynb
├── orders_ETL.json
├── requirements.txt
├── .gitignore
└── venv/                  # Local virtual environment, not tracked by Git
```

## Setup

Clone the repository:

```bash
git clone https://github.com/Suryansh-Samal/ETL-Project.git
```

Navigate into the project directory:

```bash
cd ETL-Project
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate the virtual environment on Windows:

```bash
venv\Scripts\activate
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

Open `ETL_Project.ipynb` in VS Code or Jupyter Notebook and run the cells.

## Future Improvements

This project is currently implemented as a manually executed ETL pipeline. The next goal is to evolve it into a more realistic and scalable data-engineering workflow.

Planned improvements include:

* Automating the ETL pipeline
* Implementing batch ingestion
* Scheduling regular data ingestion
* Handling incremental data loads
* Improving error handling and logging
* Adding data validation and quality checks
* Moving transformations toward a more production-oriented pipeline
* Exploring orchestration tools such as Apache Airflow
* Exploring distributed processing with PySpark as the dataset grows
* Improving the database loading strategy

The long-term goal is to turn this project from a manually executed notebook into an **automated and production-oriented ETL pipeline**.

## Current Status

**Completed:**

* JSON data extraction
* Processing of nested JSON data
* Data transformation using Pandas
* SQL Server connection using SQLAlchemy and pyodbc
* Loading transformed data into SQL Server
* Project environment and dependency management
* Git version control and GitHub repository

**Future:**

* Automated ingestion
* Batch processing
* Incremental loads
* Scheduling and orchestration
* Data quality checks
* Production-oriented pipeline architecture

## Author

**Suryansh**

This project is part of my journey toward building practical data-engineering projects and learning how ETL pipelines can be designed, automated, and scaled.
