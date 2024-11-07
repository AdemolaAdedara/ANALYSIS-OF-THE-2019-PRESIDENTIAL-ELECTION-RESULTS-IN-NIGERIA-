## ANALYSIS-OF-THE-2019-PRESIDENTIAL-ELECTION-RESULTS-IN-NIGERIA-

---

### PROJECT OVERVIEW

---

This project aims to analyze and visualize the 2019 Presidential Election results in Nigeria. The goal is to provide insights into the election process, including voter participation, party performance, and regional distribution of votes. By examining the results in-depth, we hope to draw conclusions on the electoral trends and patterns in Nigeria.  

---

### DATA SOURCES 

---

The primary data source for this project is the [Nigerian Election Results (1999-2019)](https://www.kaggle.com/datasets/xibilolu/nigerian-election-results-19992019) dataset available on Kaggle. The dataset includes comprehensive election results data from 1999 to 2019, including:

- Voter registration figures
- Voter accreditation details
- Election results per state and party
- Election-winning party per state

The data was downloaded from Kaggle and cleaned to provide relevant metrics for the analysis of the 2019 Presidential Election.

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

For this project, we focused solely on the 2019 Nigerian Presidential Election results from the dataset found on Kaggle: [Nigerian Election Results 1999-2019](https://www.kaggle.com/datasets/xibilolu/nigerian-election-results-19992019). Below is the step-by-step breakdown of the analysis process.

---

#### 1. **Data Collection**

   - I downloaded the 2019 election data from the Kaggle dataset.
    The data included the following columns:

     - States
    
     - APC
       
     - PDP
       
     - PCP
       
     - ADC
       
     - APGA
       
     - Other Parties
       
     - Registered Votes
       
     - Accredited Votes
       
     - Winner

---

#### 2. **Data Cleaning and Preprocessing**

   - **Filtering for 2019**: We filtered the dataset to include only the 2019 election results.
   - **Handling Missing Data**: Any missing values in key columns (such as registered votes or accredited votes) were either filled or removed.
   - **Data Formatting**: The dataset was checked for inconsistencies in data types, ensuring that numerical values were correctly formatted (e.g., total votes, percentages).

#### 3. **Data Loading into Power BI**
   - We imported the cleaned 2019 data into Power BI.
   - Using **Power Query**, we created additional calculated columns for specific metrics:
     - **Voter Turnout Percentage** per state: `(Accredited Votes / Registered Votes) * 100`
     - **Total Votes** per party per state
     - **Winning Party** for each state
     - **Percentages** for APC, PDP, and other parties across each state.

#### 4. **Data Transformation**
   - **Aggregation**: We aggregated the data to compute totals for votes, winning party per state, and overall national statistics.
   - **Calculated Metrics**: We created new measures to visualize the following:
     - **Voter Turnout** per state
     - **Total Votes** for each party
     - **Percentage of Votes** per party across states

#### 5. **Data Visualization**
   - **Power BI Visuals**: Using Power BI's native visualizations, we created the following:
     - **Total Registered Votes**: A bar chart showing the total number of registered voters by state.
     - **Total Accredited Votes**: A bar chart showing the total number of accredited voters per state.
     - **States Won by APC**: A map visual showing the states won by the APC.
     - **States Won by PDP**: A map visual showing the states won by the PDP.
     - **Election Winning Party**: A pie chart showing the winning party in the election.
     - **Total Votes by Party Across States**: A stacked bar chart displaying the total votes each party received across the states.
     - **States' Total Votes and Their Winners**: A table displaying each state, total votes cast, and the winning party.
     - **Voter Turnout Percentage by States**: A bar chart showing voter turnout percentages per state.
     - **Registered Votes by States**: A map visual showing the number of registered voters in each state.

#### 6. **Analysis and Insights**
   - The analysis focused on understanding voter turnout, party performance by region, and identifying trends in the 2019 election results.
   - Insights drawn from the visualizations include:
     - **Regional Trends**: The APC dominated in the northern and western regions, while PDP was stronger in the southeastern states.
     - **Voter Turnout**: States in the southern region had higher voter turnout compared to the northern regions.
     - **Party Performance**: A comparison of party votes by state showed how each party performed across Nigeria.

#### 7. **Reporting**
   - Generated detailed reports summarizing the election results, with insights on party dominance, voter engagement, and turnout.
   - Insights were presented using Power BI's built-in dashboard capabilities.
