# VisA

Visual analytics app for exploring machine learning classifications.   

## Structure

- ```.github/workflows/``` Directory containing GitHub Actions configurations.
-   - `tests.yml` Configuration for running unit tests on commit.
- ```.streamlit/``` Directory containing Streamlit configurations.
  - `config.toml` Configuration file for Streamlit server settings.
- ```app/``` Directory containing Streamlit application files.
  - `lucas_organic_carbon/` Directory containing data files for the Lucas Organic Carbon dataset [[ESDAC](https://esdac.jrc.ec.europa.eu/projects/lucas)].
      - `target/` Directory containing target data files.
      - `training_test/` Directory containing training and test data files.
  - `services/` Directory containing supporting files.
    - `data.py` Contains functions for loading and preparing data.
    - `error_analysis.py` Contains functions for visualizing error analysis.
    - `feature_importance.py` Contains functions for visualizing feature importance.
    - `model.py` Contains functions for training and evaluating the machine learning model.
  - `__init__.py` Initialization file for the app module.
  - `app.py` Main application file for the Streamlit dashboard.
  - `config.py` Configuration file for general settings used in the app.
  - `requirements.txt` Lists the Python packages required to run the app.
  - `test_app.py` Unit tests for checking the app.
- ```check_env.py``` Script to check if the required environment and packages are installed.
- ```environment.yml``` Conda environment configuration file listing the dependencies.
- ```local-install-instructions.md``` Instructions for setting up the project locally.
