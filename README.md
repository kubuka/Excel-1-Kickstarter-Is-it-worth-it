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

![Zrzut ekranu 2025-04-25 o 18 56 10](https://github.com/user-attachments/assets/e17f59b9-d466-48d3-92c7-3f8604327e1e)

🟰 Summary:
- The **United States** is by far the most active country, with **289,671** campaigns and a success rate of **38%**.
- Other active countries include the **United Kingdom** (**33,215 campaigns**, 36%) and **Canada** (**14,508 campaigns**, 28%).
- The highest success rates are seen in **Hong Kong** (38%) and the **USA** (38%), while **Italy** (16%) and **Austria** (19%) have the lowest.

This analysis shows a strong presence of English-speaking countries on Kickstarter, and highlights significant differences in success rates depending on the region, possibly influenced by cultural, economic, or market factors.

### ✅ Time

In this section, I analyzed how the timing of campaign launches affects their number and success, using **Power Pivot** and **DAX**.

To answer the questions, I created a separate **Calendar table** and established a **one-to-many relationship** with the main dataset.

  ![Zrzut ekranu 2025-04-25 o 19 11 12](https://github.com/user-attachments/assets/1cc2e8d7-cf73-45dc-89f7-2fd9cabb8242)

Additionally, I used DAX to create a custom column that assigned each campaign to a specific season based on its launch date.


Key questions explored:

- Has the number of Kickstarter projects increased over time?
- Which months are the most popular for launching campaigns?
- Does the season affect the success rate?

![Zrzut ekranu 2025-04-25 o 19 14 53](https://github.com/user-attachments/assets/60008c73-b1fe-4e8f-a821-51c858ddea2c) ![Zrzut ekranu 2025-04-25 o 19 15 01](https://github.com/user-attachments/assets/5af8e6d1-ff8b-4e12-9335-c6baf1026bca) ![Zrzut ekranu 2025-04-25 o 19 15 14](https://github.com/user-attachments/assets/c32c86b7-1428-45ac-8eda-948d18d0c4bc)


#### 🟰 Summary – Time

- The number of campaigns grew rapidly between **2009 and 2015**, peaking at **74,438** campaigns in **2015**.
- After 2015, there was a noticeable decline in new campaign launches each year.
- **August**, **July**, and **May** are the most popular months for starting a campaign, each with over **33,000** launches.
- **Spring** campaigns have the highest success rate at **38%**, slightly better than other seasons (Summer 35%, Autumn 36%, Winter 35%).

This analysis suggests that both the time of year and overall platform trends influence the volume and success of crowdfunding projects.

### ✅ Finance

In this section, I explored the financial performance of Kickstarter campaigns using **Power Pivot** and **DAX**.

To answer the questions, I created custom measures to calculate both the **average** and **median** pledged amounts, as well as a new column to flag campaigns that **exceeded their funding goal**. I then used `CALCULATE` and `COUNT` functions to determine how often goals were surpassed.

Key questions explored:

- Which projects raised the most money?
- What is the difference between the average and median amount pledged?
- In which categories do campaigns most frequently exceed their funding goals?

![Zrzut ekranu 2025-04-25 o 19 24 02](https://github.com/user-attachments/assets/053768f7-acf2-4390-b3df-5e6b944a55a2)

![Zrzut ekranu 2025-04-25 o 19 24 20](https://github.com/user-attachments/assets/f48672f3-500d-42d5-a12f-133585efddc8) 

![Zrzut ekranu 2025-04-25 o 19 24 40](https://github.com/user-attachments/assets/26790156-12d5-4e21-956e-2d916c6ac08b)


#### 🟰 Summary – Finance

- The top-funded projects include:
  - **Pebble Time - Awesome Smartwatch** ($20.3M)
  - **COOLEST COOLER** ($13.3M)
  - **Pebble 2, Time 2 + Pebble Core** ($12.8M)
- The **average** amount pledged across all projects is **$9,144**, while the **median** is significantly lower at **$632**, showing a large disparity caused by a few exceptionally high-funded campaigns.
- The difference between the average and median amounts is **$8,512**, highlighting the skewness of the data.
- The categories with the most campaigns exceeding their funding goals are:
  - **Music** (23,274 successful campaigns)
  - **Film & Video** (22,641 successful campaigns)
  - **Games** (12,567 successful campaigns)

This analysis shows that while a few campaigns raise extremely high amounts, the majority of projects gather more modest funding. It also emphasizes that some categories are much more successful in surpassing their targets than others.

## 📊 Final Dashboard & Summary

After completing the analysis across five key dimensions — **overall success**, **geography**, **time** and **finance** — I summarized the most important insights and visualized them in a dynamic and interactive **Excel dashboard**.

The dashboard allows users to **filter the data by country**, enabling a more targeted analysis based on regional interest.

#### ✨ Dashboard Features

**Static visuals** (always visible):
- 📈 Number of campaigns per year (2009–2018)
- 🥇 Top countries by success rate
- 🗂 Distribution of all campaigns across categories

**Dynamic visuals** (change based on selected country):
- ✅ Average success rate for the selected country
- 📊 Category breakdown: number of campaigns per category + their individual success rates
- 🏆 Table of top campaigns by funds raised
  
![Zrzut ekranu 2025-04-25 o 19 34 52](https://github.com/user-attachments/assets/fd0aa4cd-46dc-42b5-bfc3-96919ce25a98)


This final dashboard brings together key insights from the ETL process and DAX-driven analysis, offering a clear, engaging, and interactive overview of Kickstarter’s historical campaign data.












