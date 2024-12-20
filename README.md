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
   - Jupyter Notebook documenting the steps involved in the assignment, including:
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

## How to Use the Project

### Prerequisites
- Ensure you have `wget` and `bash` installed on your system.
- Have Python installed to run the Jupyter notebook.

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
The **weather-data.yml** workflow automates the `weather.sh` script.

## Example Output
After running the `weather.sh` script, you will find new weather data files in the `data/weather/` directory with filenames based on the current timestamp, e.g.:
```
data/weather/20240617_143000.json
```

## Future Improvements
- Enhance the `weather.sh` script to include error handling for failed downloads.
- Extend the analysis in `weather.ipynb` to explore more variables.

## References Used

- Chat GPT. (n.d.). ChatGPT. OpenAI. Available at: https://www.openai.com/chatgpt (Accessed: 20 December 2024).
- GeeksforGeeks. (n.d.). Shell Scripting - Define #!/bin/bash. Available at: https://www.geeksforgeeks.org/shell-scripting-define-bin-bash/ (Accessed: 20 December 2024).
- GeeksforGeeks. (n.d.). wget Command in Linux/Unix. Available at: https://www.geeksforgeeks.org/wget-command-in-linux-unix/ (Accessed: 20 December 2024).
- GitHub. (n.d.). Basic writing and formatting syntax. Available at: https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax (Accessed: 20 December 2024).
- GitHub. (n.d.). Cloning a repository. Available at: https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository (Accessed: 20 December 2024).
- GitHub. (n.d.). GitHub Actions Documentation. Available at: https://docs.github.com/en/actions (Accessed: 20 December 2024).
- Met Éireann. (n.d.). Met Éireann - The Irish National Meteorological Service. Available at: https://www.met.ie (Accessed: 20 December 2024).

---
**Author:** Myles Henehan
**Module:** Computer Infrastructure  
**Institution:** Atlantic Technological University


