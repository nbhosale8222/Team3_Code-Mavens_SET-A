UrbanPulse  - Urban Mobility Analytics Platform

> **Python Data Science Hackathon – Set A**
> **Team 3 | Code Mavens**

UrbanPulse AI is a comprehensive urban mobility analytics platform designed to analyze public transportation data, improve route efficiency, detect data quality issues, and provide actionable insights through interactive dashboards and geospatial visualization.

The project goes beyond the hackathon requirements by implementing a modular data engineering pipeline, custom algorithms, statistical analytics, and a full-fledged Streamlit dashboard.

---

##  Features

###  Intelligent ETL Pipeline

* Cleans and validates noisy transportation datasets
* Handles missing values using route-wise median imputation
* Detects and caps passenger outliers using Z-score analysis
* Standardizes route IDs and zone names
* Generates derived analytical features
* Exports cleaned dataset automatically

---

###  Custom Route Ranking Algorithm

Implemented completely **without using Python's built-in sorting functions**.

Features:

* Custom Merge Sort (O(n log n))
* Route efficiency computation
* Passenger ranking
* Delay-aware efficiency scoring
* Top 5 and Bottom 5 route identification
* Correctness assertion after sorting

Efficiency Score:

```text
Efficiency = Average Passengers / (1 + Average Delay)
```

---

###  Advanced Analytics Dashboard

Generates a high-quality 4-panel analytical dashboard containing:

* Daily passenger trend with rolling average
* Passenger distribution by zone
* Delay histogram with normal distribution curve
* Route efficiency scatter plot

Output:

```
mobility_dashboard.png
```

---

###  Interactive Mobility Map

Built using **Folium**

Includes:

* Zone-wise Circle Markers
* Passenger HeatMap
* Traffic intensity visualization
* Interactive popups
* Layer controls

Output:

```
city_mobility_map.html
```

---

###  Bonus Streamlit Dashboard

UrbanPulse AI also provides a modern interactive dashboard featuring:

* Data Quality Analysis
* Route Intelligence
* Recommendation Engine
* Analytics Dashboard
* Interactive Folium Map
* Download Center

---

#  Project Architecture

```
UrbanPulse-AI
│
├── pipeline.py          # Complete business logic
├── solution.py          # CLI Entry Point
├── app.py               # Streamlit Dashboard
├── requirements.txt
│
├── outputs/
│   ├── cleaned_ridership.csv
│   ├── mobility_dashboard.png
│   └── city_mobility_map.html
│
└── README.md
```

The project follows a clean layered architecture:

```
Raw Dataset
      │
      ▼
 ETL Pipeline
      │
      ▼
Clean Dataset
      │
      ├────────► Statistical Dashboard
      │
      ├────────► Route Ranking
      │
      └────────► Interactive Map
                     │
                     ▼
              Streamlit Dashboard
```

---

#  Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Folium
* Streamlit
* streamlit-folium

---

#  Outputs

The pipeline automatically generates:

| File                     | Description                  |
| ------------------------ | ---------------------------- |
| `cleaned_ridership.csv`  | Clean transportation dataset |
| `mobility_dashboard.png` | Statistical dashboard        |
| `city_mobility_map.html` | Interactive zone map         |

---

#  Running the Project

## 1. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 2. Run Complete Pipeline

```bash
python solution.py
```

---

## 3. Launch Interactive Dashboard

```bash
streamlit run app.py
```

---

#  Data Cleaning Pipeline

The ETL engine performs:

* Passenger value correction
* Route-wise delay imputation
* Zone normalization
* Route ID cleaning
* Outlier detection
* Feature engineering
* CSV generation

---

#  Algorithm Used

Instead of Python's built-in sorting methods, the project implements:

* Recursive Merge Sort
* Stable Merge Operation
* Generic Key-Based Sorting

Time Complexity:

```
O(n log n)
```

Space Complexity:

```
O(n)
```

---

#  Dashboard Visualizations

✔ Daily Passenger Trends

✔ Rolling Mean Analysis

✔ Zone-wise Passenger Distribution

✔ Delay Distribution

✔ Route Efficiency Scatter Plot

---

#  Interactive Mapping

The Folium map visualizes:

* Passenger density
* Zone performance
* HeatMap analysis
* Peak traffic regions
* Interactive statistics

---

#  Key Highlights

* Modular software architecture
* Production-style ETL pipeline
* Custom Merge Sort implementation
* Statistical data analysis
* Geospatial visualization
* Interactive Streamlit application
* Automated output generation
* Reproducible pipeline using fixed random seed

---

#  Repository Structure

```
.
├── app.py
├── pipeline.py
├── solution.py
├── requirements.txt
├── README.md
├── cleaned_ridership.csv
├── mobility_dashboard.png
└── city_mobility_map.html
```

---

#  Team

**Team 3 – Code Mavens**

Python Data Science Hackathon

---

#  License

This project was developed for educational and hackathon purposes.

---

## ⭐ If you found this project useful, consider giving it a Star!
