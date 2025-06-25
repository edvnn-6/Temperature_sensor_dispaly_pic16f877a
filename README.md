# Temperature_sensor_dispaly_pic16f877a

This project reads temperature data from an LM35 analog temperature sensor and displays the result on a 16x2 LCD screen using a PIC microcontroller.

## 👨‍💻 Author
**Edvin Jose Vakaparamban**  
Created on: May 11, 2025

## 🛠 Components Used
- **PIC Microcontroller** (tested with 16F877A / similar)
- **LM35 Temperature Sensor**
- **16x2 LCD Display** (in 4-bit mode)
- **Supporting components**: Resistors, wires, breadboard, etc.

## ⚙️ Features
- Reads analog data from the LM35 sensor via ADC
- Converts the ADC value to Celsius
- Displays temperature in real time on a 16x2 LCD
- Custom degree symbol `°` is displayed using ASCII code `223`

## 🔧 How It Works
1. The ADC module reads voltage from the LM35 sensor.
2. The analog value is converted to a digital value between 0 and 1023.
3. The digital value is then converted to temperature using the formula:
4. The temperature is displayed on the LCD with a one-second refresh rate.

## 📂 File
- **temperator_sensor_dispaly.c**: Complete source code including:
- ADC initialization and reading
- LCD initialization, commands, and data writing
- Main loop to display temperature continuously

## 📌 Pin Configuration
- LCD Data Pins: `RB0 - RB3` (D4-D7)
- LCD Control Pins: `RB4 (EN)`, `RB5 (RS)`
- Analog Input (LM35): `AN0`

## 💡 Notes
- Make sure the microcontroller is running at a frequency of 16 MHz (`_XTAL_FREQ 16000000`)
- Adjust ADCON1 settings if using a different PIC model or analog pin
- The degree symbol `°` is represented by ASCII code `223` in most LCDs


