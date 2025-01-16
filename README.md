# Detection Buddy Punching

This project focuses on detecting "buddy punching," a form of fraudulent time punching where employees clock in or out for their coworkers. The system uses advanced anomaly detection techniques and clustering algorithms to analyze time-punching patterns and identify irregularities that may indicate fraudulent activity.

## Features

- **Data Preprocessing**:
  - Cleans and organizes the data to remove duplicate or invalid records.
  - Converts timestamp data into a usable numerical format for analysis.

- **Anomaly Detection**:
  - Implements two models for detecting anomalies:
    1. **Isolation Forest**: Identifies outliers based on the isolation of data points in the feature space.
    2. **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)**: Clusters data and labels outliers as noise.

- **Visualization and Insights**:
  - Generates histograms and reports to visualize time-punching patterns.
  - Identifies patterns or clusters of employee activity to detect possible buddy punching cases.

- **Output Management**:
  - Saves processed and analyzed data to an Excel file for easy review.
  - Filters out redundant data to improve the accuracy of detection models.

## How It Works

1. **Data Collection**:
   The system starts with a dataset containing employee IDs ("legajos") and timestamps of their clock-ins/outs.

2. **Preprocessing**:
   - Rows where employees appear consecutively or repeatedly are removed.
   - Timestamps are converted to numerical values for compatibility with machine learning models.

3. **Model Application**:
   - Isolation Forest identifies outliers by isolating them in the feature space.
   - DBSCAN clusters the data and marks noise points as potential anomalies.

4. **Analysis**:
   - The system analyzes and visualizes time differences between punches to find irregular patterns.
   - Groups records by employee sequences to identify common patterns or deviations.

5. **Export Results**:
   - Outputs the analysis to an Excel file for further review.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/detection-buddy-punching.git
   ```
2. Navigate to the project directory:
   ```bash
   cd detection-buddy-punching
   ```
3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. Prepare your dataset and place it in the project directory.
2. Run the main script:
   ```bash
   python main.py
   ```
3. Review the output files for analysis results.

## Dependencies

- Python 3.8+
- pandas
- scikit-learn
- matplotlib
- seaborn

## Future Enhancements

- Implementing a user interface for easier interaction.
- Adding support for real-time detection.
- Integrating other anomaly detection models for comparison.

## Contribution

Contributions are welcome! Feel free to fork this repository and submit pull requests.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

