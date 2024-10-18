# Data_Cleaning_in_Excel_using_Power_Query
This project involves data cleaning, transformation, and analysis of job offers in the Data Science field across the United States, using Power Query in Excel. The dataset is sourced from Kaggle and contains detailed job information, such as job title, salary estimates, company details, and more. 


![image](https://github.com/user-attachments/assets/f23d6099-01b3-42e2-833a-67bbb5c68284)


## Project Overview

The dataset provides insights into various job roles in the Data Science field, including information about salaries, company sizes, locations, and other factors that can influence job opportunities.

### Data Source

- **Dataset**: Kaggle - [Data Science Job Offers in USA](#)
- **Columns in the Dataset**:
  - Job Title
  - Salary Estimate
  - Job Description
  - Rating
  - Company Name
  - Location
  - Headquarters
  - Size (Number of Employees)
  - Founded Year
  - Type of Ownership
  - Industry
  - Sector
  - Revenue
  - Competitors

## Project Workflow

The following steps were performed in Power Query in Excel:

### Step 1: Data Cleaning and Column Creation
1. **Min_sal and Max_sal**: 
   - Created two new columns by extracting the minimum and maximum salary values from the existing `Salary Estimate` column.
2. **Role Type**:
   - Categorized the `Job Title` column into five major Data Science job roles: 
     - Data Scientist, Data Analyst, Data Engineer, Machine Learning Engineer, and Other.
   - This was done using a custom formula in Power Query.
3. **Location Correction**:
   - Split the `Location` column into two separate columns: one for the city and one for the state.
4. **State Abbreviation**:
   - Created a column for state abbreviations by removing null and inconsistent values.
5. **Full State Name**:
   - Imported an external `state_mapping` CSV file and merged it with the main dataset (`DS_jobs`) to create a column with the full state names using the “Merge Queries” option in Power Query.
  

     ![image](https://github.com/user-attachments/assets/e9e38bf4-9e29-47d0-a4c9-d5710ea5ef05)


### Step 2: Salary by Role Type
- Created a duplicate of the main query (`DS_jobs`), then selected only the columns `Role Type`, `Min_sal`, and `Max_sal`.
- Grouped the data by `Role Type` using the **Group By** option and created the following new columns:
  - **Job Count**: Total number of job postings for each role.
  - **Average Min Salary**: The average minimum salary for each role.
  - **Average Max Salary**: The average maximum salary for each role.


    ![image](https://github.com/user-attachments/assets/74c5e125-031a-4f6d-8c38-29223252a15b)


### Step 3: Salary by Company Size
- Created a reference query from the main dataset.
- Grouped the data by `Company Size` to calculate:
  - Number of job postings.
  - Average minimum and maximum salary for each company size.
 

    ![image](https://github.com/user-attachments/assets/ae773157-9c09-42a0-9802-2dd37918f680)


### Step 4: Salary by State
- Used a reference query to analyze the number of job roles and their respective average minimum and maximum salaries across different states.


  ![image](https://github.com/user-attachments/assets/616f8e30-6e48-4817-ad66-ee9d8b7fddf1)


### Step 5: Salary by Size and Role
- Created a duplicate query and analyzed the count of job roles and their corresponding salary ranges based on both company size and job role.


  ![image](https://github.com/user-attachments/assets/6fe7c783-ca8e-4e15-aa71-6960c49d0847)


## Key Insights
- **Role Type**: Identified the distribution of Data Science job roles and analyzed their respective salary ranges.
- **Company Size**: Examined how company size impacts the number of job postings and salary estimates.
- **State**: Showcased the regional differences in Data Science job postings and salaries across the United States.
- **Role and Size**: Analyzed how both job roles and company size together influence salary offers.

## Tools and Technologies Used
- **Microsoft Excel Power Query**: For data cleaning, transformation, and analysis.
- **CSV**: Used for importing additional state data (state abbreviations).
  
## How to Use
1. Clone the repository.
2. Open the Excel file and go to the Power Query Editor to see the data cleaning steps and transformations.
3. Explore the cleaned data and the various insights by role type, company size, and state.

## Conclusion
This project demonstrates the power of Excel and Power Query in cleaning and analyzing data, especially for job market analysis. The insights derived from the cleaned dataset provide valuable information on job roles, salary trends, and how different factors like location and company size impact job offers in the Data Science field.

