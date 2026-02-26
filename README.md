# VukelicEtAl2026_NigerGiraffeCMR_TempAndPrecip
This repository contains supporting data and R scripts for the capture-mark-recapture (CMR) analyses used to assess the effects of temperature and precipitation on apparent survival of the West African giraffe in the Giraffe Zone (2005–2018), implemented using multistate mark-recapture (MSMR) models. It also includes the Google Earth Engine (GEE) scripts used to extract the climate covariates and the digitised habitat polygon (GeoJSON; derived from O’Connor et al., 2019) required to reproduce the climate data extraction workflow.

## Repository Structure

---

### 📂 R/

R scripts used for multistate mark–recapture (MSMR) analyses and goodness-of-fit assessment.

- **MSMR_temperature_GZ.R**  
  Performs MSMR analysis with temperature as a covariate  
  (number of days with maximum daily temperature ≥ 35 °C, excluding December–February).

- **GOF_MSMR_temperature.R**  
  Fits and exports a saturated global MSMR model for goodness-of-fit evaluation.

- **MSMR_precipitation_GZ.R**  
  Performs MSMR analysis with precipitation as a covariate  
  (total June–July–August precipitation, mm).

- **GOF_MSMR_precipitation.R**  
  Fits and exports a saturated global MSMR model for goodness-of-fit evaluation.

---

### 📂 data_for_R/

Input data used in the R analyses.

- **DailyMaxTemp_GZ_simple_05_18.csv**  
  Daily maximum temperature (°C), 1 January 2005 – 31 December 2018.

- **DailyPrecip_GZ_simple_05_18.csv**  
  Daily precipitation (mm), 1 January 2005 – 31 December 2018.

- **WA_giraffe_encounter_histories.csv**  
  Encounter histories are not publicly available due to data governance arrangements and the conservation status of the West African giraffe.  
  Access may be granted upon reasonable request and subject to an appropriate Data Sharing Agreement.

---

### 📂 gee_climate_extraction/

Google Earth Engine (GEE) scripts used to derive climate covariates.

- **ERA5_daily_max_T.js**
- **CHIRPS_daily_precipitation.js**

---

### 📂 spatial_data_for_gee/

- **GZ_simple.geojson**  
  Habitat polygon used for climate extraction in GEE.
