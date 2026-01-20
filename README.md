# SQL---Data-Cleaning-Transformation

The objective was to apply robust SQL data engineering techniques to improve data quality, enforce consistency, and create a structured foundation for accurate housing market analysis.
________________________________________
## Business Problem

Real estate and housing datasets are often sourced from multiple systems and manual processes, resulting in:

-	Inconsistent date formats
-	Missing or incomplete address information
-	Poorly structured text fields
-	Duplicate transaction records
-	Redundant columns that add noise and complexity
  
These issues reduce trust in reporting, slow down analysis, and can lead to incorrect business conclusions if not addressed at the data layer.
________________________________________
## Data & Tools

Dataset:

Nashville housing transaction data containing property details, sale dates, prices, owner information, and vacancy indicators.

Tools & Technologies:

-	Microsoft SQL Server
-	T-SQL (CTEs, joins, window functions, string functions)
________________________________________
## Methodology

1.	Date Standardization
   
-	Converted inconsistent sale date formats into a standardized SQL DATE type
-	Created a new, clean date column to support accurate time-based analysis

2.	Missing Data Resolution

-	Identified missing property address records
-	Used self-joins and parcel identifiers to populate null addresses from related records
-	Ensured address completeness without introducing duplication

3.	Data Normalization & Column Structuring
   
-	Split compound address fields into separate address, city, and state columns
-	Applied string parsing techniques (SUBSTRING, CHARINDEX, PARSENAME) to normalize text fields
-	Improved data usability for filtering, grouping, and geographic analysis

4.	Categorical Value Standardization
   
-	Replaced inconsistent binary indicators (“Y” / “N”) with meaningful values (“Yes” / “No”)
-	Improved readability and reduced ambiguity for business users

5.	Duplicate Record Identification
   
-	Used a Common Table Expression (CTE) with ROW_NUMBER() to identify duplicate transactions
-	Applied business logic across multiple fields (parcel, price, date, legal reference) to ensure accuracy

6.	Schema Optimization
    
-	Removed redundant and unused columns
-	Streamlined the table structure to improve clarity, maintainability, and query performance
________________________________________
## Key Outcomes

-	A fully standardized and analysis-ready housing dataset
-	Improved data accuracy and consistency across critical fields
-	Elimination of duplicate and redundant records
-	Clear, well-structured columns optimized for BI and analytics use
________________________________________
## Business Value

This project demonstrates how SQL can be used not just for querying data, but for data quality management and transformation. The cleaned dataset enables:

-	More reliable housing market analysis
-	Faster and more accurate reporting
-	Reduced risk of misleading insights
-	Seamless integration with BI tools such as Power BI or Tableau
________________________________________
## Skills Demonstrated

-	Advanced SQL data cleaning and transformation
-	Use of CTEs and window functions
-	String manipulation and text parsing
-	Data quality validation and normalization
-	Schema design and optimization
-	Translating raw transactional data into analytics-ready structures
________________________________________
## Outcome

The final output is a clean, structured, and trustworthy housing dataset that can be confidently used for exploratory analysis, dashboards, and predictive modeling. 
This project highlights my ability to apply SQL as a core data analytics and data engineering   tool to solve real-world data quality challenges.
