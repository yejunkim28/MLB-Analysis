# MLB Batting Analytics: Left vs Right-Handed Batter Analysis

## Project Overview

This project investigates the impact of a baseball player's batting side on their hitting success. The primary research question examines whether left-handed batters have a higher overall batting average than right-handed batters using historical MLB data from 2013-2024.

## Research Question

**Do left-handed batters have a higher overall batting average than right-handed batters?**

---

## Project Structure

```
├── Left_Right/                          # Main analysis notebooks
│   ├── 1.hitting_individuals_api.ipynb  # Fetch individual hitter data via API
│   ├── 2.merge.ipynb                    # Merge and consolidate data
│   ├── 3.data_analysis.ipynb            # Core analysis & visualizations
│   ├── all_hitters_historical.csv       # Consolidated hitter data
│   └── data_attack/                     # Processed data by year
│
├── data/                                # Raw data repository
│   ├── 2013-2024/                       # Yearly data folders
│   │   ├── hitters_individual.csv       # Individual hitter statistics
│   │   ├── team_standings.csv           # Team standings data
│   │   └── team_stats.csv               # Aggregate team statistics
│   └── example_data.xlsx                # Sample data reference
│
├── data_collection_outside/             # Data collection scripts
│   ├── hitting_team_scrape.ipynb        # Web scraper for team hitting data
│   └── team_standing_scrape.ipynb       # Web scraper for standings
│
├── preprocessing/                       # Data preparation
│   └── preprocess.ipynb                 # Data cleaning & standardization
│
├── EDA/                                 # Exploratory Data Analysis
│   ├── individual.ipynb                 # Individual hitter EDA
│   └── team_scale.ipynb                 # Team-level EDA
│
├── visualizations/                      # Output visualizations directory
│
├── venv/                                # Python virtual environment
│
├── output.csv                           # Analysis output file
├── output.xlsx                          # Excel output file
└── README.md                            # This file
```

---

## How to Use

### Setup

1. **Create and activate virtual environment:**

   ```bash
   python -m venv venv
   source venv/bin/activate  # macOS/Linux
   # or
   venv\Scripts\activate     # Windows
   ```

2. **Install dependencies:**
   ```bash
   pip install pandas matplotlib seaborn requests jupyter
   ```

### Running the Analysis Pipeline

#### Step 1: Data Collection (Optional - data already included)

- Run `data_collection_outside/hitting_team_scrape.ipynb` to fetch team hitting data
- Run `data_collection_outside/team_standing_scrape.ipynb` to fetch standings

#### Step 2: Data Preprocessing

- Run `preprocessing/preprocess.ipynb` to clean and standardize data

#### Step 3: Main Analysis

- Run `Left_Right/1.hitting_individuals_api.ipynb` to fetch individual hitter data
- Run `Left_Right/2.merge.ipynb` to consolidate all data sources
- Run `Left_Right/3.data_analysis.ipynb` for analysis and visualizations

#### Step 4: Exploratory Analysis (Optional)

- Run `EDA/individual.ipynb` for individual hitter insights
- Run `EDA/team_scale.ipynb` for team-level patterns

---

## Data Sources

### Raw Data

- **Years Covered:** 2013-2024
- **Data Types:**
  - Individual hitter statistics (batting average, hits, at-bats, home runs, strikeouts, etc.)
  - Team standings and aggregate statistics
  - Batting side information (Left, Right, Switch)

### Data Files

- `data/[YEAR]/hitters_individual.csv` - Individual player stats by year
- `data/[YEAR]/team_standings.csv` - Team standings data
- `data/[YEAR]/team_stats.csv` - Aggregate team statistics
- `Left_Right/all_hitters_historical.csv` - Consolidated historical dataset

---

## Key Metrics Analyzed

- **Batting Average (avg):** Primary success metric
- **Hits:** Total successful hits
- **At-Bats:** Total at-bats
- **Home Runs:** Long-distance hits
- **Strike-Outs:** Failed at-bats
- **Games Played:** Player availability
- **Batting Side:** Left, Right, or Switch hitter

---

## Analysis Output

The main analysis notebook (`Left_Right/3.data_analysis.ipynb`) generates:

- Distribution comparisons between left and right-handed batters
- Trend analysis across seasons (2013-2024)
- Statistical summary tables
- Visualizations saved to `visualizations/` directory
- Consolidated results in `output.csv` and `output.xlsx`

---

## Key Findings

The analysis examines:

1. Mean batting average by batting side
2. Distribution of batting performance
3. Seasonal trends and changes over time
4. Player-level and aggregate-level comparisons
5. Statistical significance of differences

---

## Dependencies

- Python 3.7+
- pandas
- matplotlib
- seaborn
- jupyter
- numpy (implied by pandas)
- requests (for data collection)

Install all at once:

```bash
pip install -r requirements.txt
```

---

## Notes

- Data spans 2013-2024 MLB seasons
- Analysis focuses on players with sufficient at-bat records
- Switch hitters may be analyzed separately due to different hitting patterns
- Historical data has been cleaned and standardized for consistency

---

## Questions?

For more details about the research question and methodology, see the markdown sections in `Left_Right/3.data_analysis.ipynb`.
# MLB_analysis
