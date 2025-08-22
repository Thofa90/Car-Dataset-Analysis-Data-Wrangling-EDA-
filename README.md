# 🚗 Car Dataset Analysis (Data Wrangling & EDA)

# 📌 Project Overview

This project focuses on data wrangling and exploratory data analysis (EDA) using a car dataset containing vehicle specifications, performance, and pricing information.
The aim is to clean, transform, and explore the dataset to extract business insights into car pricing, popularity, and fuel efficiency trends.

⸻

# 🎯 Goals
	•	Perform data cleaning and wrangling to prepare the dataset for analysis.
	•	Conduct feature engineering to derive new business-relevant metrics.
	•	Carry out exploratory data analysis (EDA) with descriptive stats, visualizations, and correlation analysis.
	•	Summarize patterns and insights useful for automotive industry decisions.

# 🛠️ Steps of Analysis

**Importing Packages**

All required Python libraries were imported for data loading, numerical operations, data manipulation, data analysis, and visualization.

Data Loading

	•	Loaded the dataset into a Pandas DataFrame.
	•	Performed initial inspection (.head(), .info(), .describe()).

Understanding the Dataset

	•	Checked dataset dimensions, column descriptions, and datatypes.
	•	Identified potential issues like missing values, inconsistent formatting, and outliers.

 # 🔹 Project Tasks

**Task 1: Cleaning the Dataset**

1.1 Handle Missing Data → Filled or dropped missing values appropriately.
1.2 Data Type Conversion → Converted columns to suitable data types.
1.3 Filtering Data → Kept only cars from 1995 onwards.
1.4 String Operations → Standardized text (lowercase for categorical fields).

⸻

**Task 2: Feature Engineering**

	•	Created Total MPG = (city mpg + highway MPG) / 2
	•	Created Price per HP = MSRP / Engine HP
	•	Saved the cleaned dataset as CSV for future use.

⸻

**Task 3: Exploratory Data Analysis (EDA)**

**🔹 Descriptive Statistics**

	•	The average Engine HP is ~259, with most cars around 241 HP → slightly right-skewed distribution.
	•	The average MSRP is ~$44,162, but with high variance, indicating a wide range of prices (from affordable compact cars to luxury/performance vehicles).
	•	Fuel efficiency is balanced:
	•	Highway MPG → 26.75
	•	City MPG → 19.83
This reflects typical consumption patterns across categories.

**🔹 Group Analysis by Driven Wheels**

	1. All-Wheel Drive (AWD):
 
	•	Compact AWD cars range widely ($30K 4-cylinders → $1.7M 16-cylinders).
	•	Large AWD vehicles are expensive ($49K–$179K).
	•	4–6 cylinders dominate popularity, while high-cylinder models are niche luxury.
 
	2. Four-Wheel Drive (4WD):
 
	•	Compact 4WD → 8-cylinder engines most popular.
	•	Large 4WD → 6-cylinder more popular than 8-cylinder.
	•	Midsize 4WD → trend: more cylinders = higher price but lower popularity.
 
	3. Front-Wheel Drive (FWD):
 
	•	Compact FWD are most affordable.
	•	Popularity peaks at 0-cylinder (EVs/hybrids) & 4-cylinder cars.
	•	Large/midsize FWD → 6-cylinder most popular.
 
	4. Rear-Wheel Drive (RWD):
 
	•	Compact RWD spans 0–12 cylinders, with prices escalating quickly.
	•	Large RWD → 6-cylinder most popular, 12-cylinder least.
	•	Midsize RWD → 8-cylinder preferred (performance balance).

**🔹 Summary of Visualizations**

	•	Histogram (City MPG):
 
Most cars fall in 20–25 MPG, showing this as the typical urban fuel efficiency.

	•	Bar Chart (MSRP by Vehicle Size):
 
Large cars cost the most, midsize moderate, compact cheapest.

	•	Scatter Plot (Engine HP vs MSRP):
 
Strong positive correlation → higher horsepower = higher price.

	•	Box Plot (MSRP by Driven Wheels):
 
RWD & AWD → wider price variability & outliers.
FWD & 4WD → tighter ranges.

	•	Line Plot (MPG by Transmission Type):
 
Manual/automatic stable, while direct_drive (EVs) show extreme fuel efficiency (>100 MPG).

Summary in short :
	•	SUVs and larger vehicles show higher MSRP.
	•	Engine HP strongly correlates with price.
	•	Drivetrain type influences pricing and performance.

**🔹 Heatmap (Correlation Analysis)**

	•	Engine HP ↔ MSRP → strong positive correlation.
	•	Engine HP ↔ City/Highway MPG → strong negative correlation (powerful cars use more fuel).
	•	MSRP ↔ MPG → weak negative correlation.
	•	City MPG ↔ Highway MPG → strong positive correlation (cars efficient in one tend to be efficient in the other).
	•	Popularity → very weak correlations with all features.

**📌 Insight:** Pricing is mainly driven by Engine HP and Vehicle Size, while fuel efficiency is closely tied between city and highway use. Popularity is less dependent on technical specs, hinting at brand/market factors.

**✅ Key Takeaways from EDA**

	•	Horsepower is a primary driver of MSRP.
	•	Vehicle size & driven wheels strongly influence pricing and popularity.
	•	Fuel efficiency varies more by transmission type (EV vs non-EV) than size.
	•	High-cylinder cars are niche: expensive but less popular.
	•	Compact & midsize, lower-cylinder vehicles dominate the market (affordable + efficient).
	•	Correlation analysis confirms trade-off: More horsepower = higher cost but lower MPG.

⸻

📦 Libraries Used
	•	pandas, numpy → data wrangling
	•	matplotlib, seaborn → visualization
	•	scipy, statsmodels, sklearn → statistics, scaling, correlation
