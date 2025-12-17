# 📊 ESPHome Smart Energy Dashboard

An advanced graphical dashboard for the **Sunton ESP32-S3 8048S070** 7" display, built with **ESPHome + LVGL** and integrated with **Home Assistant**.  
The project provides a modern, clear, and highly readable interface for monitoring household energy consumption, photovoltaic production, inverter parameters, and environmental data.

---

## ✨ Features

- **Central clock** with date, day, and year, synchronized via Home Assistant.  
- **Weather**: condition translated into Romanian, outdoor temperature, humidity, and atmospheric pressure.  
- **Indoor rooms**: temperature and humidity for two rooms, displayed symmetrically.  
- **Household consumption & photovoltaic production**: energy values displayed in large font, with the unit “W” separated below for maximum readability.  
- **Active power**: displayed distinctly, updated every 5 seconds.  
- **Inverter temperature**: internal temperature value followed by °C, with a subtitle “INVERTER”.  
- **Electrical grid**: dedicated section showing voltage (V), current (A), and frequency (Hz), each with one decimal place.  
- **Optimized design**: separation of numeric values from units, large fonts for critical data, small fonts for titles and labels.  

---

## 🛠️ Technologies

- **ESPHome** for integration with Home Assistant and hardware control.  
- **LVGL** for graphical rendering on the display.  
- **ESP32-S3 with PSRAM** for performance and smooth updates.  
- **Custom fonts** (OpenSans, Roboto Bold) with full diacritic support.  

---

## ⚙️ Data Sources & Home Assistant Entities

### 🌡 Outdoor environment (via BME280 sensor, integrated with ESPHome)
- `sensor.bme280test_bme280_temperature_2` → Outdoor temperature  
- `sensor.bme280test_bme280_humidity_2` → Outdoor humidity  
- `sensor.bme280test_bme280_pressure` → Atmospheric pressure  

### 🏠 Indoor rooms (Tuya thermometers via Home Assistant)
- `sensor.t_h_sensor_6_homerseklet` → Room 1 temperature  
- `sensor.t_h_sensor_6_paratartalom` → Room 1 humidity  
- `sensor.andras_szoba_temperatura` → Room 2 temperature  
- `sensor.andras_szoba_umiditate` → Room 2 humidity  

### ⚡ Energy data (Huawei inverter, Huawei power meter, Tuya Local bidirectional sensor)
- `sensor.bidirectional_energy_meter_power_b` → Household consumption  
- `sensor.inverter_active_power` → Photovoltaic production  
- `sensor.power_meter_active_power` → Active power  
- `sensor.inverter_internal_temperature` → Inverter internal temperature  
- `sensor.power_meter_tensiune` → Grid voltage  
- `sensor.bidirectional_energy_meter_current_b` → Grid current  
- `sensor.power_meter_frequency` → Grid frequency  

### ☁️ Weather condition
- `weather.forecast_home`

---

## 📂 Fonts

This project uses custom fonts for clarity and diacritic support:
- `OpenSans-Regular.ttf`
- `Roboto-Bold.ttf`

They are included in the `/fonts` folder.  
Copy them into your ESPHome configuration directory before compiling.

---

## 🚀 Installation & Usage

Clone this repository
git clone https://github.com/DaradiciLevente/ESP32-8048S070c-ESPHOME-HOME-ASSISTANT-DASHBOARD.git

Copy the YAML configuration files into your ESPHome setup
Place the fonts (OpenSans-Regular.ttf, Roboto-Bold.ttf) from the /fonts folder into your ESPHome directory
Flash the firmware to the Sunton ESP32-S3 8048S070 board
Ensure all Home Assistant entities listed above are available

---

## 📸 Screenshots

![IMG_20251216_213325006_HDR](https://github.com/user-attachments/assets/f508c554-762a-4351-b67d-01d055618fc6)

---

## 🎥 Demo Video

A demo video will be available soon on YouTube.  
👉 [[YouTube link](https://youtube.com/shorts/c-pyQ2oMEn4)] (to be added after publishing)

https://youtube.com/shorts/c-pyQ2oMEn4

Check out the demo video here: [YouTube Short](https://www.youtube.com/shorts/c-pyQ2oMEn4)

---

## 📄 License

This project is open-source and distributed under the **MIT License**.  
See the [LICENSE](LICENSE) file for details.
