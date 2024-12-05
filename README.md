### **# Synthetic Time Series Anomaly Detection**:  
This repository contains a Python-based implementation for generating synthetic multivariate time series data, performing anomaly detection, and visualizing results. The synthetic data includes hardware monitoring metrics such as CPU temperature, usage, memory usage, battery levels, and CPU power, with random anomalies introduced. The data is generated using Python libraries like `wmi`, `psutil`, and `pandas`. Anomaly detection is performed using the Isolation Forest algorithm. The project is designed to generate large amounts of data (1GB+) for testing machine learning models, making it ideal for tasks such as anomaly detection, system monitoring, and performance evaluation. This project generates synthetic multivariate time series data simulating hardware metrics such as CPU temperature, usage, memory usage, and battery levels. Anomalies are introduced randomly into the data, and an anomaly detection model is applied using the Isolation Forest algorithm. The project demonstrates how to generate large-scale time series data for testing anomaly detection models. The data is saved as a CSV file and can be used for further analysis or training machine learning models.

## Requirements
- Python 3.x
- `psutil` - for system and hardware monitoring
- `wmi` - for fetching Windows hardware sensor data (only works on Windows)
- `pandas` - for data manipulation
- `sklearn` - for machine learning algorithms (Isolation Forest)
- `matplotlib` - for data visualization

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/synthetic-time-series-anomaly-detection.git
   cd synthetic-time-series-anomaly-detection
   ```

2. **Create a Virtual Environment** (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use venv\Scripts\activate
   ```

3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **For Windows Users**:  
   If you're using `wmi` to get system sensor data, make sure you have `pywin32` installed:
   ```bash
   pip install pywin32
   ```

## Usage

1. **Generate Data**:  
   You can run the provided Python code (found in `data_generation.ipynb`) to start generating synthetic data. This code will collect hardware metrics for a specified duration and sampling rate, introducing random anomalies.
   
2. **Anomaly Detection**:  
   Once the data is generated, the `anomaly_detection.ipynb` notebook applies the Isolation Forest algorithm to detect anomalies in the time series data.

3. **Visualization**:  
   After detecting anomalies, the results are visualized using `matplotlib` to highlight anomalies in time series plots.

## File Structure

```
.
├── data_generation.ipynb       # Jupyter notebook for data generation
├── anomaly_detection.ipynb     # Jupyter notebook for anomaly detection
├── requirements.txt            # Project dependencies
├── hardware_monitor_data.csv   # Generated time series data (generated during runtime)
├── README.md                   # Project overview and instructions
└── LICENSE                     # License information (optional)
```

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements
- `wmi` for hardware monitoring on Windows.
- `psutil` for system performance metrics.
- `sklearn` for machine learning models.
```

---

### **Notes**:
- Replace `yourusername` in the GitHub URL with your actual GitHub username.
- Ensure that the `requirements.txt` file is created with the necessary dependencies (e.g., `psutil`, `wmi`, `pandas`, `scikit-learn`, `matplotlib`).

### **requirements.txt Example**:
```txt
psutil
wmi
pandas
scikit-learn
matplotlib
pywin32
```
