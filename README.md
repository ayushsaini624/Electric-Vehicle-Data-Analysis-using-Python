# Electric Vehicle Data Analysis 🚗⚡️

## 📌 Project Overview
This project performs an in-depth analysis of an Electric Vehicle (EV) dataset using Python. The goal is to explore various attributes of electric cars, uncover meaningful patterns, visualize key relationships, and conduct a statistical hypothesis test to compare leading manufacturers. The analysis provides actionable insights for consumers, manufacturers, and industry analysts.

The project was developed as part of my **Internshala Python Training**.

---

## 📂 Dataset
- **Source**: `FEV-data-Excel.xlsx`
- **Details**:
  - Contains comprehensive specifications for various electric vehicle models.
  - Key features include: `Make`, `Model`, `Minimal price (gross) [PLN]`, `Engine power [KM]`, `Battery capacity [kWh]`, `Range (WLTP) [km]`, and `Drive type`.
  - The dataset provides a snapshot of the current EV market landscape.

---

## ⚙️ Data Cleaning and EDA
- Loaded the dataset using **Pandas** and performed initial data inspection.
- Checked for and handled missing values to ensure data quality.
- Conducted Exploratory Data Analysis (EDA) to understand the distribution of key numerical features like `Price`, `Range`, and `Engine Power` using histograms and box plots.

---

## 🧑‍💻 Feature Engineering
- Created new categorical features to better segment the data for analysis:
  - **Price_Category**: Grouped vehicles into price brackets (e.g., 'Low', 'Medium', 'High').
  - **Range_Category**: Classified vehicles based on their WLTP range to identify short, medium, and long-range models.

---

## 📊 Data Visualization & Insights
Several visualizations were created using **Matplotlib** and **Seaborn** to uncover trends:
- **Top 10 EV Manufacturers**: A bar chart identified the brands with the most vehicle models on the market.
- **Drive Type Distribution**: A pie chart showed the prevalence of different drive types (AWD, 2WD).
- **Price vs. Range Analysis**: A scatter plot revealed the relationship between a vehicle's price and its driving range.
- **Battery Capacity vs. Range**: A scatter plot demonstrated the strong positive correlation between battery size and achievable range.
- **Correlation Heatmap**: A heatmap was generated to visualize the correlation between all numerical attributes, highlighting key relationships.



---

## 🔬 Hypothesis Testing
A statistical test was conducted to compare the performance of two major EV manufacturers.
- **Question**: Is there a statistically significant difference in the average engine power between vehicles made by **Tesla** and **Audi**?
- **Test Used**: Two-sample independent t-test (`ttest_ind` from the `scipy.stats` module).
- **Hypotheses**:
  - **Null Hypothesis (H₀)**: The mean engine power of Tesla vehicles is equal to the mean engine power of Audi vehicles.
  - **Alternative Hypothesis (H₁)**: The mean engine powers are not equal.

---

## 🏆 Key Findings & Conclusion
- **Result**: The t-test yielded a **p-value of 0.1167**, which is greater than the significance level of 0.05.
- **Conclusion**: We **fail to reject the null hypothesis**. The analysis shows that there is **no statistically significant difference** in the average engine power between Tesla and Audi models in this dataset. The observed variations are likely due to chance.
- **General Insights**: The analysis confirms that `Battery capacity` is a primary driver of `Range`. While premium brands dominate the high-price segments, there is a growing diversity in models across different price points.

---

## 🔧 Tools & Libraries Used
- **Python**
- **Pandas**: For data manipulation and analysis.
- **NumPy**: For numerical operations.
- **Matplotlib**: For creating static and animated visualizations.
- **Seaborn**: For high-level statistical data visualization.
- **SciPy**: For scientific and statistical computing (specifically for the t-test).
