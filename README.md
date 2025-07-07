## 🌐 WeatherMLProject

This project demonstrates **two machine learning tasks** using real-time weather data fetched from an API:

---

### ⚙️ Data Source

We use the **OpenWeatherMap API** to fetch current weather data (e.g., temperature, humidity, pressure) for a specific location. The data is then used in two separate machine learning tasks:

---

### 📡 1. Weather Data Collection via API

We used the OpenWeatherMap API in a script to:

- Call the weather API using a personal API key.
- Fetch current weather data for a specific city (e.g., London).
- Extract features like:
  - `temperature`
  - `humidity`
  - `pressure`
  - `weather condition` (as a label)
- Save the collected data to a local CSV file (`weather_data.csv`) for further use.

> 💡 **API used**: `api.openweathermap.org/data/2.5/weather?q=CityName&appid=YOUR_API_KEY`

---

### 📈 2. Temperature Prediction (Regression)

- **Objective**: Predict temperature using other weather features.
- **Features**: Humidity, Pressure
- **Target**: Temperature
- **Model Used**: `LinearRegression`
- **Notebook**: `01_Temperature_Regression.ipynb`

---

### 🧠 3. Weather Condition Classification

- **Objective**: Classify the type of weather (e.g., Clear, Rainy, Cloudy) using numerical weather features.
- **Data Reuse**: We reuse the same `weather_data.csv` generated in the regression task.
- **Preprocessing**:
  - Encode weather conditions (e.g., `Rain`, `Clear`) into numeric labels.
  - Scale the features using `StandardScaler`.
- **Model Used**: `RandomForestClassifier` (with baseline comparison to `LogisticRegression`)
- **Notebook**: `02_Condition_Classification.ipynb`

---

### 📁 Project Structure

