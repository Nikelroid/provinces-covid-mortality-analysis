# Iran Provinces Excess Mortality Analysis

![R](https://img.shields.io/badge/R-4.2%2B-blue?logo=r&logoColor=white)
![Tidyverse](https://img.shields.io/badge/Tidyverse-2.0%2B-9A275A?logo=r&logoColor=white)
![Data.table](https://img.shields.io/badge/data.table-1.14%2B-yellow?logo=r&logoColor=white)
![Heatmaply](https://img.shields.io/badge/heatmaply-1.4%2B-orange)
![ggplot2](https://img.shields.io/badge/ggplot2-Data_Viz-blue?logo=r&logoColor=white)

## Description
This project utilizes linear regression models to analyze and estimate excess mortality rates across 31 provinces in Iran. By training models on historical mortality data (pre-1398/2020), the project projects expected baseline death rates and compares them against actual reported figures during the COVID-19 pandemic era. The analysis accounts for seasonal variations, calculates weighted penalties for different age groups, and visualizes the performance of each province using normalized heatmaps.

## Features
* **Linear Regression Modeling:** Fits individual regression models for 31 provinces to forecast baseline mortality.
* **Excess Mortality Calculation:** Computes the deviation between observed and predicted deaths to quantify excess mortality.
* **Age-Stratified Analysis:** Evaluates mortality impact across 21 distinct age groups with specific weighting factors.
* **Visualization:** Generates interactive heatmaps (raw and normalized) to visualize excess death distribution over time and geography.
* **Statistical Evaluation:** Performs t-tests and calculates performance factors to identify provinces with the best and worst outcomes.

## Installation

### Prerequisites
* [R](https://www.r-project.org/) (Version 4.0 or higher recommended)
* [RStudio](https://posit.co/download/rstudio-desktop/) (Optional, but recommended)

### Setup
1.  Clone this repository:
    ```bash
    git clone [https://github.com/your-username/regression-hw1.git](https://github.com/your-username/regression-hw1.git)
    ```
2.  Open the project in RStudio or your preferred R environment.
3.  Install the required dependencies by running the following command in the R console:
    ```r
    install.packages(c("data.table", "ggplot2", "tidyverse", "heatmaply"))
    ```

## Usage

1.  **Prepare Data:** Ensure the dataset `iranprovs_mortality_monthly.csv` is available.
    * *Note:* You may need to update the file path in `HW1-R.Rmd` (line 17) or `HW1-R.R` to match your local directory structure:
        ```r
        mortality = fread("./path/to/iranprovs_mortality_monthly.csv", encoding="UTF-8")
        ```
2.  **Run the Analysis:**
    * Open `HW1-R.Rmd` and "Knit" the file to generate a full HTML report with visualizations.
    * Alternatively, run the script `HW1-R.R` line-by-line to execute the logic interactively.
3.  **View Results:**
    * The script will generate plots for regression fits.
    * Heatmaps will display excess mortality (visualized in the Viewer pane or output HTML).
    * Console output will list the "Best" and "Worst" performing provinces based on the calculated mortality factors.

## Contributing
Contributions are welcome! Please follow these steps:
1.  Fork the repository.
2.  Create a feature branch (`git checkout -b feature/NewFeature`).
3.  Commit your changes (`git commit -m 'Add some NewFeature'`).
4.  Push to the branch (`git push origin feature/NewFeature`).
5.  Open a Pull Request.

## License
This project is open-source and available under the [MIT License](LICENSE).

## Contact
For questions or support, please contact **Nima Kelidari** or open an issue in this repository.
````t
