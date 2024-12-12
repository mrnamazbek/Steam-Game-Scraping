# Project Three: Comprehensive Steam Games Data Analysis

## **Overview**
This project is designed to scrape, clean, analyze, and visualize Steam games data to extract meaningful insights about trends, game popularity, monetization, and localization. The project combines web scraping, data wrangling, and advanced visualizations.

## **Project Structure**
The project directory is organized as follows:

```
├── analyzing
│   ├── analyzing_and_cleaning.ipynb      # Notebook for data cleaning and analysis
│   └── working columns                  # File detailing the final selected columns
├── scraping
│   ├── ConvertToCSV.py                  # Script to convert JSON to CSV
│   ├── ParseExample.py                  # Example of parsing Steam data
│   ├── SteamGamesScraper.py             # Main script for scraping Steam data
│   ├── applist.json                     # List of app IDs scraped from Steam
│   ├── discarted.json                   # Scraped data discarded due to errors
│   ├── games.json                       # Raw scraped data
│   ├── notreleased.json                 # Data on unreleased games
│   └── starting_guide                   # Instructions for setting up scraping
├── visualizationing
│   ├── 3d_chart.html                    # Interactive 3D bar chart visualization
│   ├── cleaned_data.csv                 # Cleaned dataset for visualization
│   ├── visualization.ipynb              # Main visualization notebook
│   └── visualization2.ipynb             # Additional visualizations
```

## **Steps in the Project**

### **1. Scraping Data**
#### **Objective**
Scrape data about games from Steam to create a raw dataset for analysis.

#### **Key Script**
- `SteamGamesScraper.py`: This script uses Steam’s API to extract game data including metadata such as name, release date, price, genres, reviews, and more.

#### **Output**
- `games.json`: The raw dataset containing details about all scraped games.
- `discarted.json` & `notreleased.json`: Files to track discarded and unreleased game data.

### **2. Converting and Cleaning Data**
#### **Objective**
Convert raw JSON data into a structured format (CSV) and clean it for analysis.

#### **Steps**
1. **Conversion**:
   - Use `ConvertToCSV.py` to transform `games.json` into `games.csv`.
2. **Cleaning**:
   - Handle missing values, redundant columns, and incorrect data formats in `analyzing_and_cleaning.ipynb`.
   - Filter out unnecessary columns based on relevance (see `working columns`).

#### **Output**
- `cleaned_data.csv`: The cleaned dataset ready for analysis and visualization.

### **3. Data Analysis**
#### **Objective**
Gain insights about trends, monetization, and popularity.

#### **Key Techniques**
1. **Data Wrangling**:
   - Extracting release years, splitting genres, and calculating statistical summaries.
2. **Advanced Analysis**:
   - Correlation between price and reviews.
   - Trends in game releases over time.
   - Popular genres and their reception.

#### **Notebook**
- `analyzing_and_cleaning.ipynb`: Performs detailed analysis using Pandas and Numpy.

### **4. Visualization**
#### **Objective**
Create visual representations to highlight patterns and insights.

#### **Visualizations**
1. **Time Trends**:
   - Line chart of game releases over years using Matplotlib and Seaborn.
2. **Correlations**:
   - Heatmap of numerical correlations (e.g., price vs. reviews).
3. **Popular Genres**:
   - Bar charts and boxplots to show distribution and popularity of genres.
4. **Interactive 3D Charts**:
   - A 3D bar chart for genre popularity using Plotly (saved as `3d_chart.html`).

#### **Notebooks**
- `visualization.ipynb` and `visualization2.ipynb` for creating static and interactive visualizations.

### **5. Final Outputs**
#### **Key Deliverables**
- Cleaned dataset: `cleaned_data.csv`
- Interactive visualizations: `3d_chart.html`
- Analysis notebooks: `analyzing_and_cleaning.ipynb`, `visualization.ipynb`

## **How to Use**

### **Prerequisites**
1. Install Python and Jupyter Notebook.
2. Install necessary libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn plotly requests
   ```

### **Execution Steps**
1. **Scrape Data**:
   Run `SteamGamesScraper.py` to scrape raw data.
   ```bash
   python scraping/SteamGamesScraper.py
   ```
2. **Convert Data**:
   Convert JSON to CSV using `ConvertToCSV.py`.
   ```bash
   python scraping/ConvertToCSV.py
   ```
3. **Clean and Analyze Data**:
   Open and execute `analyzing_and_cleaning.ipynb`.
4. **Visualize Data**:
   Open and execute `visualization.ipynb` or `visualization2.ipynb`.

### **Advanced Use**
- Modify `SteamGamesScraper.py` to customize scraping parameters.
- Explore interactive charts in `3d_chart.html` for deeper insights.

## **Conclusion**
This project demonstrates the end-to-end process of data scraping, cleaning, analysis, and visualization. By focusing on Steam games data, we uncover trends in the gaming industry and deliver actionable insights using advanced visualization techniques.

For questions or contributions, feel free to reach out!

