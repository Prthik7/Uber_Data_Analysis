# Uber_Data_Analysis
Here is a professional **README.md** file based on your Uber data analysis project. It includes problem statements from the image, code analysis from the PDF, and insights generated from the dataset (`UberDataset.csv`):

---

# 🚗 Uber Data Analysis Project

## 📊 Project Overview

This project focuses on analyzing Uber ride data to extract meaningful insights into user behavior. By processing and visualizing the data, we answer key business questions that can help Uber improve user experience, plan services, and optimize performance.

---

## 📝 Dataset Description

The dataset `UberDataset.csv` contains 1,156 rows and the following columns:

| Column Name | Description                               |
| ----------- | ----------------------------------------- |
| START\_DATE | Date and time when the ride started       |
| END\_DATE   | Date and time when the ride ended         |
| CATEGORY    | Type of ride (Business or Personal)       |
| START       | Starting location                         |
| STOP        | Ending location                           |
| MILES       | Distance of the trip in miles             |
| PURPOSE     | Purpose of the trip (Meeting, Meal, etc.) |

---

## ❓ Business Questions Answered

1. **In which category do people book the most Uber rides?**

   * **Answer**: `Business` rides are booked more frequently than personal rides.
   * 📊 Visualized using: `sns.countplot(dataset['CATEGORY'])`

2. **For which purpose do people book Uber rides the most?**

   * **Answer**: `Meeting` is the most common purpose, followed by `Errand/Supplies` and `Meal/Entertainment`.
   * 📊 Visualized using: `sns.countplot(dataset['PURPOSE'])`

3. **At what time do people book cabs the most from Uber?**

   * **Answer**: Rides peak during `evening` hours (15:00–19:00).
   * 📊 Time categorized using `pd.cut()` on hour extracted from `START_DATE`.

4. **In which months do people book Uber rides less frequently?**

   * **Answer**: The months with the least rides are generally `June` and `July`.
   * 📊 Visualized using: `sns.lineplot()` on monthly counts.

5. **On which days of the week do people book Uber rides the most?**

   * **Answer**: `Friday` and `Monday` have the highest booking frequencies.
   * 📊 Visualized using: `sns.barplot(x=day_label.index, y=day_label)`

6. **How many miles do people usually book a cab for through Uber?**

   * **Answer**: Most rides are under `20 miles`. Boxplots show outliers above `40 miles`.
   * 📊 Visualized using: `sns.boxplot()` and `sns.distplot()` (miles < 40)

---

## 🧹 Data Preprocessing

* Missing values in `PURPOSE` filled with `"NOT"`.
* Removed rows with any null values (`dropna()`).
* Converted `START_DATE` and `END_DATE` to datetime.
* Extracted `hour`, `day`, `month`, and created labels like `day-night`, `DAY`, and `MONTH`.

---

## 📁 Files Included

* `UberDataset.csv` — The source dataset.
* `Screenshot_Uber_Data_analysis_project.pdf` — Contains code screenshots.
* `README.md` — Documentation of the project (you’re reading it!).

---

## 🔧 Tools & Libraries Used

* Python (Pandas, NumPy)
* Data Visualization: Matplotlib, Seaborn
* Jupyter Notebook or any Python IDE

---

## 📈 Sample Visuals

* Bar charts for ride categories and purposes
* Line plots for monthly trends
* Boxplots and distribution plots for ride distance
* Day-wise ride frequency bar charts

---

## 📌 Conclusion

This analysis helps Uber understand:

* User behavior by time, day, and month.
* Distance trends to optimize pricing.
* Popular purposes and categories for targeted service development.


