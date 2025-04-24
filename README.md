# 🎯 Kickstarter Data Analysis – First Excel Project

![gifexcel1](https://github.com/user-attachments/assets/a6afa697-e3b6-4abc-bfb2-b4a0aa594bdc)


### Introduction
This is my very first data analysis project using **Microsoft Excel**.  
I worked with a real-world dataset from **Kickstarter** to explore various aspects of crowdfunding campaigns – including:

- Success rates by category and country  
- Relationships between funding goals and outcomes  
- Time-based trends in campaign launches and performance  

This also marks the beginning of my data analysis portfolio and a documented step in my learning journey :)

### Excel Skills Used
- **📊 Pivot Tables**
- **📈 Pivot Charts**
- **🧮 DAX (Data Analysis Expressions)**
- **🔍 Power Query**
- **💪 Power Pivot**

## 📁 Dataset

The dataset comes from [Kickstarter Projects](https://www.kaggle.com/datasets/kemical/kickstarter-projects), originally published on Kaggle.  
It contains over **370,000** Kickstarter campaigns with details such as:

- Project name, category, and country
- Funding goal and amount pledged
- Launch and deadline dates
- Project status (successful, failed, canceled, etc.)
- Currency used

### 🔄 Data Cleaning & Transformation (Power Query)

As part of the ETL (Extract, Transform, Load) process in **Power Query**, I performed several cleaning and transformation steps to prepare the dataset for analysis:

- **Removed unnecessary columns** that were not relevant to the analysis (e.g. currency, ID).
- **Standardized currencies** by converting all amounts to the same currency (USD).
- **Filtered out rare categories** by removing any category with fewer than 100 projects, to focus on meaningful trends.

![Zrzut ekranu 2025-04-24 o 20 33 55](https://github.com/user-attachments/assets/dc050dd6-178f-4e0a-9890-97d0a99cdd75)

- **Added external data** by importing a country ISO table from Wikipedia.
    - Cleaned the imported data.
    - Merged it with the main dataset to expand country names.

![wikiskrin](https://github.com/user-attachments/assets/715b0a89-3540-49c5-91dc-7743f3389cd3)

These steps helped simplify the dataset, reduce noise, and improve the quality of the analysis.

## 🔍 Analysis

The analysis focused on four key areas to better understand patterns in Kickstarter campaigns:

1. **Overall Success** – General success rates and campaign outcomes  
2. **Geography** – Performance by country  
3. **Time** – Launch trends and seasonality  
4. **Finance** – Goals, pledges, and overfunding  

### ✅ Overall Success

In this part of the analysis, I explored general trends in Kickstarter campaign outcomes using **Power Pivot** and **DAX formulas**.

I focused on answering the following questions:

- What percentage of Kickstarter projects are successful?
- Which categories have the highest success rates?
- What is the average funding goal in each category?

I built interactive pivot tables to quickly compare campaign performance across categories.

![Zrzut ekranu 2025-04-24 o 20 53 32](https://github.com/user-attachments/assets/a1c2117e-a7d3-4fef-acfe-4a73a57f80c1)


Using DAX, I calculated success rate  and goal averages

![Zrzut ekranu 2025-04-24 o 20 56 52](https://github.com/user-attachments/assets/c7e26841-6b56-49b8-9d66-16c5e0b1720b)
![Zrzut ekranu 2025-04-24 o 20 57 11](https://github.com/user-attachments/assets/b254887f-b0a9-4e79-ab79-7d78580b37c2)


🟰 Summary:
- The overall success rate of Kickstarter campaigns is **36%**.
- **Dance** (63%), **Theater** (60%), and **Comics** (54%) are the most successful categories.
- Categories like **Technology** (20%) and **Journalism** (22%) have the lowest success rates.
- The average funding goal across all categories is **$45,092**.
- **Technology** projects have the highest average goal (**$102,059**), while **Dance** has the lowest (**$9,409**).

### ✅ Geography

In this part of the analysis, I examined how location influences the success of Kickstarter campaigns using **Power Pivot**

I focused on answering two key questions:

- Which countries launch the most crowdfunding campaigns?
- What are the success rates of campaigns by country?


![Zrzut ekranu 2025-04-24 o 21 13 55](https://github.com/user-attachments/assets/899cfbab-b08a-4b91-964f-53ca2ef4cffc)     ![Zrzut ekranu 2025-04-24 o 21 14 11](https://github.com/user-attachments/assets/75655daa-f546-40a4-86c3-8a6799cd3a64)













