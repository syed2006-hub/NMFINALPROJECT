# 🧠 Structural Health Monitoring System:

A desktop application that reads strain and vibration data from sensors, analyzes it using Google Gemini AI, and alerts the user about potential structural issues through visual and audio cues.

---

## 🚀 Features:

- 📂 Loads sensor data from a `.csv` file
- 🤖 Uses Gemini AI to analyze strain and vibration values
- 🔊 Plays alert sounds based on severity (critical/moderate)
- 💬 Displays real-time system status and alerts
- 🖥️ Built with a user-friendly Tkinter GUI
- 🧵 Uses threading to maintain GUI responsiveness during API analysis

---

## 🛠️ Technology Used:

- **Python 3.x**
- **Tkinter** – for GUI development
- **Google Gemini AI API** – for intelligent analysis
- **CSV** – for reading sensor input
- **`dotenv`** – for secure API key management
- **`requests`** – for making API calls
- **`pygame` & `winsound`** – for audio alerts

---

## ⚙️ How It Works:

1. Sensor data is read from `sensor_data.csv`.
2. Each record contains `strain` and `vibration` values.
3. These values are sent to Gemini with predefined rules to interpret the structural condition.
4. Based on the AI’s response:
   - **Critical stress** → Plays emergency MP3 alarm
   - **Moderate stress** → Emits a beep
   - **Normal operation** → Displays confirmation
5. The app iterates through the dataset and presents a live system status.

---

## 📊 Data Collection:

- The data used for this demo is simulated and stored in `sensor_data.csv`.
- Each row in the dataset includes:
  - `strain`: a float value
  - `vibration`: a float value
## 🎯 Objective : 
To assist infrastructure inspectors and engineers in real-time monitoring and decision-making by leveraging AI for structural integrity assessment.

## 🕹️ Controls:
▶ Start Monitoring – Begins analysis from the first record

⏹ Stop Monitoring – Pauses monitoring at the current index


## 📈 Output Explanation :
### Sensor Values	AI Response	Alert:
- **Strain > 0.8 & Vibration > 0.2	"Critical stress"	🚨 Emergency alarm**
- **Strain > 0.5 & Vibration > 0.05	"Moderate stress"	⚠️ Warning beep**
- **Else	"Normal operation"	✅ Safe status**

Example:

```csv
strain,vibration
0.3,0.04
0.7,0.1
0.9,0.25

