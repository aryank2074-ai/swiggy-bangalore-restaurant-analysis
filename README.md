# swiggy-bangalore-restaurant-analysis
# 🍛 Swiggy Bangalore Restaurant Analysis

> **Where should you eat in Bangalore's foodie hubs — without burning a hole in your pocket?**
> An exploratory data analysis of Swiggy restaurants across **Koramangala, HSR Layout and BTM Layout**, uncovering rating trends, pricing patterns and cuisine popularity.

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Cleaning-150458?logo=pandas)
![Plotly](https://img.shields.io/badge/Plotly-Interactive%20Charts-3F4F75?logo=plotly)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4c72b0)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)

---

## 📌 Project Overview

Swiggy lists hundreds of outlets in Bangalore, but which ones actually offer **great ratings at a friendly price**? This project cleans a Swiggy outlet dataset and answers questions such as:

- 🌟 How are ratings distributed across restaurants?
- 💸 Is a higher cost-for-two really linked to a higher rating?
- 📍 How do **Koramangala, HSR and BTM** compare on price and quality?
- 🍜 Which cuisines dominate the Bangalore food scene?
- 🏆 Which restaurants are both **highly rated (4.0+)** and **budget-friendly (≤ ₹500 for two)**?

---

## 📂 Dataset

| Column | Description |
|---|---|
| `Shop_Name` | Name of the restaurant / outlet |
| `Cuisine` | Comma-separated list of cuisines served |
| `Location` | Sub-area and locality (e.g. *Sector 5, HSR*) |
| `Rating` | Swiggy customer rating |
| `Cost_for_Two` | Approximate cost for two people (₹) |

**Size:** 118 outlets × 5 features · **Duplicates:** 0 · **Missing values:** 0

---

## 🧹 Data Cleaning & Preparation

- Converted `Rating` from text to `float`; unrated outlets (`--`) were set to `0` and excluded from rating-distribution plots
- Stripped the `₹` symbol from `Cost_for_Two` and converted it to `int`
- Standardised cuisine text with `.str.title()`
- Grouped outlets by area (Koramangala / HSR / BTM) using text matching on `Location`
- Split multi-cuisine strings to build cuisine frequency tables

---

## 🔍 Analysis Performed

1. **Rating distribution** across all rated restaurants
2. **Area-wise analysis** – rating and cost histograms for BTM, HSR and Koramangala
3. **Cost vs. Rating** interactive scatter plot (Plotly)
4. **Best-value finder** – restaurants with rating ≥ 4.0 and cost ≤ ₹500
5. **Top 15 cheapest** and **top 15 most expensive** highly rated restaurants
6. **Cuisine analysis** – overall and area-wise bar + pie charts

---

## 💡 Key Insights

| Area | Typical Rating | Typical Cost for Two | Max Cost |
|---|---|---|---|
| **BTM** | ~4.0 – 4.2 | ₹200 – ₹350 | ₹600 |
| **HSR** | 4.0 and above | ₹300 – ₹400 | ₹800 |
| **Koramangala** | ~4.0 – 4.3 | ₹200 – ₹350 | ₹600 |

- ✅ **92 of 118** outlets have a rating of 4.0 or higher, and **82** of them cost ₹500 or less for two
- 🥇 **Khichdi Experiment** tops the value list with a **4.8 rating at just ₹200** for two
- 🍦 Ice-cream brands like **Natural Ice Cream** and **Corner House** hold a strong **4.6** at low prices
- 🥢 **Chinese, North Indian and South Indian** are the most frequent cuisine tags, followed by **Biryani, Fast Food and Desserts**
- 📈 Paying more does **not** guarantee a better rating — many budget outlets match or beat pricier ones

---

## 🛠️ Tech Stack

- **Language:** Python
- **Data handling:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn, Plotly Express
- **Environment:** Jupyter Notebook

---

## 🚀 Getting Started

```bash
# 1. Clone the repository
git clone https://github.com/<aryank2074-a>/swiggy-bangalore-restaurant-analysis.git
cd swiggy-bangalore-restaurant-analysis

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn plotly jupyter

# 3. Launch the notebook
jupyter notebook swiggy_project_new.ipynb
```

> Make sure `Swiggy Bangalore Outlet Details.csv` is in the same folder as the notebook.

---

## 📁 Project Structure

```
├── swiggy_project_new.ipynb            # Main analysis notebook
├── Swiggy Bangalore Outlet Details.csv # Dataset
└── README.md
```

---

## 🔮 Future Improvements

- Scrape a larger dataset covering more Bangalore neighbourhoods
- Add review counts / delivery time for deeper analysis
- Build a **restaurant recommendation** system based on budget + cuisine
- Deploy an interactive dashboard using Streamlit

---

## 🙋 Author

**Aryan**
Feel free to ⭐ the repo if you found it useful, and connect with me on [LinkedIn](#) / [GitHub](#).
