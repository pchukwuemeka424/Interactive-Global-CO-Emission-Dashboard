# 🌍 Interactive Global CO₂ Emission Dashboard

This project is an **interactive dashboard** built with [Streamlit](https://streamlit.io/) and [Plotly](https://plotly.com/python/) to visualize **global CO₂ emissions** using synthetic data. It allows users to explore trends across countries, continents, and time.

## 🚀 Features

- 🎚️ Year range filter (1990–2024)
- 🌎 Filter by country or continent
- 📊 Interactive line and bar charts
- 📈 Summary metrics: total, average, top emitter
- 📥 Download filtered data as CSV
- ⚡ Fast, lightweight, and fully responsive UI

## 🧪 Dataset

- `synthetic_co2_emissions.csv` is a generated dataset simulating CO₂ emissions from 10 countries across 5 continents between 1990 and 2024.
- Emissions are in **megatonnes (Mt)**.

## 🗃️ File Structure

interactive_global_co2_dashboard/
├── app.py # Main Streamlit app
├── data/
│ └── synthetic_co2_emissions.csv # Synthetic CO₂ data
└── README.md


## 🛠️ Requirements

Install dependencies:

```bash
pip install streamlit pandas plotly

▶️ How to Run

Launch the dashboard with:

streamlit run app.py

This will open a browser window where you can interact with the dashboard.
📂 Data Generation (Optional)

You can regenerate the synthetic dataset using the script below:

import pandas as pd
import numpy as np

np.random.seed(42)
years = list(range(1990, 2025))
countries = ['USA', 'China', 'India', 'Germany', 'Brazil', 'Nigeria', 'Canada', 'Australia', 'UK', 'Russia']
continents = {
    'USA': 'North America', 'China': 'Asia', 'India': 'Asia', 'Germany': 'Europe', 'Brazil': 'South America',
    'Nigeria': 'Africa', 'Canada': 'North America', 'Australia': 'Oceania', 'UK': 'Europe', 'Russia': 'Europe'
}

data = []
for country in countries:
    for year in years:
        co2 = np.random.normal(loc=500, scale=100)
        data.append([year, country, continents[country], max(co2, 50)])

df = pd.DataFrame(data, columns=['Year', 'Country', 'Continent', 'CO2_Emissions_Mt'])
df.to_csv('data/synthetic_co2_emissions.csv', index=False)

📄 License

This project is open-source and free to use under the MIT License.
✨ Created by: [Your Name]

For research, teaching, or demonstration purposes.


Would you like me to generate this as a downloadable `README.md` file?

