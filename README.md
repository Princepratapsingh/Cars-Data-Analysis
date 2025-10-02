Project Overview
This project provides a comprehensive data analysis of a car dataset, focusing on key performance indicators (KPIs) like sales volume, pricing strategy, customer satisfaction (ratings), and safety standards. The goal was to transform raw, messy data into actionable insights to understand the competitive landscape of the automotive market.

🛠️ Tools and Technologies
Python: The core programming language used for data manipulation and analysis.

Pandas: Essential library for data cleaning, transformation, and manipulation.

NumPy: Used for numerical operations and handling missing values.

Matplotlib: Used for generating data visualizations (plots and charts).

Jupyter Notebook: The primary environment for executing the code and documenting the analysis process (Cars Dataset.ipynb).

💾 Dataset Details
The dataset (all_cars_datset_final.csv) contains records for various car models across different brands, including:

Column	Description
Brand	Manufacturer of the car.
Car Name	Specific model name.
Price	Car price (in Lakhs/Crores, converted to Lakhs for uniformity).
Rating	Customer rating out of 5.
Safety	Safety rating (e.g., Star Safety, converted to Star number).
Mileage	Fuel efficiency (converted to Average kmpl).
Power (BHP)	Engine power (converted to Average BHP).
FY2024(sales)	Total sales volume for the fiscal year 2024.

Export to Sheets
✅ Data Cleaning & Preprocessing Steps
The raw data required significant cleaning to convert text-based, range, and currency-formatted fields into uniform numerical data.

Price Normalization: Converted prices from 'Lakhs' and 'Crores' to a single unit: Lakhs. Missing prices were imputed using the median.

Range Conversion: For Mileage and Power (BHP), the average of the range (e.g., '17-25 kmpl' -> 21 kmpl) was calculated. Missing values were imputed using the mean.

Rating Extraction: Removed the '/5' suffix and imputed missing values using the mean rating.

Safety Quantification: Extracted the numerical star rating (e.g., '4 Star Safety' -> 4). Missing safety ratings were assigned 0 stars.

Sales Standardization: Removed commas and quotes from the FY2024(sales) column and treated any missing sales data as 0.

📊 Key Analytical Insights
The analysis yielded two major insights, visualized through charts:

1. Market Leadership: Top 10 Brands by Sales 🏆
Insight: Clearly identified Maruti Suzuki as the undisputed market leader by sales volume, followed by Hyundai, Mahindra, and Tata.


2. Safety Standards: Top 10 Safest Cars 🛡️
Insight: Sorted cars by their 5-Star Safety Rating, highlighting models where Indian manufacturers Tata and Mahindra show strong dominance, demonstrating significant improvement in safety standards across their popular models.

Output File: top_10_safest_cars.csv contains the list of these models.

✍️ How to Run the Code
Clone this repository

Install required libraries: pip install pandas numpy matplotlib

Open the notebook: jupyter notebook "Cars Dataset.ipynb"

Run all cells to replicate the cleaning process and generate the plots.

