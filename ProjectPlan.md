# Project Plan
Grange Kalinich

### Overview
<sup><sup>Describe the overall goal of your project.</sub></sub>

The primary goal of this project is to analyze the relationship between educational attainment and unemployment rates across the United States at the state level. The project will involve acquiring, cleaning, integrating, and analyzing time series data from two distinct sources. The main point is to determine the correlation between various education metrics and employment outcomes over a multiple year period. I also plan to build a simple predictive model if the relationship is strong.


### Research Question(s)
<sup><sup>What is/are the question(s) you intend to address?</sub></sub>
1. What is the year to year correlation between the percentage of the population with a Bachelor’s degree or higher and the overall unemployment rate in U.S. states?
2. Can educational attainment variables, when combined with other demographic factors, be used to predict a state’s unemployment rate?


### Team
<sup><sup>Clearly define team member roles and responsibilities</sub></sub>

I have gotten permission to work on this project individually. 

**Role:** Data Scientist / Project Lead

**Responsibilities:**
- Data Acquisition: Write Python scripts to access ACS data and load the unemployment dataset.
- Data Integration & Cleaning: Standardize data formats, handle missing values, merge datasets.
- Analysis & Modeling: Perform correlation analysis, make visualizations, and develop the predictive model.
- Other Tasks: Complete the Project Plan, Interim Status Report, and Final Report, ensuring full reproducibility and transparency.

### Datasets
<sup><sup>Identify and describe the datasets that you will use. You need to use at least two different datasets that need to be integrated. If you are looking for ideas for datasets to use, please reach out via Campuswire.</sub></sub>

**Dataset 1: American Community Survey (ACS) 1-Year Estimates**

-  Source: U.S. Census Bureau - https://www.census.gov/data/developers/data-sets/acs-1year.html 
- Description: This dataset provides detailed demographic, social, economic, and housing data for areas with populations of 65,000 or more. This covers years from 2005 to 2024. Using the 1-year estimates which is beneficial for year to year analysis. To access the data I will be making API calls to it.


**Dataset 2: Unemployment in America Per US State**
- Source: Kaggle - https://www.kaggle.com/datasets/justin2028/unemployment-in-america-per-us-state?select=Unemployment+in+America+Per+US+State.csv
- Description: I have downloaded this csv from Kaggle, but the data is originally from the Bureau of Labor Statistics. It includes total unemployment and the percentage of the labor force that is unemployed, broken down by State/Area.

Since I plan on looking at the data by state and year, I will integrate this data by state and year. This will help analyze the relationships needed for this project. Each dataset has that information along with FIPS (Federal Information Processing Standard) codes. To see an example of each dataset you can see the file "Datasets Examples.ipynb" where I have loaded them and show 5 random samples from the year 2022.


### Timeline
<sup><sup>Document the plan and timeline for implementing your project including who will complete each task. Your plan must clearly address each of the requirements described above.</sub></sub>

**Part 1: Acquisition & Integration**
1. Finalize required ACS variables and write the correct Python API script. 
2. Load and profile the local unemployment CSV. 
3. Clean, standardize, and merge both datasets on State/FIPS code and Year.

<sup>This is also slightly more involved because in the ACS variables, although the data is there, the codes used might vary year by year. Since I plan to view over a longer period of time I will need to make sure I have all of the correct codes needed.</sup>

**Part 2: Profiling & Cleaning**
1. Address missing values, outliers, and data type inconsistencies. 
2. Create derived metrics as needed.
3. Conduct initial data profiling.

<sup>This part is just initially checking to make sure that the data makes sense (such as 100% being unemployed is probably bad) and setting up for any analysis that will be done later.</sup>

**Part 3: Analysis & Modeling**
1. Calculate and visualize correlation coefficients for my first research question. 
2. Develop a basic linear regression or classification model for prediction for my second research question.
3. Create any other plots to show the data as needed.

<sup>Since the data is ready at this point, I should be able to actually start looking at it and find meaning in it.</sup>

**Other Parts Within: Reporting**
1. Write the Interim Status Report (due mid-semester).
2. Write the Final Report in Markdown. 
3. Ensure full reproducibility and other requirements are met. 

<sup>In this part, I have different reports and requirements to complete which are listed here.</sup>


### Constraints
<sup><sup>Describe any known constraints.</sub></sub>
1. ACS 1-Year Geographic Constraint: The ACS 1-Year estimates are only published for areas (including states) with a population of 65,000 or more. This could cause some lapse in the data, however, because I am going by state it should not cause huge concern.
2. API Rate Limits: Since I am using an API there is potential for rate limiting when making API calls to the Census Bureau.
3. Licensing: Must ensure compliance with U.S. Government data policies for both Census and the unemployment data source, and properly cite both datasets. As well as making sure I look at the Kaggle site where I found the data for unemployment.


### Gaps
<sup><sup>Identify any known gaps or areas where you need additional input.</sub></sub>
1. Specific ACS Variables: As stated before, when trying to get the same data, the codes used might vary year by year. I will need to take a more in depth look and see what is relevant.
2. Handling Error: Since the ACS is only within a certain population, it might have higher chances for error as smaller states might be impacted. 
3. Inconsistent Counting: Although they are both information from the government they are from different sources. This makes total counts somewhat different in how they are presented. I will need to check ACS to see if there is anything more informative than just “population over 25” as the unemployment dataset has a different total population for states.


<sup><sub>*Your plan should anticipate later course topics even if you don’t yet know all the details. It is expected that your plan will evolve over time.*</sub></sup>
