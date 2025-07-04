# Rain Prediction Using Logistic Regression and Real-Time Weather Data

This project uses a Logistic Regression machine learning model to predict **whether it will rain** in a given city, based on **real-time weather data**. The model is trained on historical weather observations and uses features like temperature, humidity, wind speed, and cloud cover.

---

## Features

- Trained logistic regression model with 98%+ accuracy  
- Real-time weather data using OpenWeatherMap API  
- Encoded city and weather conditions  
- Predicts rain and shows probability (%)  
- Trained on April–June 2024 Maharashtra weather data  

---

## Project Structure

```
rain-prediction-ml/
├── shuffled_weather_data.csv       # Historical dataset
├── logistic_model.pkl              # Trained ML model
├── model_training.ipynb            # Jupyter notebook for training
├── real_time_prediction.py         # Script to fetch live data & predict rain
├── requirements.txt                # Required Python packages
└── README.md                       # Project documentation
```

---

## Dataset Overview

**File**: `shuffled_weather_data.csv`  
**Cities**: Mumbai, Pune, Thane, Bhayander, Mahabaleshwar  
**Total Records**: ~450 (April – June 2024)

### Key Features:
- `temp` – Temperature (°C)  
- `humidity` – Humidity (%)  
- `windgust`, `windspeed` – Wind speeds (m/s)  
- `sealevelpressure` – Air pressure (hPa)  
- `cloudcover` – Cloud coverage (%)  
- `conditions` – Text description (e.g., Clear, Rain)  
- `city`, `city_encoded`, `conditions_encoded` – Encoded inputs  
- `will_rain` – Target (1 = Rain, 0 = No Rain)

---

## Model Details

- **Algorithm**: Logistic Regression  
- **Framework**: scikit-learn  
- **Accuracy**: ~98.1% on test data  
- **Target**: `will_rain` (binary classification)

---

## Real-Time Rain Prediction

### Example:

```
Location: (lat , long) @ 2025-06-30 18:45 IST  
Input to Model: [27.62, 81, 10.97, 8.2, 1005, 100, 1, 1]  
Probability of rain (Logistic Regression): 6.06%
```

### How it works:
1. Fetches current weather using OpenWeatherMap API
2. Encodes city and conditions
3. Feeds data to trained ML model
4. Prints rain prediction & probability

---

## How to Run

1. **Install requirements**
```bash
pip install -r requirements.txt
```

2. **Run the real-time prediction script**
```bash
python real_time_prediction.py
```

3. *(Optional)* Retrain the model using the notebook
```bash
jupyter notebook model_training.ipynb
```

---

## 🔧 Tech Stack

- Python
- Pandas, NumPy
- scikit-learn
- OpenWeatherMap API
- Visual Crossing (for historical weather data)

---

## Future Enhancements

- Predict rain for specific future time (e.g. 6 AM tomorrow)
- Add more cities or global data
- Deploy using Streamlit or Flask
- Try other models (Random Forest, XGBoost)

---

## Contact

**Author**: [Prithvi Yadav]  

---

> Weather predictions aren't always perfect, but machine learning helps us get closer! 
