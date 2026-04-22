# GigSmart AI 
### AI-Powered Earning Advisor for Indian Gig Workers


## Problem Statement

India has 12+ million food delivery gig workers 
working across platforms like Zomato, Swiggy, and 
Blinkit. These workers randomly decide which app 
to login to — resulting in significant income loss.

**No AI-powered decision support tool exists 
for Indian gig workers.**



## Solution

GigSmart AI is a machine learning system that 
analyzes time, weather, location, and order 
patterns to recommend:

1. **Which app to login** (Zomato/Swiggy/Blinkit)
2. **Expected earning** for that session

---

## Dataset

- **Source:** Kaggle Food Delivery Dataset 
  (gauravmalik26/food-delivery-dataset)
- **Type:** Hybrid — Real Kaggle data enriched 
  with India-specific synthetic features
- **Size:** 45,593 records, 16 features
- **Target Variables:**
  - best_app — Classification
  - net_profit — Regression

### Features Used
| Feature            | Type        | Source                  |
| ------------------ | ----------- | ----------------------- |
| hour               | Numerical   | Extracted from dataset  |
| day_of_week        | Numerical   | Extracted from date     |
| is_weekend         | Binary      | Derived                 |
| is_festival        | Binary      | Real data               |
| weather            | Categorical | Real data               |
| zone_type          | Categorical | Derived from city       |
| is_lunch_time      | Binary      | Derived from hour       |
| is_dinner_time     | Binary      | Derived from hour       |
| distance_km        | Numerical   | Synthetic (zone-based)  |
| estimated_time_min | Numerical   | Real data               |
| expected_payout    | Numerical   | Synthetic (India logic) |
| fuel_cost          | Numerical   | Derived                 |
| time_cost          | Numerical   | Derived                 |
| net_profit         | Numerical   | Calculated              |
| best_app           | Categorical | Target (Classification) |


## Key EDA Findings

- **Rain** generates 2x profit (Rs 75) vs 
  clear weather (Rs 40)
- **Swiggy** earns 4x more on weekends (Rs 79) 
  vs Blinkit (Rs 17)
- **Blinkit** dominates busy metro zones (78%)
- **Zomato** strongest during lunch + festivals
- **Evening 17-23** has highest order volume
- **expected_payout** is strongest profit 
  predictor (correlation: 0.801)

---

## Project Structure

GigSmart-AI/
├── data/
│   ├── raw/              ← Kaggle dataset
│   └── processed/        ← Final ML dataset
├── notebooks/
│   ├── dataset_prep.ipynb← Data preparation
│   └── eda.ipynb         ← Exploratory analysis
├── src/                  ← ML models (coming soon)
├── requirements.txt
└── README.md

---

## Tech Stack

| Category | Technology |
|----------|-----------|
| Language | Python 3.13 |
| Data Processing | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| ML Models | Scikit-learn (coming soon) |
| IDE | VS Code + Jupyter |

---

## Target Distribution

|| App     | Count  | Percentage |
| ------- | ------ | ---------- |
| Blinkit | 16,007 | 35.1%      |
| Zomato  | 15,794 | 34.6%      |
| Swiggy  | 13,792 | 30.3%      |



## Real World Impact

- Target users: **12M+ Indian gig workers**
- Estimated additional monthly earning: 
  **Rs 1,500 - 2,000**
- Zero existing AI solution in India 
  for this problem
- Works for Zomato, Swiggy, and Blinkit

---

## Setup & Installation

```bash
# Clone the repository
git clone https://github.com/Loveena-15/GigSmart-AI

# Navigate to project
cd GigSmart-AI

# Create virtual environment
python -m venv venv
venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```




## Contributors

**Loveena**
- GitHub:https://github.com/Loveena-15?tab=repositories
- LinkedIn:https://www.linkedin.com/in/loveena-loveena-3a609a327/

**Kashish**
- GitHub:https://github.com/Kashishtalwar12
- LinkedIn:https://www.linkedin.com/in/kashish-talwar-610592324?utm_source=share_via&utm_content=profile&utm_medium=member_android