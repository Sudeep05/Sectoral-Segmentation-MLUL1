# Customer and Sectoral Segmentation using K-Means Clustering

This repository contains end-to-end Machine Learning workflows for behavioral and financial segmentation using K-Means clustering. The projects demonstrate data preprocessing, exploratory data analysis (EDA), optimal cluster selection, and business insight generation.

##  Project Structure

- **`GR_02_MLUL1_mall_of_america.ipynb`**: Focuses on customer behavioral segmentation based on mall Wi-Fi session data.
- **`GR_02_MLUL1_sectoral_segments.ipynb`**: Focuses on segmenting companies in the Pharmaceutical sector based on quarterly financial ratios.

---

##  1. Mall of America: Customer Behavioral Segmentation

### **Problem Statement**
The goal is to understand how shoppers navigate the Mall of America (MoA) to identify distinct segments for targeted marketing and operational improvements.

### **Key Workflow**
1.  **Data Cleaning**: Filtered out employees and extremely short visits (outliers) to focus on genuine shoppers.
2.  **Feature Engineering**: Created floor-based occupancy percentages (L0 to L4) as primary behavioral features.
3.  **Cluster Selection**: Used **Elbow Method** and **Silhouette Scores** to determine the optimal number of shopper segments.
4.  **Multi-Level Segmentation**:
    * **Level 1**: Global segmentation based on floor occupancy.
    * **Level 2**: Sub-segmentation of the "Floor 3 dominant" group to identify micro-segments by mall wings (North, South, East, West).
5.  **Visualization**: Principal Component Analysis (PCA) was used for 2D visualization of high-dimensional clusters.

### **Identified Segments**
- **L3 Leisure**: High occupancy on the entertainment floor (cinemas/dining).
- **Quick Errands**: Targeted visits with low duration, mostly on lower levels.
- **Explorers**: Shoppers who balance time across multiple floors.

---

## 2. Sectoral Segmentation: Pharmaceutical Financial Analysis

### **Problem Statement**
To detect company segments based on financial performance and risk profiles within the pharmaceutical industry using quarterly balance sheet data.

### **Key Workflow**
1.  **Exploratory Data Analysis (EDA)**: Analyzed 50 companies across 14 financial features, including ROA, ROE, Debt/Equity, and Sales Growth.
2.  **Preprocessing**: Normalized financial ratios using `StandardScaler` to handle varying units (percentages vs. absolute values).
3.  **Clustering Technique**:
    * Implemented **K-Means** for general performance grouping.
    * Used **DBSCAN** for outlier detection to identify companies with highly unusual financial profiles.
4.  **Evaluation**: Utilized Silhouette Analysis to validate segment cohesion.

### **Business Applications**
- **Risk Assessment**: Identifying high-debt companies with low asset turnover.
- **Growth Identification**: Segmenting high-growth "rising stars" based on sales growth and ROCE.

---

## Tech Stack
- **Languages**: Python
- **Libraries**: 
    - `scikit-learn`: K-Means, DBSCAN, PCA, Silhouette Score.
    - `pandas` & `numpy`: Data manipulation.
    - `matplotlib` & `seaborn`: Data visualization.

## How to Use
1.  **Clone the repo**:
    ```bash
    git clone <your-repo-url>
    ```
2.  **Install dependencies**:
    ```bash
    pip install pandas numpy scikit-learn matplotlib seaborn openpyxl
    ```
3.  **Run the notebooks**: Open the `.ipynb` files in Jupyter Lab, Jupyter Notebook, or Google Colab to see the analysis results and visualizations.

---
