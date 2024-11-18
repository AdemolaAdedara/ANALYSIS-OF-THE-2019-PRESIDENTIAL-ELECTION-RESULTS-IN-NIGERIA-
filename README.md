## ANALYSIS OF THE 2019 PRESIDENTIAL ELECTION RESULTS IN NIGERIA

---

### TABLE OF CONTENTS

---

 - [PROJECT OVERVIEW](#project-overview)

 - [DATA SOURCE](#data-source)

 - [INSTALLATIONS](#installations)

 - [TOOLS USED](#tools-used)

 - [ANALYSIS PROCESS](#analysis-process)

 - [VISUALIZATION ](#visualization)

 - [RESULTS AND INSIGHTS](#results-and-insights)

 - [RECOMMENDATIONS ](#recommendations)

---

### PROJECT OVERVIEW

---

This project aims to analyze and visualize the 2019 Presidential Election results in Nigeria. The goal is to provide insights into the election process, including voter participation, party performance, and regional distribution of votes. By examining the results in-depth, I hope to draw conclusions on the electoral trends and patterns in Nigeria.  

---

### DATA SOURCE

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

   - From the Kaggle dataset, I downloaded "2019pres" data [Nigerian Election Results (1999-2019)](https://www.kaggle.com/datasets/xibilolu/nigerian-election-results-19992019?select=2019pres.csv).
     
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
     
   - Using **Power Query**, I created an additional calculated column for a specific metric:
     
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

---

This Power BI report includes the following visuals:

<img width="595" alt="power bi project 1" src="https://github.com/user-attachments/assets/e4d6cb5e-74e4-42ce-9e90-e9ec40504d03"> 

<img width="604" alt="power bi project 2" src="https://github.com/user-attachments/assets/ac05d8c3-65ed-4482-920c-0b081900abfc">

<img width="479" alt="power bi project 3" src="https://github.com/user-attachments/assets/48c23946-774d-4c37-8b2e-fe4c71ec529a">

---

### RESULTS AND INSIGHTS

---

Based on my Power BI analysis of the 2019 Nigerian Presidential Election results, I derived the following key insights from the visuals created.

#### 1. **Total Registered Voters**

   - The total number of registered voters varied significantly by state, with the highest numbers in regions such as Lagos and Kano.
   - States with larger populations generally had a higher number of registered voters, reflecting population distribution trends across Nigeria.

---

#### 2. **Total Accredited Votes**

   - Not all registered voters were accredited to vote; there was a noticeable drop between registered voters and accredited voters in many states.
   - States in the North Central and South West regions showed relatively higher accreditation rates, indicating active voter participation in those areas.

---

#### 3. **States Won by APC and PDP**

   - **APC** (All Progressives Congress) won in states predominantly located in the northern and southwestern regions, showing strong support in these areas.
     
   - **PDP** (Peoples Democratic Party) had more success in the southeastern states, displaying a regional divide in party preferences.
     
   - This geographic division in party dominance reflects historical political trends and regional support bases for each party.

---

#### 4. **Election Winning Party**

   - The overall winner of the 2019 Presidential Election was **APC**, based on a majority of states supporting the party.
     
   - This result aligns with the trend of APC dominance in populous regions, which likely contributed significantly to their national vote tally.

---

#### 5. **Total Votes of Each Party Across States**

   - APC and PDP were the dominant parties across all states, with APC generally receiving higher vote counts in northern and western states.
     
   - Other smaller parties, including PCP, ADC, and APGA, had limited impact and only received significant votes in specific regions, underscoring the two-party dominance in Nigerian politics.

---

#### 6. **States’ Total Votes and Their Winners**

   - In states where voter turnout was high, APC and PDP had close competition, especially in battleground states such as Osun and Ekiti.

   - In some states, the winning party had a significant margin over others, highlighting strong regional loyalties and predictable voting patterns in those areas.

---

#### 7. **Voter Turnout Percentage by States**

   - Voter turnout varied widely across states, with some southern states achieving higher turnout rates than northern ones.
     
   - States with higher urban populations, such as Lagos and Rivers, recorded lower turnout percentages, potentially due to logistical challenges and voter apathy.
     
   - Northern states had varied turnout rates, with some rural areas showing strong turnout, suggesting different levels of voter mobilization across regions.

---

#### 8. **Registered Votes by States**

   - States with high registered voter counts did not always translate to high voter turnout or party dominance.
     
   - Kano and Lagos, which had the highest registered voters, showed contrasting results in voter turnout and party support, indicating that large voter bases do not always reflect the final outcomes.
     
   - This suggests opportunities for future voter engagement initiatives, especially in high-population states with low turnout.

---

#### **Overall Insights**

   - The 2019 Nigerian Presidential Election results highlight clear regional divides in party dominance, with APC and PDP having distinct areas of support.
     
   - Voter turnout remains a critical factor influencing electoral outcomes. States with high turnout often influenced the winning party, while low-turnout regions showed weaker engagement.
     
   - Understanding voter behavior by region provides insights for political parties in strategizing future campaigns, focusing on states with high registered voters but historically low turnout.

These insights offer a comprehensive overview of the political landscape in Nigeria as of 2019, showing regional preferences, voter engagement, and party dominance patterns that could shape future elections.

---

### RECOMMENDATIONS

Based on the analysis of the 2019 Nigerian Presidential Election results, here are several recommendations to improve future electoral processes, enhance voter participation, and strengthen democratic engagement:

#### 1. **Increase Voter Turnout through Education and Awareness Campaigns**

   - States with low voter turnout, particularly in the northern regions, may benefit from targeted awareness and education campaigns that emphasize the importance of civic participation.
     
   - Engaging local influencers, traditional leaders, and community organizations could help address barriers to voting and improve turnout rates in future elections.

---

#### 2. **Implement Robust Voter Registration Processes**

   - Analysis showed disparities between registered and accredited voters across states. Improving the voter registration process can help ensure accurate records, minimize discrepancies, and provide a clearer reflection of eligible voters.
     
   - Regular updates and verification of voter rolls, especially in densely populated or rural areas, could reduce the gap between registered and accredited voters.

---

#### 3. **Enhance Electoral Transparency and Accessibility**

   - Transparency measures, such as real-time reporting of election results at each stage, could build trust in the electoral process.
     
   - Providing accessible polling stations, particularly in remote areas, and ensuring accommodations for persons with disabilities could increase voter participation.

---

#### 4. **Focus on Equitable Resource Allocation for All Political Parties**

   - The data showed concentrated dominance of APC and PDP in various regions. Equitable access to campaign resources for all parties would foster a more inclusive electoral environment, where smaller parties can compete fairly.
     
   - Encouraging equal media coverage, funding support, and platform access can help diversify political representation and choice.

---

#### 5. **Address Regional Disparities in Voter Turnout**

   - The analysis highlighted regional differences in voter engagement. Policymakers and election officials should investigate the causes of these disparities and work to address region-specific challenges.
     
   - Initiatives like improved security measures in conflict-prone areas and enhancing voter education in underrepresented regions could foster broader electoral participation.

---

#### 6. **Leverage Data Analytics for Future Election Planning**

   - Continuing to collect, analyze, and publicly share election data can improve planning for future elections by highlighting areas in need of support or reform.
     
   - Data analytics can provide insights into voter behavior, enabling targeted interventions to address low participation and improve electoral efficiency.

---

#### 7. **Encourage Youth and First-Time Voters**

   - Programs targeting youth engagement and first-time voters can invigorate the democratic process, as these groups often have lower turnout rates.
     
   - Partnering with schools, universities, and youth-focused organizations can help foster a culture of early and continued civic participation.

---

By implementing these recommendations, Nigeria can work towards more transparent, fair, and inclusive elections, enhancing democratic representation and ensuring that every citizen’s voice is heard.

