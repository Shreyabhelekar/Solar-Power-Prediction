
# Solar Power Prediction using Linear Regression

This project predicts solar power output based on weather and solar position data using **Linear Regression**. It uses both raw and engineered features to improve prediction accuracy.

---

## Features

- Predicts **solar power output (in kW)** using:
  - Zenith angle
  - Angle of incidence
  - Shortwave radiation
  - Relative humidity
  - Cloud cover
  - Temperature
- Uses **feature engineering** to create more informative inputs:
  - Radiation × Humidity
  - Radiation / Cloud Cover
  - Temperature / Radiation
  - Angle / Zenith
- Includes **data normalization** using `StandardScaler`
- Allows **interactive user input** for real-time predictions
- Evaluated using:
  - R² Score
  - MAE, MSE, RMSE

---

## Dataset

The dataset contains solar and weather data with the following key columns:

- `zenith`
- `angle_of_incidence`
- `shortwave_radiation_backwards_sfc`
- `relative_humidity_2_m_above_gnd`
- `total_cloud_cover_sfc`
- `temperature_2_m_above_gnd`
- `low_cloud_cover_low_cld_lay`
- `generated_power_kw` *(target)*

**Engineered Features**:
- `radiation_humidity`
- `radiation_zenith`
- `angle_ratio`
- `radiation_efficiency`
- `temp_radiation_ratio`

---

## Technologies Used

- Python
- NumPy, Pandas
- Scikit-learn (LinearRegression, StandardScaler)
- Jupyter Notebook

---

## How to Run

1. Clone or download the repository.

2. Install the required packages:
   ```bash
   pip install numpy pandas scikit-learn

# Installation

Clone the repository: git clone https://github.com/Shreyabhelekar/Solar-Power-Prediction.git

Navigate to the project directory: cd Solar-Power-Prediction

Install required Python libraries: pip install -r requirements.txt

# Results

- Achieved R² score ~0.63
- Used feature engineering to boost prediction quality
- Prevented negative outputs using max(prediction, 0)
