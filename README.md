# Cryptocurrency Clustering and Stochastic Modeling Analysis

## 📊 Research Overview

This repository presents a comprehensive analysis of cryptocurrency market behavior through spectral clustering and stochastic modeling. The study examines 100 major cryptocurrencies to identify distinct behavioral patterns and model their price dynamics using appropriate stochastic processes.

## 🎯 Research Objectives

1. Identify and categorize cryptocurrencies with similar market behavior patterns
2. Select representative cryptocurrencies for each behavioral group
3. Characterize the statistical properties of cryptocurrency log-returns
4. Determine the most appropriate stochastic models for each group

## 📋 Methodology

### Step 1: Data Collection
- **Data Source**: Binance Exchange API
- **Dataset**: OHLC (Open, High, Low, Close) price data
- **Sample**: Top 100 cryptocurrencies by market capitalization (2019)
- **Time Period**: [Specify your date range]
- **Frequency**: Daily data

### Step 2: Spectral Clustering
- **Algorithm**: Spectral clustering based on return correlation structure
- **Number of Clusters**: 3 groups
- **Features Used**: Log-return time series
- **Similarity Metric**: Correlation-based similarity matrix
- **Purpose**: Categorize cryptocurrencies into distinct behavioral groups

### Step 3: Representative Selection
- **Method**: [Describe your selection criteria]
  - Option 1: Cryptocurrency closest to cluster centroid
  - Option 2: Highest liquidity/market cap within cluster
  - Option 3: Most representative correlation pattern
- **Result**: 3 representative cryptocurrencies (one per cluster)

### Step 4: Log-Return Distribution Analysis
For each representative cryptocurrency, we analyzed:
- **Descriptive Statistics**: Mean, variance, skewness, kurtosis
- **Normality Tests**: Jarque-Bera, Shapiro-Wilk, Kolmogorov-Smirnov
- **Tail Behavior**: Extreme value analysis, tail index estimation
- **Temporal Properties**: Autocorrelation, volatility clustering

### Step 5: Stochastic Model Fitting
Candidate models evaluated:
- **Geometric Brownian Motion (GBM)**: Baseline model with constant volatility
- **Jump Diffusion Model**: Captures sudden price jumps
- **GARCH Models**: Accounts for volatility clustering
- **Lévy Processes**: Heavy-tailed distributions
- **Student's t-Distribution**: Alternative for non-normal returns

**Model Selection Criteria**:
- Log-likelihood
- Akaike Information Criterion (AIC)
- Bayesian Information Criterion (BIC)
- Goodness-of-fit tests

## 📁 Repository Structure

```
cryptocurrency-clustering-analysis/
│
├── README.md                          # Project overview and documentation
├── requirements.txt                   # Python dependencies
├── .gitignore                        # Git ignore rules
│
├── data/                             # Data directory
│   ├── raw/                          # Raw OHLC data from Binance
│   │   ├── BTC_USDT.csv
│   │   ├── ETH_USDT.csv
│   │   └── ...
│   ├── processed/                    # Cleaned and processed data
│   │   ├── log_returns.csv
│   │   └── correlation_matrix.csv
│   └── top_100_cryptos_2019.csv      # List of cryptocurrencies analyzed
│
├── notebooks/                        # Jupyter notebooks for analysis
│   ├── 01_data_collection.ipynb      # Data retrieval and preprocessing
│   ├── 02_spectral_clustering.ipynb  # Clustering analysis
│   ├── 03_representative_selection.ipynb  # Representative selection
│   ├── 04_distribution_analysis.ipynb     # Statistical analysis
│   ├── 05_stochastic_modeling.ipynb       # Model fitting
│   └── 06_results_visualization.ipynb     # Final visualizations
│
├── src/                              # Source code (your existing code)
│   ├── __init__.py
│   ├── data_collection.py            # Data retrieval functions
│   ├── clustering.py                 # Spectral clustering implementation
│   ├── distribution_analysis.py      # Statistical analysis tools
│   ├── stochastic_models.py          # Model fitting functions
│   └── utils.py                      # Helper functions
│
├── results/                          # Analysis outputs
│   ├── figures/                      # Visualizations
│   │   ├── correlation_heatmap.png
│   │   ├── cluster_dendrogram.png
│   │   ├── representatives_returns.png
│   │   └── model_comparison.png
│   ├── tables/                       # Summary tables
│   │   ├── cluster_assignments.csv
│   │   ├── statistics_summary.csv
│   │   └── model_parameters.csv
│   └── clustering_results.pkl        # Saved clustering results
│
├── tests/                            # Unit tests (optional)
│   └── test_clustering.py
│
└── docs/                             # Additional documentation
    ├── methodology.md                # Detailed methodology
    ├── data_description.md           # Data documentation
    └── references.md                 # Academic references
```

## 🔑 Key Findings

### Cluster Characteristics

**Cluster 1: [Name/Description]**
- Representative: [e.g., Bitcoin (BTC)]
- Characteristics: [e.g., Lower volatility, established cryptocurrencies]
- Number of members: [X cryptocurrencies]
- Best-fit model: [e.g., Geometric Brownian Motion]

**Cluster 2: [Name/Description]**
- Representative: [e.g., Ethereum (ETH)]
- Characteristics: [e.g., Moderate volatility, smart contract platforms]
- Number of members: [X cryptocurrencies]
- Best-fit model: [e.g., Jump Diffusion]

**Cluster 3: [Name/Description]**
- Representative: [e.g., [Altcoin name]]
- Characteristics: [e.g., High volatility, smaller market cap]
- Number of members: [X cryptocurrencies]
- Best-fit model: [e.g., GARCH(1,1)]

### Statistical Insights

- **Distribution Properties**: [e.g., All representatives show non-normal distributions with fat tails]
- **Volatility Patterns**: [e.g., Evidence of volatility clustering across all clusters]
- **Model Performance**: [e.g., Jump diffusion models outperform GBM for all representatives]

## 🚀 Getting Started

### Prerequisites

```bash
Python >= 3.8
```

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/cryptocurrency-clustering-analysis.git
cd cryptocurrency-clustering-analysis
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

### Usage

Run the notebooks in sequence:

```bash
jupyter notebook notebooks/01_data_collection.ipynb
```

Or run the complete pipeline:

```bash
python src/main.py
```

## 📊 Results Preview

[Include 2-3 key visualizations here, such as:]
- Cluster visualization
- Representative log-return distributions
- Model fit comparisons

## 📚 References

1. [Your academic references for spectral clustering]
2. [References for stochastic modeling]
3. [Cryptocurrency market literature]

## 🔬 Future Work

- Extend analysis to more recent time periods (2020-2024)
- Investigate time-varying parameters in stochastic models
- Apply regime-switching models
- Develop trading strategies based on cluster assignments

## 📝 License

[Choose your license: MIT, Apache 2.0, etc.]

## 👤 Author

**[Your Name]**
- GitHub: [@yourusername](https://github.com/yourusername)
- Email: your.email@example.com

## 🙏 Acknowledgments

- [Any acknowledgments]
- Data provided by Binance Exchange
