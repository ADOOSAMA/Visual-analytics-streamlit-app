# VisA - Visual Analytics for Machine Learning

A comprehensive Streamlit-based web application for exploring machine learning model performance through interactive visualizations and analysis tools.

## Overview

VisA provides an intuitive interface for training machine learning models, comparing different approaches, and gaining insights through advanced visual analytics. The application supports multiple datasets, model comparison capabilities, and sophisticated feature importance analysis.

## Features

### Data Management
- **Multiple Dataset Support**: Built-in support for Lucas Organic Carbon dataset, Iris, Wine, and Breast Cancer datasets
- **Custom Data Upload**: Upload your own CSV files for target and training data
- **Data Sampling**: Configurable data percentage usage for experimentation
- **Data Visualization**: Interactive plots for target distribution, feature profiles, and feature distributions

### Machine Learning
- **Random Forest Classifier**: Train models with customizable hyperparameters
- **Model Comparison**: Train and compare multiple models side-by-side
- **Performance Metrics**: Comprehensive evaluation including accuracy, precision, recall, and F1-score
- **Model Export**: Download trained models as pickle files

### Advanced Analytics
- **Error Analysis**: Detailed confusion matrix visualization with class-specific metrics
- **Feature Importance**: Built-in feature importance analysis with interactive charts
- **Interval Importance**: Analyze the impact of feature value intervals on model performance
- **Joint Feature Analysis**: Explore interactions between multiple features using heatmaps

### Interactive Visualizations
- **Dynamic Charts**: Plotly-based interactive visualizations
- **Customizable Views**: Adjustable parameters for different analysis perspectives
- **Real-time Updates**: Live model training and evaluation updates
- **Export Capabilities**: Download trained models and analysis results

## Project Structure

```
visa/
├── app/                          # Main application directory
│   ├── __init__.py              # App module initialization
│   ├── app.py                   # Main Streamlit application
│   ├── config.py                # Configuration settings
│   ├── requirements.txt         # Python dependencies
│   ├── test_app.py              # Unit tests
│   ├── lucas_organic_carbon/    # Lucas dataset files
│   │   ├── target/              # Target data files
│   │   │   └── lucas_organic_carbon_target.csv
│   │   └── training_test/       # Training and test data
│   │       ├── autoencoder_predictions.csv
│   │       └── compressed_data.csv
│   └── services/                # Core functionality modules
│       ├── __init__.py          # Services module initialization
│       ├── data.py              # Data loading and preparation
│       ├── model.py             # Model training and evaluation
│       ├── error_analysis.py    # Error analysis visualizations
│       └── feature_importance.py # Feature importance analysis
├── .streamlit/                  # Streamlit configuration
│   └── config.toml              # Streamlit server settings
├── .git/                        # Git version control
├── .gitignore                   # Git ignore rules
├── LICENSE.txt                  # Project license
└── README.md                    # Project documentation
```

## Installation

### Prerequisites
- Python 3.8 or higher
- pip or conda package manager

### Setup
1. Clone the repository:
```bash
git clone <repository-url>
cd visa
```

2. Install dependencies:
```bash
pip install -r app/requirements.txt
```

3. Run the application:
```bash
streamlit run app/app.py
```

## Usage

### Getting Started
1. **Select Dataset**: Choose from built-in datasets or upload custom CSV files
2. **Configure Model**: Adjust hyperparameters in the sidebar
3. **Train Model**: Click "Update Model" to train with current settings
4. **Explore Results**: Navigate through the three main tabs for comprehensive analysis

### Key Workflows

#### Model Training
- Adjust hyperparameters (max depth, number of estimators, etc.)
- Set data percentage for sampling
- Configure model comparison settings
- Train and evaluate models

#### Data Exploration
- View target distribution and class balances
- Examine feature profiles and distributions
- Analyze raw data structure

#### Error Analysis
- Review overall model performance metrics
- Examine class-specific performance
- Analyze confusion matrices
- Identify problematic prediction patterns

#### Feature Importance
- Explore built-in feature importance rankings
- Analyze interval-based feature importance
- Investigate joint feature interactions
- Visualize feature impact on model performance

## Configuration

### Model Parameters
- **Max Depth**: Maximum tree depth (1-200)
- **Number of Estimators**: Number of trees (1-1000)
- **Min Samples Split**: Minimum samples to split (2-20)
- **Min Samples Leaf**: Minimum samples per leaf (1-20)
- **Max Features**: Feature selection strategy (sqrt, log2)
- **Data Percentage**: Sampling ratio (1-100%)

### Visualization Settings
- **Normalize Confusion Matrix**: Toggle normalized/raw confusion matrix
- **Number of Features**: Control feature importance display
- **Interval Counts**: Configure interval analysis granularity
- **Color Schemes**: Customizable visualization colors

## Datasets

### Built-in Datasets
- **Lucas Organic Carbon**: Soil organic carbon classification with PCA and autoencoder features
- **Iris**: Classic flower species classification
- **Wine**: Wine quality classification
- **Breast Cancer**: Medical diagnosis classification

### Custom Data Format
- **Target CSV**: Single column with class labels
- **Training CSV**: Feature columns with numerical values
- **Index Alignment**: Ensure matching row indices between files

## Technical Details

### Dependencies
- **streamlit**: Web application framework
- **pandas**: Data manipulation and analysis
- **scikit-learn**: Machine learning algorithms
- **plotly**: Interactive visualizations

### Architecture
- **Modular Design**: Separated concerns across service modules
- **Caching**: Optimized data loading and model training
- **Session Management**: Persistent state across user interactions
- **Error Handling**: Comprehensive error management and user feedback

### Performance
- **Data Sampling**: Configurable data size for faster experimentation
- **Caching**: Streamlit caching for improved performance
- **Parallel Processing**: Efficient model training and evaluation

## Development

### Testing
Run the test suite:
```bash
python -m pytest app/test_app.py
```

### Code Structure
- **Services**: Core functionality modules
- **Configuration**: Centralized settings management
- **Error Handling**: Comprehensive logging and user feedback
- **Documentation**: Inline code documentation

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests for new functionality
5. Submit a pull request

