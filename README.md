# IoT Sensor Data Pipeline

## Overview

This project is an IoT Sensor Data Pipeline that collects weather data from the Open-Meteo API, processes it using Apache Kafka, and stores it in a MongoDB database. An interactive dashboard is provided to visualize the collected data.

## Features

- **Data Collection**: Fetches weather data from the Open-Meteo API.
- **Kafka Integration**: Sends the collected data to a Kafka topic for real-time data processing.
- **Data Storage**: Consumes data from Kafka and stores it in MongoDB.
- **Data Visualization**: An interactive dashboard built with Dash and Plotly to visualize the data.

## Project Structure

```plaintext
.
├── app.py                 # Script for fetching weather data and sending it to Kafka
├── kafka_consumer.py      # Kafka consumer script that stores data in MongoDB
├── dashboard.py           # Dash-based interactive dashboard for data visualization
├── requirements.txt       # Project dependencies
├── .gitignore             # Files and directories to be ignored by Git
└── LICENSE                # Project license (MIT)
```

## Setup and Installation

### Prerequisites

- **Python 3.6+**
- **Kafka**
- **MongoDB**

### Installation

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/YourUsername/iot-sensor-data-pipeline.git
   cd iot-sensor-data-pipeline
   ```

2. **Set Up the Virtual Environment**:

   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. **Install Dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

### Configuration

- **Kafka**: Make sure Kafka is running on `localhost:9092`. If not, update the `bootstrap_servers` in `app.py` and `kafka_consumer.py`.
- **MongoDB**: Ensure MongoDB is running on `localhost:27017`. You can change the connection details in `kafka_consumer.py` if needed.

## Usage

### 1. Run the Kafka Producer

Collect weather data and send it to Kafka:

```bash
python app.py
```

### 2. Run the Kafka Consumer

Consume the data from Kafka and store it in MongoDB:

```bash
python kafka_consumer.py
```

### 3. Run the Dashboard

Visualize the collected data in an interactive dashboard:

```bash
python dashboard.py
```

Open your web browser and go to `http://127.0.0.1:8050/` to see the dashboard.

## Visualizations

- **Temperature Data Over Time**: The dashboard provides a line chart showing how the temperature has changed over time, based on the data collected from the Open-Meteo API.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements.

## Acknowledgments

- **[Open-Meteo API](https://open-meteo.com/)**: The source of the weather data used in this project.
- **[Apache Kafka](https://kafka.apache.org/)**: Used for real-time data processing.
- **[MongoDB](https://www.mongodb.com/)**: Used for data storage.
- **[Dash](https://dash.plotly.com/)**: Used for creating the interactive dashboard.

---

### Instructions:

1. Replace `"YourUsername"` with your actual GitHub username in the clone command.
2. Modify any sections or add more details based on your personal contributions or specific configurations.
