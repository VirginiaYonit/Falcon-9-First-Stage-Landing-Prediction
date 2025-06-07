# Falcon-9 First Stage Landing Prediction

A data science capstone project simulating the role of a data scientist at *SpaceY*, a fictional competitor to SpaceX.

## Project Goal

Predict whether the Falcon 9 first stage will successfully land after launch, using public data from the SpaceX API and Wikipedia. The aim is to support launch cost estimation and mission planning through machine learning.

## Project Structure

- **Data Collection**:  
  - SpaceX REST API (`/v4/launches/past` and additional endpoints)
  - Web scraping from Wikipedia using BeautifulSoup

- **Data Wrangling & Feature Engineering**:  
  - Filtering for Falcon 9 only  
  - Handling missing values (`PayloadMass`)  
  - One-hot encoding of categorical features  
  - Merging data sources

- **EDA**:  
  - SQL queries and Python visualizations (seaborn, matplotlib)  
  - Exploration of success rates by orbit, site, booster version, etc.

- **Interactive Visualizations**:  
  - Folium maps for launch site context  
  - Dash dashboard to explore success rate by site and payload

- **Machine Learning**:  
  - Pipeline: `StandardScaler → SelectKBest → Classifier`  
  - Models: Logistic Regression, SVM, KNN, Decision Tree  
  - Best model: **SVM with RBF kernel**

## Key Results

- SVM model achieves 83.3% accuracy  
- Orbit, payload mass, and launch site were key predictive features  
- Folium maps and Dash app provide accessible, interactive insights

## Notebooks

You can find all completed notebooks in the `/notebooks` folder:
- Data collection via API and scraping
- SQL exploratory analysis
- EDA and visualization
- Machine learning pipeline

## Dashboard & Visuals

- Plotly Dash app: interactive site & payload analysis  
- Folium maps: spatial launch site insights  
(*Screenshots available in `/images` and final presentation*)

## Presentation

The full presentation is available in PDF/PowerPoint format in this repository.  
Peer-reviewed as part of the IBM Data Science Capstone.

## Tools Used

- Python, Pandas, NumPy  
- BeautifulSoup, SQLite, Seaborn, Matplotlib, Plotly, Folium, Dash  
- Scikit-learn, GridSearchCV

## Author

**Virginia Levy Abulafia**  
Capstone project for the [IBM Data Science Certificate](https://www.coursera.org/professional-certificates/ibm-data-science)

---


