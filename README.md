# VukelicEtAl2026_NigerGiraffeCMR_TempAndPrecip
This repository contains supporting data and R scripts for the capture-mark-recapture (CMR) analyses used to assess the effects of temperature and precipitation on apparent survival of the West African giraffe in the Giraffe Zone (2005–2018), implemented using multistate mark-recapture (MSMR) models. It also includes the Google Earth Engine (GEE) scripts used to extract the climate covariates and the digitised habitat polygon (GeoJSON; derived from O’Connor et al., 2019) required to reproduce the climate data extraction workflow.

Repository Structure

R/

R scripts used for multistate mark-recapture (MSMR) analyses and goodness-of-fit assessment.

MSMR_temperature_GZ.R
Performs MSMR analysis with temperature as a covariate.
Temperature is defined as the number of days with maximum daily temperature ≥ 35 °C, excluding the December–February period.

GOF_MSMR_temperature.R
Fits and exports a saturated global MSMR model with temperature as a covariate for goodness-of-fit evaluation.

MSMR_precipitation_GZ.R
Performs MSMR analysis with precipitation as a covariate.
Precipitation is defined as total June–July–August (JJA) precipitation (mm).

GOF_MSMR_precipitation.R
Fits and exports a saturated global MSMR model with precipitation as a covariate for goodness-of-fit evaluation.

data_for_R/

Input data used in the R analyses.

DailyMaxTemp_GZ_simple_05_18.csv
Daily maximum temperature (°C), 1 January 2005 – 31 December 2018.
Used in temperature-based MSMR analyses.

DailyPrecip_GZ_simple_05_18.csv
Daily precipitation (mm), 1 January 2005 – 31 December 2018.
Used in precipitation-based MSMR analyses.

WA_giraffe_encounter_histories.csv
Encounter histories used in MSMR analyses are not publicly available due to data governance arrangements and the conservation status of the West African giraffe.
The dataset is collectively owned by the responsible Nigerien authorities and collaborating NGOs.
Access may be granted upon reasonable request and subject to an appropriate Data Sharing Agreement with the responsible institutions.
To request access, contact the corresponding author.

gee_climate_extraction/

Google Earth Engine (GEE) scripts used to derive climate covariates.

ERA5_daily_max_T.js
Extracts daily maximum 2 m air temperature (°C) from the ERA5 reanalysis dataset (ECMWF/ERA5/DAILY) for the defined habitat polygon (1 January 2005 – 31 December 2018).

CHIRPS_daily_precipitation.js
Extracts daily precipitation (mm) from the CHIRPS dataset (UCSB-CHG/CHIRPS/DAILY) for the same polygon and time period.

spatial_data_for_gee/

GZ_simple.geojson
Digitised habitat polygon used in Google Earth Engine for climate data extraction.
