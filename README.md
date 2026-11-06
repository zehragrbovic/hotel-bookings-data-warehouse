\# Hotel Bookings Data Warehouse \& Business Intelligence



A data warehousing and business intelligence project developed using Python, Pandas, MySQL, and Microsoft Power BI.



\## Overview



This project explores hotel booking data through a data preparation and ETL workflow, dimensional data modelling, relational database integration, and business intelligence reporting.



The original dataset contains over 119,000 hotel booking records. Python and Pandas were used to clean and transform the data, derive analytical attributes, and prepare fact and dimension tables for a dimensional data warehouse.



The resulting data model was implemented in MySQL and explored through a seven-page Power BI report.



\## Technologies



\- \*\*Python\*\* – Data preparation and ETL

\- \*\*Pandas\*\* – Data cleaning and transformation

\- \*\*MySQL\*\* – Relational database and data warehouse

\- \*\*MySQL Connector/Python\*\* – Database integration

\- \*\*Microsoft Power BI\*\* – Business intelligence and visualisation



\## Project Workflow



1\. \*\*Data preparation:\*\* Loaded and cleaned the original hotel bookings dataset using Pandas.

2\. \*\*Data transformation:\*\* Derived additional attributes, including total nights, arrival dates, weekdays, and booking revenue.

3\. \*\*Dimensional modelling:\*\* Designed a star-schema-based warehouse consisting of a central fact table and dimension tables.

4\. \*\*ETL and database loading:\*\* Prepared fact and dimension data and integrated Python with MySQL for data loading.

5\. \*\*Business intelligence:\*\* Explored the warehouse through a Power BI report containing seven analytical pages.



\## Data Warehouse Design



The warehouse consists of a central `fact\_bookings` table and the following dimension tables:



\- `dim\_country`

\- `dim\_customer\_type`

\- `dim\_date`

\- `dim\_deposit\_type`

\- `dim\_distribution\_channel`

\- `dim\_hotel`

\- `dim\_market\_segment`

\- `dim\_meal`

\- `dim\_reservation\_status`

\- `dim\_room\_type`



The fact table contains booking-related measures and foreign keys connecting bookings to their corresponding dimensions.



See \[`docs/star\_schema.png`](docs/star\_schema.png) for the schema diagram.



\## Power BI Report



The Power BI report contains seven pages exploring different aspects of hotel booking data:



1\. Revenue and average daily rate (ADR) over time.

2\. Required parking spaces by hotel.

3\. Revenue by market segment.

4\. Total nights by customer type.

5\. Cancellations over time.

6\. Average total nights by customer type.

7\. Booking nights and average ADR by weekday.



The report file is not included in this repository.



\## Repository Structure



```text

hotel-bookings-data-warehouse/

├── data/

│   └── dimensions/

├── docs/

│   └── star\_schema.png

├── notebooks/

│   ├── dataPrep.ipynb

│   └── ETL.ipynb

├── powerbi/

├── .gitignore

├── requirements.txt

└── README.md

```



\## Setup



\### Prerequisites



\- Python 3.11 or compatible version

\- MySQL Server

\- Jupyter Notebook

\- Microsoft Power BI Desktop (for viewing or recreating the report)



\### Python dependencies



Install the required packages:



```bash

pip install -r requirements.txt

```



\### Database configuration



The notebooks use environment variables for MySQL connection settings:



```text

DB\_HOST=localhost

DB\_USER=your\_mysql\_username

DB\_PASSWORD=your\_mysql\_password

DB\_NAME=hotel\_bookings

```



Configure these variables in your local environment before running the database-loading cells.



\### Data availability



The original dataset and generated CSV files are not currently distributed with this repository because their original source and redistribution licence have not yet been verified.



\## Notes



This repository documents an academic Business Intelligence project. The notebooks preserve the development workflow, including exploratory and experimental work.



The Power BI report and MySQL database are maintained separately from the public repository.



\## Author



Zehra Grbović

