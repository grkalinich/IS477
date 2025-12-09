# Interim Status Report
Grange Kalinich

### <sup><sup>Overview</sub></sub>
<sup><sup>Submit a report on the status of your project (~1000-1500 words)</sub></sub>


### General Update
<sup><sup>An update on each of the tasks described on your project plan including references to specific artifacts in your repository (such as datasets, scripts, workflows, workflow diagrams, etc).</sub></sub>

General things completed:
- I have added organized the files for each part of the project.
- Worked towards completing the timeline.


### Updated Timeline
<sup><sup>An updated timeline indicating the status of each task and when they will be completed.</sub></sub>

Below is my timeline copied from my [ProjectPLan.md](../ProjectPlanItems/ProjectPlan.md) with the tasks I have done crossed off. I think I am on a good pace and the next steps will be a lot more personally fun as working with the API took some time.

**~~Part 1: Acquisition & Integration~~**
1. ~~Finalize required ACS variables and write the correct Python API script.~~
2. ~~Load and profile the local unemployment CSV.~~
3. ~~Clean, standardize, and merge both datasets on State/FIPS code and Year.~~

<sup>~~This is also slightly more involved because in the ACS variables, although the data is there, the codes used might vary year by year. Since I plan to view over a longer period of time I will need to make sure I have all of the correct codes needed.~~</sup>

**~~Part 2: Profiling & Cleaning~~**
1. ~~Address missing values, outliers, and data type inconsistencies.~~ 
2. ~~Create derived metrics as needed.~~
3. Conduct initial data profiling.

<sup>This part is just initially checking to make sure that the data makes sense (such as 100% being unemployed is probably bad) ~~and setting up for any analysis that will be done later~~.</sup>

**Part 3: Analysis & Modeling**
1. Calculate and visualize correlation coefficients for my first research question. 
2. Develop a basic linear regression or classification model for prediction for my second research question.
3. Create any other plots to show the data as needed.

<sup>Since the data is ready at this point, I should be able to actually start looking at it and find meaning in it.</sup>

**Other Parts Within: Reporting**
1. ~~Write the Interim Status Report (due mid-semester).~~
2. Write the Final Report in Markdown. 
3. Ensure full reproducibility and other requirements are met. 

<sup>In this part, I have different reports and requirements to complete which are listed here.</sup>


### Changes Made
<sup><sup>A description of any changes to your project plan itself, in particular about your progress so far. Also include changes you made to your plan based on feedback you may have received for Milestone 2.</sub></sub>

I did not make any changes, but I did make some choices within the code of which variables and items I thought were good for future use.


### Summary of Contribution
<sup><sup>Each team member has to write a short summary of their contributions to the current milestone. Each team member should add and commit their contribution summary themselves to the shared github repo.</sub></sub>

Since I am working individually, I did everything. The main thing I did was create the [DataA&I+PC.ipynb](DataA&I+P&C.ipynb) which completed Part 1 and most of Part 2 of my timeline. This file walks step by step my thought process and any "changes" I may have made. Here is a summary (copied from the bottom of that document):
- Extract (API/CSV)
- Transform (Clean strings, aggregate averages, normalize columns)
- Validate (Compare vs. FRED)
- Derived Metrics (As needed in both)
- Load (Merge and Save)

The resulting [merged_education_unemployment_data.csv](../merged_education_unemployment_data.csv) being made.

This resulting file will be used for the rest of the parts of my timeline.