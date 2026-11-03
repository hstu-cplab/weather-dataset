# Weather Dataset

This directory contains the weather-focused dataset for crop recommendation research. It is intended for weather analysis,
environmental pattern exploration, crop-classification experiments, and other
machine-learning workflows using atmospheric and weather-related measurements.

The data was collected by **Cyber Physical Laboratory**
([cplab.org](https://cplab.org)).

### Collection location and method

- **Location:** Northern area of Bangladesh, Dinajpur District
- **Collection device:** Embedded Weather Station

## Contents

| File | Description |
|---|---|
| `weather-dataset.csv` | Weather features and the associated crop label |
| `README.md` | Dataset documentation |

The CSV contains **130,050 records** and **6 columns**. Each record is
represented by one header row followed by one data row.

## Features and target

| Column | Role | Description |
|---|---|---|
| `weather_temperature` | Feature | Weather temperature measurement |
| `weather_humidity` | Feature | Weather humidity measurement |
| `light_intensity` | Feature | Light-intensity measurement |
| `air_pressure` | Feature | Atmospheric air-pressure measurement |
| `rainfall` | Feature | Rainfall measurement |
| `crop` | Target | Crop category associated with the record |

The source dataset does not provide units or a data dictionary for the numeric
columns. Applications should therefore preserve the original values and
confirm the intended units with the data provider before reporting physical
measurements.

## Dataset preparation

This dataset was created by selecting the following columns from the merged
source file:

```text
weather_temperature, weather_humidity, light_intensity, air_pressure, rainfall, crop
```

Rows remain in the same order as the source dataset. The `crop` column is
included so that the file can be used directly for supervised learning. For
feature-only analysis or prediction, use the five weather columns as inputs
and treat `crop` as the label.

## Recommended usage

Typical uses include:

- Summarizing weather conditions associated with different crop categories.
- Exploring relationships between temperature, humidity, light, pressure, and
  rainfall.
- Training and evaluating crop-classification models.
- Building preprocessing pipelines for tabular environmental data.

Before modelling, consider checking class balance, validating numeric
conversion, scaling features where required by the algorithm, and using a
stratified train/test split. Do not use the target column as an input feature.s

## Citation and attribution

When using this dataset, credit the **Cyber Physical Laboratory** and include
the source website: [cplab.org](https://cplab.org).
