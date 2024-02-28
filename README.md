## Automated PostgreSQL Data Import Script Using Jupyter Notebook

### Description

This Python script is a powerful and efficient solution I designed to streamline my process of importing CSV files into a PostgreSQL database. My passion for PostgreSQL led me to develop this script. 
The script automates my tedious task of creating tables and importing data, allowing for a seamless and time-saving workflow.

  Features and Workflow of this script:
1. File Organization:
The script begins by identifying all CSV files in the current directory. It then creates a new directory named 'datasets' (or uses an existing one) and moves the CSV files into this directory.
This step ensures a well-organized and centralized location for dataset management.

3. CSV to Pandas DataFrames:
The script utilizes the Pandas library to read each CSV file into a Pandas DataFrame. It handles potential encoding issues, using ISO-8859-1 encoding when necessary, showcasing attention to data integrity.

4. Table Creation and Column Transformation:
The script dynamically generates table names based on file names and cleanses column names to remove spaces, special characters, and ensure compatibility with PostgreSQL conventions.
It then iterates over each DataFrame, determining column data types and creating corresponding tables in the PostgreSQL database.

5. PostgreSQL Database Connection:
The script establishes a connection to the PostgreSQL database using user-defined parameters such as hostname, database name, username, password, and port. This ensures flexibility for connecting to various PostgreSQL instances.

6. Data Import:
The script employs the psycopg2 library to execute SQL commands for table creation and data import. It leverages PostgreSQL's COPY command, a high-performance mechanism for loading large amounts of data.
This method significantly enhances the speed of data import compared to traditional row-by-row insertion.

7. Granting Permissions:
To ensure data accessibility, the script grants SELECT permissions on the created tables to the 'public' role, providing transparency and security in data sharing.

8. Closing Connections:
The script responsibly closes the database connection after each iteration, promoting resource efficiency and preventing potential connection issues.

Motivation and Skill Showcase:
I developed this script to help me master PostgreSQL since many people don’t like using it because of the complexity of data importation which is a common pain point in the data analysis workflow. 
The automation of table creation and data import demonstrates a commitment to efficiency and proficiency in both Python programming and PostgreSQL database management.

Conclusion:
With this script, I don’t only simplify the often-time-consuming task of importing data into PostgreSQL but also contributes a valuable tool to the data analysis community. 
The script's efficiency, organization, and adaptability make it a standout addition to any data analyst's toolkit, emphasizing a commitment to excellence in database management and automation.

