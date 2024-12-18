# My repository for the Computer Infrastructure module.
** Author: Myles Henehan

This repository contains my assignment submission for the **Computer Infrastructure** module at ATU. The focus of the assignment is to automate weather data retrieval, process it, and organize the repository structure effectively. 

## Repository Overview

The repository is structured as follows:

```
.
├── .gitignore
├── weather.ipynb          # Jupyter Notebook outlining the assignment steps
├── weather.sh             # Shell script for automating weather data retrieval
├── data/                  # Directory containing downloaded weather data files
│   ├── timestamps/        # Folder containing timestamp-based files
│   └── weather/           # Folder containing downloaded weather data files
├── .github/workflows/     # Directory for GitHub Actions workflow
│   └── weather-data.yml   # GitHub Actions workflow configuration
```

### Files and Directories

1. **`.gitignore`**
   - Ensures unnecessary files are excluded from version control.

2. **`weather.ipynb`**
   - Jupyter Notebook documenting the workflow and steps involved in the assignment, including:
     - Repository structure creation.
     - Use of the `date` command and timestamp formatting.
     - Retrieval of weather data from Met Éireann using `wget`.
     - Script development for automating the retrieval process.
     - Analysis of downloaded weather data (reading and describing the dataset).

3. **`weather.sh`**
   - A shell script to automate the following tasks:
     - Retrieve the current date and format it as a timestamp.
     - Download weather data of the current day from Met Éireann.
     - Save the downloaded weather data using the timestamp as the filename in the `data/weather/` directory.

4. **`data/` Directory**
   - Contains two subdirectories:
     - **`timestamps/`**: Contains files created using formatted timestamps.
     - **`weather/`**: Contains weather data files downloaded from Met Éireann.

5. **`.github/workflows/` Directory**
   - Includes the **`weather-data.yml`** file that defines a GitHub Actions workflow. This workflow automates the execution of the `weather.sh` script.

## Steps Taken in the Assignment

The following tasks were completed as part of the assignment:

1. **Repository Structure Creation**
   - Organized files and directories to follow a clean and logical structure.

2. **Using the `date` Command**
   - Utilized the `date` command to generate formatted timestamps.

3. **Downloading Weather Data**
   - Used `wget` to download weather data for the current day from Met Éireann and save it using the timestamp as the filename.

4. **Automating with a Shell Script**
   - Wrote the `weather.sh` script to automate data retrieval and save it to the `data/weather` directory.

5. **Automating with GitHub Actions**
   - Set up a GitHub Actions workflow to run the `weather.sh` script automatically.

6. **Analyzing Weather Data**
   - Read in one of the downloaded weather data files and performed basic descriptive analysis of the dataset.

## How to Use the Project

### Prerequisites
- Ensure you have `wget` installed on your system.
- GitHub Actions will require repository permissions to run workflows.

### Running the `weather.sh` Script
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```
2. Run the script manually:
   ```bash
   bash weather.sh
   ```
   This will download the current day's weather data and save it in the `data/weather` directory with the timestamp as the filename.

### GitHub Actions Workflow
The **weather-data.yml** workflow automates the `weather.sh` script. Push changes to the repository, and the workflow will trigger automatically to retrieve and store the weather data.

## Example Output
After running the `weather.sh` script, you will find new weather data files in the `data/weather/` directory with filenames based on the current timestamp, e.g.:
```
data/weather/2024-06-17-14-30-00.txt
```

## Future Improvements
- Enhance the `weather.sh` script to include error handling for failed downloads.
- Extend the analysis in `weather.ipynb` to perform data visualization or trend analysis.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---
**Author:** [Your Name]  
**Module:** Computer Infrastructure  
**Institution:** ATU


