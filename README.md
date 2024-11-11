# Job Search Analytics Database

## Overview
This project is a relational database that tracks job applications, responses, and response times to demonstrate skills in database architecture, data modeling, and querying. It is designed as a portfolio piece to showcase capabilities in ELT/ETL processes and data analytics.

## Data Structure
Database Structure
The job application database is organized as a **snowflake schema**, with `application_facts` as the central fact table and several supporting dimension tables. This structure efficiently organizes job application data, capturing detailed information about applications, interviews, application materials, and related entities, allowing for advanced querying and scalability as new details are added.

### Central Fact Table
`application_facts`: Stores core information about each job application, including dates, outcomes, application status, and response details. This table connects to all relevant dimensions, enabling a comprehensive view of each application.
### Dimension Tables
- `application_materials`: Tracks submitted materials for each application, including resume versions, cover letters, and application platforms.
- `interviews`: Stores details on each interview round associated with an application, including type (e.g., phone or video), interview dates, and interviewers.
- `company_dim`: Contains information about companies applied to, such as company name, size, industry, and location.
- `job_dim`: Holds job-specific data, including job titles, location, and salary ranges.
- `date_dim`: Standardized date dimension that breaks down dates by day, month, year, and week, allowing for time-based analysis.
- `source_dim`: Identifies the source through which each application was submitted (e.g., LinkedIn, Welcome to the Jungle).
- `user_dim`: Tracks user details if multi-user functionality is added, capturing usernames and emails.

This structured, multi-dimensional approach offers flexibility for analyzing and presenting insights into job application trends, interview outcomes, and the evolution of submitted materials over time.

## Key Features
- Track job application timelines and outcomes
- Analyze trends in application responses by company, role, or industry
- Practice SQL queries for data analysis

## Usage
This project is intended solely for educational purposes as a demonstration of database and analytical skills.

## License
This project is licensed under a Creative Commons NonCommercial license. Please refer to the LICENSE file for details.

