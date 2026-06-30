# MLB Batting Analytics: Left vs Right-Handed Batter Analysis

## Project Overview

This project investigates the impact of a baseball player's batting side on their hitting success. The primary research question examines whether left-handed batters have a higher overall batting average than right-handed batters using historical MLB data from 2013-2024.

## Research Question

**Do left-handed batters have a higher overall batting average than right-handed batters?**

---

## Project Structure

```
├── notebooks/
│   ├── analysis/                        # Main analysis notebooks
│   │   ├── 1.hitting_individuals_api.ipynb
│   │   ├── 2.merge.ipynb
│   │   └── 3.data_analysis.ipynb
│   ├── data_collection/                 # Web scraping notebooks
│   │   ├── hitting_team_scrape.ipynb
│   │   └── team_standing_scrape.ipynb
│   ├── preprocessing/                   # Data cleaning and standardization
│   │   └── preprocess.ipynb
│   ├── eda/                             # Exploratory Data Analysis
│   │   ├── individual.ipynb
│   │   └── team_scale.ipynb
│   └── scratch/                         # One-off notebooks and experiments
│       └── something.ipynb
│
├── data/                                # Raw yearly data
│   ├── 2013/ ... 2024/                  # Season folders
│   │   ├── hitters_individual.csv
│   │   ├── team_standings.csv
│   │   └── team_stats.csv
│   └── processed/                       # Cleaned and merged datasets
│       └── left_right/
│           ├── all_hitters_historical.csv
│           └── data_attack/             # Per-season processed hitter data
│
├── outputs/                             # Final exported reports
│   ├── output.csv
│   └── output.xlsx
│
├── visualizations/                      # Output visualizations directory
├── venv/                                # Python virtual environment
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

- Run `notebooks/data_collection/hitting_team_scrape.ipynb` to fetch team hitting data
- Run `notebooks/data_collection/team_standing_scrape.ipynb` to fetch standings

#### Step 2: Data Preprocessing

- Run `notebooks/preprocessing/preprocess.ipynb` to clean and standardize data

#### Step 3: Main Analysis

- Run `notebooks/analysis/1.hitting_individuals_api.ipynb` to fetch individual hitter data
- Run `notebooks/analysis/2.merge.ipynb` to consolidate all data sources
- Run `notebooks/analysis/3.data_analysis.ipynb` for analysis and visualizations

#### Step 4: Exploratory Analysis (Optional)

- Run `notebooks/eda/individual.ipynb` for individual hitter insights
- Run `notebooks/eda/team_scale.ipynb` for team-level patterns

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
- `data/processed/left_right/all_hitters_historical.csv` - Consolidated historical dataset

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

The main analysis notebook (`notebooks/analysis/3.data_analysis.ipynb`) generates:

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

For more details about the research question and methodology, see the markdown sections in `notebooks/analysis/3.data_analysis.ipynb`.

# MLB_analysis
