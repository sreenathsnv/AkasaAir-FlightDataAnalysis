# Flight Delay Analysis Pipeline

This repository contains a data analysis pipeline to explore and understand flight delay patterns using Python. The pipeline processes flight data, cleans it, analyzes trends, and generates visualizations of flight delays based on multiple factors like airline and departure time.

## Table of Contents
- [Installation](#installation)
- [Virtual Environment Setup](#virtual-environment-setup)
- [Pipeline Overview](#pipeline-overview)
- [Usage](#usage)
- [Analysis Results](#analysis-results)
- [Dependencies](#dependencies)
- [License](#license)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/sreenathsnv/AkasaAir-FlightDataAnalysis.git
   cd AkasaAir
   ```

2. [Optional] Set up a Python virtual environment to keep dependencies isolated:
   ```bash
   # On macOS/Linux
   python3 -m venv venv
   source venv/bin/activate

   # On Windows
   python -m venv venv
   venv\Scripts\activate
   ```

3. Install the required packages:
   ```bash
   pip install -r requirement.txt
   ```

## Virtual Environment Setup

To create and activate a virtual environment:

macOS/Linux:
```bash
python3 -m venv venv
source venv/bin/activate
```

Windows:
```bash
python -m venv venv
venv\Scripts\activate
```

To deactivate the virtual environment, simply run:
```bash
deactivate
```

## Pipeline Overview

The project consists of the following main steps:

1. **Data Cleaning:**
   - Handling missing values: For DelayMinutes, NaN values are replaced with the mean delay time for the corresponding airline.
   - Duplicate entries: The average delay of duplicate records is calculated, and duplicates are removed.

2. **Inconsistency Check:**
   - Time inconsistencies (e.g., ArrivalTime earlier than DepartureTime on the same day) are checked, and corrections are applied where necessary.

3. **Analysis:**
   - Box plots and scatter plots are used to visualize delays by airlines and departure times.
   - Correlation between departure time and delays is computed to investigate potential relationships.

4. **Visualization:**
   - The pipeline provides detailed visual insights, such as box plots and scatter plots, to help interpret the results.

## Usage

After setting up your environment and installing dependencies, follow these steps:

1. Running the Jupyter Notebook: Start the Jupyter notebook server by running:
   ```bash
   jupyter notebook
   ```

2. Open the notebook file (`Sreenath-V-Akasa-Task1.ipynb`), and execute the cells step by step to perform the data analysis.

## Analysis Results

### Key Findings:
- **Correlation:** The scatter plot shows a positive correlation (0.68) between departure time and delay minutes, indicating that flights departing later in the day tend to experience more delays.
- **Airlines Comparison:** American Airlines has a larger range of delays compared to Delta and United Airlines, based on box plot analysis.

### Recommendations:
- **For Airlines:** Focus on improving flight schedules, especially for later flights, as delays tend to increase during those times.
- **For Passengers:** To minimize the risk of delays, choosing flights earlier in the day may be beneficial.

## Dependencies

All dependencies are listed in the `requirement.txt` file. The key libraries include:
- pandas: For data manipulation and analysis.
- matplotlib, seaborn: For data visualization.
- numpy: For numerical operations.
- scipy: For statistical analysis.
- jupyterlab: To run and execute the notebook.

Install all dependencies using:
```bash
pip install -r requirement.txt
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.