# 📱 SOCIAL MEDIA USAGE ANALYSIS  
### By Bill Motor  

---

## 📌 Introduction  

In this digital age, social media has redefined human communication and interaction. Platforms such as Facebook, Instagram, Twitter, and TikTok have transformed how individuals and organizations engage, share content, and influence public opinion.  

This project analyzes patterns and trends in social media usage, focusing on demographics, platform behavior, engagement patterns, and addiction impacts.

---

## 🎯 Objectives  

- Analyze user behavior across demographics  
- Identify key usage patterns and trends  
- Understand factors influencing addiction levels  
- Evaluate the impact of social media on productivity  
- Generate actionable insights through visualization  

---

## 🧰 Tech Stack  

- Python  
- Pandas – Data manipulation  
- NumPy – Numerical computations  
- Matplotlib – Visualization  
- Seaborn – Statistical visualization  

---

## 📦 Installation  
```
pip install pandas numpy matplotlib seaborn
```
---

## 📊 Dataset  

- File: Time-Wasters on Social Media.csv  
- Size: 1000 rows × 31 columns  
- Key Features: User demographics, Behavioral metrics, Usage data, and Device/OS data.

---

## 💻 Implementation & Analysis
```
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
```
## 📥 Data Loading
```
df = pd.read_csv('Time-Wasters on Social Media.csv')
```

## 🔍 Data Exploration
```
print(df.info())
print(df.describe())
```
## 📈 Visualizations

### 1. Gender Distribution
```
sns.histplot(df['Gender'])
plt.title('Gender Distribution')
plt.show()
```
📌 Insight: Male users are more than female users

### 2. Demographics Distribution
```
sns.histplot(df['Demographics'])
plt.title('Demographics Distribution')
plt.show()
```
📌 Insight: Rural users dominate over urban users

### 3. Profession Usage
```
plt.figure(figsize=(10,5))
sns.histplot(df['Profession'])
plt.xticks(rotation=45)
plt.title('Profession Distribution')
plt.show()
```
📌 Insight: Students, waiting staff, and labor workers are the most active

### 4. Age Distribution
```
sns.histplot(df['Age'], kde=True)
plt.title('Age Distribution')
plt.show()
```
📌 Insight: Age distribution is fairly uniform

### 5. Watch Reason
```
plt.figure(figsize=(10,5))
sns.histplot(df['Watch Reason'])
plt.xticks(rotation=45)
plt.title('Watch Reason')
plt.show()
```
📌 Insight: Top reasons: Habit, Boredom, Entertainment

### 6. Current Activity
```
df['CurrentActivity'].value_counts().plot(kind='pie', autopct='%1.1f%%')
plt.title('Current Activity')
plt.ylabel('')
plt.show()
```
📌 Insight: Most users are active at Home or School

### 7. Watch Time Distribution
```
plt.figure(figsize=(10,5))
sns.histplot(df['Watch Time'])
plt.xticks(rotation=45)
plt.title('Watch Time Distribution')
plt.show()
```
📌 Insight: Peak usage occurs during lunch breaks and after work

### 8. Device & OS Analysis
```
plt.figure(figsize=(12,5))
plt.subplot(1, 2, 1)
sns.histplot(df['DeviceType'])
plt.title('Device Type')
plt.subplot(1, 2, 2)
sns.histplot(df['OS'])
plt.title('Operating System')
plt.show()
```
📌 Insight: Smartphones and Android dominate usage

### 9. Connection Type
```
sns.histplot(df['ConnectionType'])
plt.title('Connection Type')
plt.show()
```
📌 Insight: Most users rely on mobile data

### 10. Device vs Addiction Level
```
plt.figure(figsize=(10,5))
sns.scatterplot(x='DeviceType', y='Addiction Level', data=df)
plt.title('Device Type vs Addiction Level')
plt.xticks(rotation=45)
plt.show()
```
📌 Insight: Smartphone users show varied addiction levels

---

### 🧠 Key Findings  

- 📱 Smartphones are the primary access device.  
- 🌍 Rural users are highly active.  
- ⏰ Usage peaks during free time (lunch/after work).  
- 😴 Habit and boredom drive most engagement.  
- 📶 Mobile data is the dominant connection type.  

---

### 🔮 Future Improvements  

- Build predictive models for addiction levels.  
- Perform user segmentation (clustering).  
- Develop interactive dashboards (Power BI / Streamlit).  

---

### 📜 License  

Open-source for educational and research purposes.  

---

## 🌍 Impact  

This project provides insights into social media behavior, helping businesses improve marketing strategies and individuals understand their digital habits.
