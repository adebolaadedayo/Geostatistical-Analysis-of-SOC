# A Geostatistical Analysis of SOC Distribution in Bavaria, Germany

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/5091575f-3869-499d-9163-19158129f3dd" />

*This study evaluated the performance of deterministic (IDW), geostatistical (OK, EBK), and hybrid (EBKR)  models in mapping the spatial distribution of Soil Organic Carbon (SOC) in a heterogeneous terrain like Bavaria, Germany.*

---

# Background

Soil organic carbon (SOC) represents the largest terrestrial carbon pool, containing significantly more carbon than the atmosphere and global vegetation combined (Chen et al., 2023; Y. Wang et al., 2011). Maintaining and increasing SOC stocks is essential for soil ecosystem services, including nutrient cycling, water retention, and the prevention of land degradation (Mustafa et al., 2020).

In Germany, mapping SOC at regional scales is essential for national greenhouse gas inventories and environmental reporting (Broeg et al., 2024). The distribution of SOC in Bavaria is highly heterogeneous, influenced by a complex interaction of climate, parent material, topography, and centuries of varied land-use history (Broeg et al., 2024).

Soil research is still reliant on traditional point-based sampling, but it does not provide the continuous coverage required for spatial decision-making (Sahu et al., 2021). Geostatistical methods, such as Ordinary Kriging (OK) and Empirical Bayesian Kriging (EBK), address this by modelling the spatial autocorrelation of SOC to predict values at unsampled locations (John et al., 2021; Veronesi & Schillaci, 2019). These methods provide the Best Linear Unbiased Estimate (BLUE) but often assume spatial stationarity, which may not hold true across a heterogeneous landscape like Bavaria (Sahu et al., 2021; Tziolas et al., 2024).

To enhance mapping accuracy, researchers have recently adopted Digital Soil Mapping (DSM) frameworks that utilize environmental covariates (Gibson et al., 2021; Y. Wang et al., 2011). Methods like Empirical Bayesian Kriging Regression (EBKR) allow for the integration of explanatory variables such as elevation and slope derived from Digital Elevation Models (DEMs), as well as soil physicochemical properties like Nitrogen and Clay content, to model the non-spatial variance of SOC (John et al., 2021; Sahu et al., 2021; Y. Wang et al., 2011).

# Objectives

The main objectives of this project were to:

- Assess the predictive accuracy of **deterministic** (IDW) and **stochastic** (OK and EBK) methods in mapping the spatial distribution of Soil Organic Carbon (SOC) in Bavaria.
- Investigate the integration of *environmental covariates*, including a terrain derivative (elevation) and a soil physicochemical property (Nitrogen), using the **Empirical Bayesian Kriging Regression** technique.
- Produce a definitive **SOC prediction surface** and an associated **Prediction Standard Error map** to quantify the spatial distribution of carbon stocks in Bavaria and identify high-uncertainty areas.


---

# Authors

* #### [Adebola David Adedayo](https://github.com/adebolaadedayo)
* #### [Saba Fatima](https://github.com/saba-fatima-eng)
