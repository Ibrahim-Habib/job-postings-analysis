# Job Posting Skills Analysis

This project contains a Python script within a Jupyter Notebook designed to analyze job descriptions from a personal job hunting tracking file. It automates the process of cleaning text data, extracting key technical skills (like Python, AWS, React, etc.), and calculating their frequency to identify the most in-demand technologies in your job search.

## Features

-   **Data Ingestion**: Reads job application data directly from an `.xlsx` file.
-   **Text Preprocessing**: Cleans the raw job description text by:
    -   Lowercasing all text.
    -   Replacing special terms (e.g., `.NET` becomes `dotnet`) to prevent data loss.
    -   Removing punctuation, numbers, and common English stopwords.
-   **Keyword Extraction**: Identifies and counts mentions of a predefined list of technical keywords and their variations (e.g., 'aws' and 'amazon web services' both count as 'aws').
-   **Frequency Analysis**: Calculates how many job postings mention each specific technology.
-   **Export Results**: Saves the final, sorted frequency count of technical skills to a `technical_skills_frequency.csv` file for further analysis or visualization.

## Getting Started

Follow these instructions to set up and run the project on your local machine.

### Prerequisites

-   Python 3.8+
-   Git

### Installation

1.  **Clone the repository:**
    ```sh
    git clone <your-repository-url>
    cd job-hunting-analysis
    ```

2.  **Create and activate a virtual environment:**
    This isolates the project's dependencies from your system's Python.

    *   On Windows:
        ```sh
        python -m venv venv
        .\venv\Scripts\activate
        ```
    *   On macOS/Linux:
        ```sh
        python3 -m venv venv
        source venv/bin/activate
        ```

3.  **Install the required packages:**
    The `requirements.txt` file contains all the necessary libraries.
    ```sh
    pip install -r requirements.txt
    ```

4.  **Download NLTK data:**
    The script uses the NLTK library to remove stopwords. Run the following command to download the necessary data:
    ```sh
    python -c "import nltk; nltk.download('stopwords')"
    ```

## How to Use

1.  **Add your data file:**
    Place your job tracking Excel file in the root directory of the project and name it `Job Hunting Tracking.xlsx`.

    *Note: The `.gitignore` file is configured to prevent this file from being committed to the repository, keeping your personal data private.*

2.  **Launch Jupyter Notebook:**
    Run the following command in your terminal:
    ```sh
    jupyter notebook
    ```

3.  **Run the analysis:**
    Open the `JobPostingsAnalysis.ipynb` (or your named notebook file) in your browser and run the cells from top to bottom.

## Output

The script will produce two outputs:

1.  A table of technologies and their frequencies will be printed directly in the notebook.
2.  A new file named `technical_skills_frequency.csv` will be created in the project's root directory. This file contains the final results, sorted by frequency in descending order.

### Example Output (`technical_skills_frequency.csv`):

| Technology | Frequency |
| :--------- | :-------- |
| python     | 25        |
| aws        | 18        |
| sql        | 15        |
| react      | 12        |
| ...        | ...       |


