# 📘 GDP per Capita Analysis Using Pandas, Matplotlib and Seaborn

## 📂 Project Overview

This project analyses a dataset containing **GDP (nominal) per capita** by country using Python libraries such as **Pandas**, **Matplotlib**, and **Seaborn**. It covers importing, cleaning, exploring, and visualising data to derive meaningful insights.


![Screenshot (479)](https://github.com/user-attachments/assets/36110124-42bc-4b0d-bb5b-01d4b74f6a91)

---

## 📌 Key Concepts Covered

- Reading and cleaning CSV data
- Handling encoding issues (`unicode_escape`)
- Setting index columns properly
- Exploring the dataset with summary statistics
- Creating plots using:
  - `matplotlib.pyplot`
  - `seaborn`

---

## 📊 Dataset Information

- **File Name**: `GDP (nominal) per Capita.csv`
- **Encoding**: `unicode_escape`
- **Index Column**: Country names (first column)
- **Note**: Data may vary due to exchange rates and does not reflect purchasing power parity (PPP).

### ⚠️ Important Considerations

The figures do **not** adjust for:
- Differences in cost of living across countries
- Fluctuations in currency exchange rates
- PPP (Purchasing Power Parity) — more reliable for income comparisons

---

## 🔧 Getting Started

To use the dataset in your own environment:

```python
import pandas as pd

# Upload or load the dataset
df = pd.read_csv("GDP (nominal) per Capita.csv", encoding='unicode_escape', index_col=0)
```

You can then begin exploring the data using:

```python
df.head()
df.describe()
df.info()
```


![Screenshot (480)](https://github.com/user-attachments/assets/da41e7b5-a719-4154-8b34-0cb60ba1270b)
![Screenshot (482)](https://github.com/user-attachments/assets/1a1f81bd-a8b9-4a41-9b78-45a772499525)
![Screenshot (481)](https://github.com/user-attachments/assets/5a6ed285-e143-46cd-a79e-355aea06ee45)

---

## 📈 Visualisation Examples

The project includes visualisations such as:

- Bar plots of countries with highest/lowest GDP per capita
- Line plots showing GDP trends
- Heatmaps for correlation analysis
- Seaborn scatter plots for regional comparison

```python
import matplotlib.pyplot as plt
import seaborn as sns

plt.figure(figsize=(10,5))
sns.barplot(data=df.sort_values('2022', ascending=False).head(10), x=df.index, y='2022')
plt.xticks(rotation=45)
plt.title('Top 10 Countries by GDP per Capita (2022)')
plt.show()
```

![Screenshot (486)](https://github.com/user-attachments/assets/5f3265a6-8398-4e3e-a4d8-03d6fc35af0d)
![Screenshot (485)](https://github.com/user-attachments/assets/49c3d730-4a61-4a64-b868-b0016c636474)
![Screenshot (484)](https://github.com/user-attachments/assets/d929fd69-d12a-47e7-8bfc-70a86698f0f8)

---

## 🧠 Summary

This notebook is a hands-on practice project for:

- Strengthening skills in **data analysis with Pandas**
- Applying **data visualisation** techniques using Matplotlib and Seaborn
- Working with real-world financial and demographic data

---

## ✅ Requirements

- Python 3.x
- Pandas
- Matplotlib
- Seaborn
- (Optional) Google Colab or Jupyter Notebook

---

> Created 🔥 by **Bafti Çakır**
