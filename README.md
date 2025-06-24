### **README.md File**

# BikeStores Sales Analysis with Python

## Overview

This project provides an in-depth analysis of the BikeStores sample database, a dataset simulating a typical retail bicycle store environment[1]. The primary goal is to extract data from a SQL Server database, perform exploratory data analysis (EDA) using Python, and derive actionable insights into sales performance, customer behavior, and product trends[2].

The entire analysis is conducted within a Jupyter Notebook, showcasing a complete workflow from database connection to final visualization.

## Key Questions Addressed

This analysis aims to answer critical business questions to inform strategic decisions, including:

-   What are the overall sales trends over time (2016-2018)?[3]
-   Which product categories and brands generate the most revenue?[4]
-   Who are the top customers by purchase volume and revenue?
-   Which stores are performing the best?
-   What is the geographical distribution of sales across different states?

---

## Technical Workflow

This project follows a structured data analysis pipeline:

1.  **Database Setup:** The project starts with a SQL Server database backup (`.bak` file), which is restored to create a fully functional relational database containing sales, customer, product, and staff data[1].
2.  **Data Extraction (Python & SQL):** A Python script within the Jupyter Notebook connects to the SQL Server database. SQL queries with `JOIN` clauses are used to extract and combine data from multiple tables (e.g., `orders`, `customers`, `products`)[3].
3.  **Data Processing & Cleaning:** The extracted data is loaded into a Pandas DataFrame. Standard data cleaning procedures are applied to ensure data quality.
4.  **Exploratory Data Analysis (EDA):** In-depth analysis is performed using Pandas to aggregate, group, and summarize the data to answer the key business questions.
5.  **Data Visualization:** Matplotlib and Seaborn are used to create a variety of charts and plots (e.g., bar charts, line graphs) to visualize the findings and make them easy to interpret.

---

## Tools and Technologies

-   **Database:** SQL Server
-   **Language:** Python
-   **Libraries:**
    -   `pyodbc` or `sqlalchemy` (for database connection)
    -   `pandas` (for data manipulation and analysis)
    -   `numpy` (for numerical operations)
    -   `matplotlib` & `seaborn` (for data visualization)
-   **Environment:** Jupyter Notebook

---

## Setup and Usage

To replicate this analysis on your local machine, follow these steps:

#### 1. Restore the Database

-   You need an instance of **SQL Server** (2016 or newer) running.
-   Using SQL Server Management Studio (SSMS), right-click on **Databases** and select **Restore Database**.
-   Choose **Device** and locate the `BikeStores.bak` file from this repository.
-   Complete the restore process.

#### 2. Set Up the Python Environment

-   **Clone the repository:**
    ```bash
    git clone https://github.com/MariamAsall/BikeStore-Analysis-.git
    cd BikeStore-Analysis-
    ```
-   **Create a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```
-   **Install dependencies:**
    ```bash
    pip install pandas numpy matplotlib seaborn pyodbc jupyterlab
    ```
    *(Note: You may also need to install the appropriate ODBC Driver for SQL Server).*

#### 3. Run the Analysis

-   **Update Connection String:** Open the `BikeStores.ipynb` notebook and update the database connection string in the first few cells to point to your local SQL Server instance.
-   **Launch Jupyter and run the notebook:**
    ```bash
    jupyter notebook
    ```
    Execute the cells in order to see the full analysis.

---
