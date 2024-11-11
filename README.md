## ANALYSIS-OF-THE-2019-PRESIDENTIAL-ELECTION-RESULTS-IN-NIGERIA-

---

### PROJECT OVERVIEW

---

This project aims to analyze and visualize the 2019 Presidential Election results in Nigeria. The goal is to provide insights into the election process, including voter participation, party performance, and regional distribution of votes. By examining the results in-depth, I hope to draw conclusions on the electoral trends and patterns in Nigeria.  

---

### DATA SOURCES 

---

The primary data source for this project is the [Nigerian Election Results (1999-2019)](https://www.kaggle.com/datasets/xibilolu/nigerian-election-results-19992019) dataset available on Kaggle. The dataset includes comprehensive governorship and presidential election results data from 1999 to 2019.

The "2019pres" data was selected from [Nigerian Election Results (1999-2019)](https://www.kaggle.com/datasets/xibilolu/nigerian-election-results-19992019?select=2019pres.csv) and cleaned to provide relevant metrics for the analysis of the 2019 Presidential Election.

---

### INSTALLATIONS

---

To open and explore this project, you will need:

- [Power BI Desktop](https://powerbi.microsoft.com/desktop/) to view and interact with the Power BI reports.

---

#### Installation Steps:

1. Download and install Power BI Desktop.
   
2. Clone this repository to your local machine.
   
3. Open the `.pbix` files in Power BI to start exploring the visualizations.

---

### TOOLS USED

---

This analysis was conducted using the following tools:

- **Power BI Desktop** for data visualization and analysis.
  
- **Excel** for initial data cleaning and preparation.

---

### ANALYSIS PROCESS

---

For this project, I focused solely on the 2019 Nigerian Presidential Election results from the dataset found on Kaggle:[Nigerian Election Results (1999-2019)](https://www.kaggle.com/datasets/xibilolu/nigerian-election-results-19992019?select=2019pres.csv). Below is the step-by-step breakdown of the analysis process.

---

#### 1. **Data Collection**

   - From the Kaggle dataset, I downloaded "2019pres" data [Nigerian Election Results (1999-2019)](https://www.kaggle.com/datasets/xibilolu/nigerian-election-results-19992019?select=2019pres.csv) .
     
   The data included the following columns:

     - States
    
     - APC
       
     - PDP
       
     - PCP
       
     - ADC
       
     - APGA
       
     - Other Parties
       
     - Registered Voters
       
     - Total Votes
       
     - Winner

---

#### 2. **Data Cleaning and Preprocessing**

   - **Handling Missing Data**: Any missing values in key columns (such as registered voters or Total votes) were either filled or removed.
     
   - **Data Formatting**: The dataset was checked for inconsistencies in data types, ensuring that numerical values were correctly formatted (e.g., total votes, States).

---

#### 3. **Data Loading into Power BI**

I imported the cleaned "2019pres" data into Power BI.
     
   - Using **Power Query**, I created an additional calculated column for specific metric:
     
     - **Voter Turnout Percentage** per state: `[TOTAL VOTES]/ [REGISTERED VOTERS]`

---

#### 4. **Data Transformation**

   - **Aggregation**: I aggregated the data to compute totals for votes, winning party per state, and overall national statistics.
     
   - **Calculated Metrics**: I created new measures to visualize the following:
     
     - **Party Votes APC**: `= COUNTROWS(FILTER('2019pres', '2019pres'[WINNER] = "APC"))`
     - **Party Votes PDP**: `= COUNTROWS(FILTER('2019pres', '2019pres'[WINNER] = "PDP"))`
     - **Total ADC Votes**: `= SUM('2019pres'[ADC])`
     - **Total PDP Votes**: `= SUM('2019pres'[PDP])`
     - **Total APC Votes**: `= SUM('2019pres'[APC])`
     - **Total PCP Votes**: `= SUM('2019pres'[PCP])`
     - **Total APGA Votes**:`= SUM('2019pres'[APGA])`
     - **Total OTHER PARTIES**:`= SUM('2019pres'[OTHER PARTIES])`
     - **Winning Party**:`= IF([Party Votes PDP] > [Party Votes APC],"PDP","APC")`

---

### VISUALIZATION

