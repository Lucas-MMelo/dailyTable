# Daily Weather Data Collector

This project is a simple Python application that collects **weather data from multiple cities** using public APIs and saves the results into a CSV file.

It was developed as part of my studies in data handling and API integration.

---

## Features

* Supports **multiple cities** using latitude and longitude
* Fetches **weather data for the last 7 days**

### Includes:

* Maximum temperature
* Rain (mm)
* Wind speed
* Automatically detects the **city name** using reverse geolocation
* Saves results into a `.csv` file
* Allows user input for additional cities

---

## Technologies Used

* Python
* Pandas
* Requests
* Datetime

---

## APIs Used

* Open-Meteo → Weather data
* OpenStreetMap (Nominatim) → Reverse geolocation (coordinates → city name)

---

## How It Works

1. The script starts with predefined coordinates:

   * Campinas
   * Indaiatuba
   * Hortolândia

2. The user can input additional coordinates.

3. For each location:

   * The weather API is called to get the last 7 days of data
   * The geolocation API is used to retrieve the city name
   * Data is structured into a Pandas DataFrame

4. The data is saved into a CSV file:

   ```
   tableDaily.csv
   ```

---

## How to Run

```bash
pip install pandas requests
python your_script_name.py
```

---

## Output Example

| city       | day        | temp_max | rain | wind |
| ---------- | ---------- | -------- | ---- | ---- |
| Campinas   | 2026-04-15 | 27.8     | 0.0  | 14.9 |
| Indaiatuba | 2026-04-15 | 28.5     | 0.0  | 10.1 |

---

## Notes

* The CSV file is overwritten each time the script runs
* The project uses free APIs, so usage limits may apply
* A custom `User-Agent` is required for the Nominatim API

---

## Author

Lucas de Moura Melo
🔗 https://github.com/Lucas-MMelo
