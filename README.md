ESPHome Smart Energy Dashboard

An advanced graphical dashboard for the Sunton ESP32-S3 8048S070 7" display, built with ESPHome + LVGL and integrated with Home Assistant. The project provides a modern, clear, and highly readable interface for monitoring household energy consumption, photovoltaic production, inverter parameters, and environmental data.
✨ Features
Central clock with date, day, and year, synchronized via Home Assistant.

Weather: condition translated into Romanian, outdoor temperature, humidity, and atmospheric pressure.

Indoor rooms: temperature and humidity for two rooms, displayed symmetrically.

Household consumption & photovoltaic production: energy values displayed in large font, with the unit “W” separated below for maximum readability.

Active power: displayed distinctly, updated every 5 seconds.

Inverter temperature: internal temperature value followed by °C, with a subtitle “INVERTER”.

Electrical grid: dedicated section showing voltage (V), current (A), and frequency (Hz), each with one decimal place.

Optimized design: separation of numeric values from units, large fonts for critical data, small fonts for titles and labels.

🛠️ Technologies
ESPHome for integration with Home Assistant and hardware control.

LVGL for graphical rendering on the display.

ESP32-S3 with PSRAM for performance and smooth updates.

Custom fonts (OpenSans, Roboto Bold) with full diacritic support.

⚙️ Data Sources & Home Assistant Entities
Outdoor temperature, humidity, pressure:

Collected from a BME280 sensor integrated via ESPHome.

Entities:

sensor.bme280test_bme280_temperature_2

sensor.bme280test_bme280_humidity_2

sensor.bme280test_bme280_pressure

Indoor room thermometers:

Two Tuya temperature/humidity sensors integrated in Home Assistant.

Entities:

sensor.t_h_sensor_6_homerseklet (Room 1 temperature)

sensor.t_h_sensor_6_paratartalom (Room 1 humidity)

sensor.andras_szoba_temperatura (Room 2 temperature)

sensor.andras_szoba_umiditate (Room 2 humidity)

Household consumption, photovoltaic production, active power, voltage, current, frequency:

Data collected from a Huawei inverter, a Huawei power meter, and a Tuya Local bidirectional energy sensor.

Entities:

sensor.bidirectional_energy_meter_power_b (Household consumption)

sensor.inverter_active_power (Photovoltaic production)

sensor.power_meter_active_power (Active power)

sensor.inverter_internal_temperature (Inverter internal temperature)

sensor.power_meter_tensiune (Grid voltage)

sensor.bidirectional_energy_meter_current_b (Grid current)

sensor.power_meter_frequency (Grid frequency)

Weather condition:

weather.forecast_home


📸 Screenshots

<img width="800" height="480" alt="dashboard_bg" src="https://github.com/user-attachments/assets/39e5d503-3311-40bc-8a5b-1f58e03e3614" />


🎥 Demo Video
A demo video will be available soon on YouTube. 👉 [YouTube link] (to be added after publishing)

📄 License
This project is open-source and distributed under the MIT License.
