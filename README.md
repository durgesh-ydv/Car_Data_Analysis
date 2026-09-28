# Used Car Data Analysis

## 📌 Project Overview

This project performs an **Exploratory Data Analysis (EDA) of used cars** to understand pricing patterns, vehicle characteristics, customer preferences, and factors that influence used-car selling prices.

The project covers the complete data-analysis workflow, including **data cleaning, exploratory analysis, statistical analysis, visualization, and MySQL integration**.

---

## 🎯 Objectives

The main objectives of this project are to:

* Clean and prepare the used-car dataset for analysis.
* Explore the distribution and characteristics of used vehicles.
* Analyze relationships between vehicle features and selling price.
* Identify popular car brands and models.
* Understand the impact of vehicle age, mileage, engine, and power on selling price.
* Compare selling prices across fuel types, transmission types, and seller types.
* Store and retrieve the cleaned dataset using MySQL.
* Generate meaningful insights through data visualization.

---

## 🗂️ Project Structure

```text
car_data_analysis/
│
├── Used_Car_Data_Analysis.ipynb
├── requirements.txt
├── README.md
│
├── data/
│   ├── raw_car_data.csv
│   └── cleaned_car_data.csv
│
└── images/
    ├── image_1.png
    ├── image_2.png
    ├── image_3.png
    └── ...
```

### Files & Folders Description

| File / Folder                  | Description                                     |
| ------------------------------ | ----------------------------------------------- |
| `Used_Car_Data_Analysis.ipynb` | Complete Python analysis and visualizations     |
| `requirements.txt`             | Python libraries required to run the project    |
| `README.md`                    | Project documentation                           |
| `data/`                        | Contains raw and cleaned datasets               |
| `raw_car_data.csv`             | Original/raw dataset                            |
| `cleaned_car_data.csv`         | Cleaned dataset used for analysis               |
| `images/`                      | Selected visualization images from the analysis |

---

## 🛠️ Technologies & Libraries

### Programming Language

* **Python**

### Data Analysis

* **Pandas**
* **NumPy**

### Data Visualization

* **Matplotlib**
* **Seaborn**
* **Plotly**

### Database

* **MySQL**
* **SQLAlchemy**
* **PyMySQL**

The complete list of dependencies is available in `requirements.txt`.

---

## 🔄 Project Workflow

```text
Raw Dataset
     ↓
Data Loading
     ↓
Data Cleaning & Preprocessing
     ↓
Exploratory Data Analysis
     ↓
Statistical Analysis
     ↓
Data Visualization
     ↓
MySQL Database Integration
     ↓
Business Insights
```

---

## 🧹 Data Cleaning & Preparation

The dataset was processed before performing the analysis.

The cleaning process included:

* Loading the raw CSV dataset using Pandas.
* Removing unnecessary columns.
* Handling missing values.
* Resetting the DataFrame index.
* Converting numerical columns into appropriate data types.
* Checking categorical and numerical variables.
* Creating a cleaned dataset for further analysis.
* Saving the cleaned data as a CSV file.

After cleaning, the dataset contained approximately **15,411 records and 13 columns**.

---

## 🗄️ MySQL Integration

The cleaned dataset was also integrated with **MySQL**.

The workflow includes:

1. Establishing a connection between Python and MySQL.
2. Uploading the cleaned dataset into a MySQL table.
3. Retrieving the data from MySQL.
4. Performing further analysis using the retrieved data.

### Database Connection

For security, database credentials are handled through environment variables instead of being directly written in the notebook.

```python
import os
from sqlalchemy import create_engine

user = os.getenv("MYSQL_USER")
password = os.getenv("MYSQL_PASSWORD")
database = os.getenv("MYSQL_DATABASE")

engine = create_engine(
    f"mysql+pymysql://{user}:{password}@localhost:3306/{database}"
)
```
---

## 📊 Exploratory Data Analysis

The project performs both **univariate and multivariate analysis**.

### Univariate Analysis

The analysis explores individual variables such as:

* Selling price
* Vehicle age
* Kilometers driven
* Mileage
* Engine
* Max power
* Fuel type
* Transmission
* Seller type
* Car brand
* Car model

Visualizations include:

* Histograms
* Count plots
* Distribution plots
* Bar charts
* Pie charts

### Multivariate Analysis

Relationships between multiple variables were analyzed, including:

* Brand vs. Selling Price
* Fuel Type vs. Selling Price
* Transmission vs. Selling Price
* Seller Type vs. Selling Price
* Vehicle Age vs. Selling Price
* Vehicle Age vs. Mileage
* Kilometers Driven vs. Selling Price
* Engine vs. Selling Price
* Max Power vs. Selling Price

---

## 📈 Correlation Analysis

Correlation analysis was performed to understand the relationship between numerical variables.

Some notable relationships with **selling price** include:

| Feature     | Correlation with Selling Price |
| ----------- | -----------------------------: |
| Max Power   |                          ~0.75 |
| Engine      |                          ~0.59 |
| Vehicle Age |                         ~-0.24 |
| KM Driven   |                         ~-0.08 |

The analysis indicates that **max power and engine size have relatively stronger positive relationships with selling price**, while vehicle age has a negative relationship.

> Correlation indicates association between variables and does not by itself establish causation.

---

## 🔍 Key Analysis Areas

The project investigates several questions, including:

* Which car models appear most frequently in the dataset?
* Which brands have the highest representation?
* What is the distribution of used-car selling prices?
* Which vehicles have the highest selling prices?
* How does vehicle age relate to selling price?
* How does kilometers driven relate to selling price?
* How does engine size relate to selling price?
* How does maximum power relate to selling price?
* How does fuel type affect the distribution of selling prices?
* How do manual and automatic vehicles compare?
* How do seller types differ?
* Which fuel types are most common?
* How does mileage vary across brands?

---

## 💡 Key Insights

The analysis provides several observations from the dataset:

* The cleaned dataset contains approximately **15,411 used-car records**.
* The dataset contains **32 brands** and **121 unique car names**.
* **Hyundai i20** is one of the most frequently represented car models in the dataset.
* Manual transmission vehicles are considerably more common than automatic vehicles.
* Dealer vehicles represent a significant portion of the dataset.
* Maximum power shows a relatively strong positive relationship with selling price.
* Engine size also shows a positive relationship with selling price.
* Older vehicles generally tend to have lower selling prices.
* Kilometers driven shows a relatively weak negative relationship with selling price.
* Selling prices vary considerably across fuel types, brands, transmission types, and seller types.

---

## 📷 Project Visualizations

Selected visualizations from the analysis are available in the [`images/`](./images/) folder.

Examples include:

* Selling Price Distribution
* Correlation Heatmap
* Top Car Models
* Brand Analysis
* Fuel Type Analysis
* Transmission Analysis
* Vehicle Age vs. Selling Price
* KM Driven vs. Selling Price
* Engine vs. Selling Price
* Max Power vs. Selling Price

---

## 📦 Installation

Clone the repository:

```bash
git clone https://github.com/your-username/car_data_analysis.git
```

Navigate to the project directory:

```bash
cd car_data_analysis
```

Install the required libraries:

```bash
pip install -r requirements.txt
```

---

## ▶️ Running the Project

Open the notebook using **Jupyter Notebook** or **VS Code**:

```text
Used_Car_Data_Analysis.ipynb
```

Run the notebook cells sequentially to reproduce the analysis.

If you want to use the MySQL section, make sure:

* MySQL is installed and running.
* A MySQL database is available.
* Your MySQL environment variables are configured.

Example environment variables:

```text
MYSQL_USER=your_username
MYSQL_PASSWORD=your_password
MYSQL_DATABASE=your_database
```

---

## 📋 Requirements

The project uses the following major Python libraries:

```text
pandas
numpy
matplotlib
seaborn
sqlalchemy
pymysql
plotly
```

Install all dependencies using:

```bash
pip install -r requirements.txt
```

---

## 🚀 Skills Demonstrated

This project demonstrates practical experience with:

* Python for Data Analysis
* Pandas
* NumPy
* Data Cleaning
* Exploratory Data Analysis (EDA)
* Statistical Analysis
* Data Visualization
* Matplotlib
* Seaborn
* Plotly
* MySQL
* SQLAlchemy
* PyMySQL
* Data Interpretation
* Business-oriented Data Analysis

---

## 📌 Future Improvements

Potential improvements to the project include:

* Building an interactive dashboard using **Power BI**.
* Adding more advanced statistical analysis.
* Creating a predictive model for used-car prices.
* Performing feature engineering.
* Comparing machine-learning models for price prediction.
* Deploying an interactive application for used-car price analysis.

---

## 👨‍💻 Author

**Durgesh Yadav**

Data Analyst | Python | SQL | Power BI | Excel

---

## ⭐ Project

If you find this project useful, feel free to **star the repository** and explore the notebook for the complete analysis.
