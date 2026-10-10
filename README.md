# Laptop Price Analysis Project

I did this project as a Data Analyst for an electronics shop. Main column is Price.
Tools used: Python, Pandas, NumPy, Matplotlib, Seaborn, SciPy.

## Files in this folder
- Sprint_1_Data_Cleaning.ipynb - cleaning work, makes Laptop_price_cleaned_final.csv
- Sprint_2_EDA_Visualization.ipynb - graphs and group study
- Sprint_3_Statistics_FeatureEngineering.ipynb - tests and new columns, makes Laptop_price_featured_final.csv
- Laptop_price_cleaned_final.csv - clean data, 994 rows and 7 columns
- Laptop_price_featured_final.csv - clean data + new groups, 994 rows and 13 columns
- visuals - all graph images
- Raw file is ../Laptop_for_messy.csv. I did not change it, only cleaned by code.

## What I did in short
1. Raw data had 1020 rows. 20 rows were duplicate, so I removed them. 1000 rows left.
2. Each column had about 24 missing values. I filled numbers with median and Brand with mode.
3. IQR rule gave 6 wrong rows (like 160 RAM, 5000 storage, 167519 price). I removed them. Final 994 rows.
4. Price mean 19490, median 17272, min 8570, max 33503.
5. Storage decides price most (correlation 0.97). 256GB = 9879, 512GB = 17493, 1TB = 31601.
6. RAM effect is small. Processor, Screen, Weight, Brand alone do not change price much.
7. Brands: Dell 214, Asus 203, Acer 202, HP 188, Lenovo 187. Lenovo average highest 19994, Dell lowest 18767.
8. Tests: RAM 4GB vs 32GB test is significant (p = 0.0076). Brand test is not significant (p = 0.678). Brand and price group test is not significant (p = 0.457).
9. New columns: Price groups Budget / Mid-Range / Premium (328 / 328 / 338), RAM groups, Storage groups, Weight groups, Performance groups (Low 11991, Mid 20849, High 25654).

## How to run
Install packages first:
pip install pandas numpy matplotlib seaborn scipy
Then open notebooks one by one in Jupyter and run all cells from top to bottom.
Start with Sprint 1, then Sprint 2, then Sprint 3.
