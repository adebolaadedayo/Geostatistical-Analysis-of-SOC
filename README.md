# A Geostatistical Analysis of SOC Distribution in Bavaria, Germany

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/5091575f-3869-499d-9163-19158129f3dd" />

*This project evaluated the performance of deterministic (IDW), geostatistical (OK, EBK), and hybrid (EBKR)  models in mapping the spatial distribution of Soil Organic Carbon (SOC) in a heterogeneous terrain like Bavaria, Germany.*

---

# Background

Soil organic carbon (SOC) represents the largest terrestrial carbon pool, containing significantly more carbon than the atmosphere and global vegetation combined (Chen et al., 2023; Y. Wang et al., 2011). Maintaining and increasing SOC stocks is essential for soil ecosystem services, including nutrient cycling, water retention, and the prevention of land degradation (Mustafa et al., 2020).

In Germany, mapping SOC at regional scales is essential for national greenhouse gas inventories and environmental reporting (Broeg et al., 2024). The distribution of SOC in Bavaria is highly heterogeneous, influenced by a complex interaction of climate, parent material, topography, and centuries of varied land-use history (Broeg et al., 2024).

Soil research is still reliant on traditional point-based sampling, but it does not provide the continuous coverage required for spatial decision-making (Sahu et al., 2021). Geostatistical methods, such as Ordinary Kriging (OK) and Empirical Bayesian Kriging (EBK), address this by modelling the spatial autocorrelation of SOC to predict values at unsampled locations (John et al., 2021; Veronesi & Schillaci, 2019). These methods provide the Best Linear Unbiased Estimate (BLUE) but often assume spatial stationarity, which may not hold true across a heterogeneous landscape like Bavaria (Sahu et al., 2021; Tziolas et al., 2024).

To enhance mapping accuracy, researchers have recently adopted Digital Soil Mapping (DSM) frameworks that utilize environmental covariates (Gibson et al., 2021; Y. Wang et al., 2011). Methods like Empirical Bayesian Kriging Regression (EBKR) allow for the integration of explanatory variables such as elevation and slope derived from Digital Elevation Models (DEMs), as well as soil physicochemical properties like Nitrogen and Clay content, to model the non-spatial variance of SOC (John et al., 2021; Sahu et al., 2021; Y. Wang et al., 2011).

---

# Objectives

The main objectives of this project were to:

- Assess the predictive accuracy of **deterministic** (IDW) and **stochastic** (OK and EBK) methods in mapping the spatial distribution of Soil Organic Carbon (SOC) in Bavaria.
- Investigate the integration of *environmental covariates*, including a terrain derivative (elevation) and a soil physicochemical property (Nitrogen), using the **Empirical Bayesian Kriging Regression** technique.
- Produce a definitive **SOC prediction surface** and an associated **Prediction Standard Error map** to quantify the spatial distribution of carbon stocks in Bavaria and identify high-uncertainty areas.

---

# Repository Structure

### 📂 Repository Structure

```text
├── analysis/
│   ├── esda/                # Global/Local Moran's I results, Voronoi maps
│   └── validation/          # Cross-validation tables (RMSE/ME metrics)
├── data/
│   ├── raw/                 # LUCAS 2018 Topsoil Data
│   ├── processed/           # Cleaned LUCAS 2018 Topsoil Data
│   └── shapefiles/          # GADM Bavaria boundary
├── docs/                    # Final PDF Report and Appendix tables
├── output/
│   ├── maps/                # High-resolution prediction surfaces and error maps
│   └── stats/               # Descriptive statistics and semivariogram plots
└── README.md                # The main project landing page

```

---

# 🛠️ Technical Stack (ArcGIS Pro Workflow) 

This project was developed exclusively using **ArcGIS Pro**, leveraging advanced geostatistical extensions for predictive modeling.

* **Geostatistical Modeling:** Geostatistical Wizard, Ordinary Kriging, Empirical Bayesian Kriging (EBK).
* **Hybrid Modeling:** EBK Regression Prediction (incorporating SRTM DEM and Nitrogen covariates).
* **Spatial Statistics:** Global/Local Moran's I (Anselin), Voronoi Tessellation, and Outlier Analysis.
* **Data Preprocessing:** Coordinate System Transformation (ETRS 1989 UTM Zone 32N), Dimensionality Reduction, and Spatial Clipping.
* **Validation:** Leave-one-out Cross-Validation (LOOCV) using RMSE and Mean Error metrics.

---

# Methodology

![methodology](https://github.com/user-attachments/assets/c7555d59-a113-4cce-810e-89976e192c26)

- **Data:** 118 topsoil samples from the LUCAS 2018 dataset in [ESDAC](https://esdac.jrc.ec.europa.eu/content/lucas-2018-topsoil-data) and boundary shapefile obtained from [GADM](https://gadm.org/data.html).
- **Analysis:** Conducted Exploratory Spatial Data Analysis (ESDA) using Global and Local Moran's I to identify spatial clustering
- **Validation:** Models were cross-validated using RMSE and Mean Error (ME).

---

# Key Findings

| Parameter          | IDW    | OK     | EBK    | EBKR   |
| --------------     | ------ | ------ | ------ | ------ |
| Mean Error (ME)    | -0.461 | 0.040  | -0.005 | 0.008  |                       
| RMSE               | 19.792 | 16.449 | 16.618 | 16.680 |

- **Best Model:** Empirical Bayesian Kriging Regression (EBKR).
- **Result:** The EBKR achieved the highest local precision (standard error of 1.88) by integrating Elevation and Nitrogen as covariates.
- **Spatial Trend:** There was a significant North-South gradient with carbon hotspots in the Alpine foreland.

---

# Authors

* #### [Adebola David Adedayo](https://github.com/adebolaadedayo)
* #### [Saba Fatima](https://github.com/saba-fatima-eng)
