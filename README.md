# Detroit Tigers Home Run Predictor

The 2025 Detroit Tigers finished with a record of 87-75, finishing 2nd place in the AL Central and making it to the American League Divisional Series, where they lost in Game 5 to the Seattle Mariners. The Detroit Tigers ranked the 7th youngest across the MLB in Batters' Average Age, which is weighted based on the at bats and games played of each batter. Despite being a relatively young squad, the Detroit Tigers finished in the top 10 of total home runs. With much of the roster being so young and under contract for the upcoming 2026 season, there is well-warranted buzz around the organization. This project attempts to rework a project from 2023 by incorporating more nuanced data science techniques to achieve more accurate results.


## Overview

This project uses data obtained from the MLB's Baseball Savant website, containing a wide variety of an individual player's batting analytics. The project explores just how accurate a machine learning approach can predict a singular player performance metric. 


## Data 

The raw data used in this project can be found in the `data/raw` folder. In the notebook, this path is stored as:

```python
raw_data = folder_path + "data/raw/"
```


## Environment Setup

### Installing uv (If not Already Installed)

MacOS/Linux(or the WSL terminal on Windows):

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

Windows (Powershell):

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

Verify Installation

```bash
uv --version
```

### Once Installed ...

1. Initialize a `uv` Environment

```bash
uv init
```

Feel free to remove the `main.py` file created during `uv` init

```bash
rm main.py
```

2. Change the Python Requirement

Open `pyproject.toml`

```bash
vim pyproject.toml
```

Set `requires-python` = ">=3.11, <3.13"

3. Add Dependencies

In this project we use the following libraries
 - matplotlib
 - numpy
 - pandas
 - scikit-learn
 - tensorflow
 - ipykernel (if you want to run notebook)

```bash
uv add matplotlib numpy pandas scikit-learn tensorflow ipykernel
```


## Reproducing a Result

### Running the Notebooks

Open the notebook in VSCode and click kernel on the top right. Select the Python interpreter associated with this directory. Also, you will need to change the `folder_path` variable at the top of the notebook

1. Open the `data.ipynb` file and run its contents

**What will Generate:**
 - Home run distribution figures
 - Train/Val/Test indices arrays

*note:* the imputation portion of the notebook is computationally expensive, so it will need time to run (~ 5-10 minutes)

2. Open the `model.ipynb` file and run its contents

**What will Generate**
 - Tables with the model's predictions
 - A residual plot of the predictions for the Validation Set

### Home Run Distributions

**Home Run Histogram:** run cell `11` from the `data.ipynb` notebook
**Home Run Boxplot:** run cell `12` from the `data.ipynb` notebook to reproduce the Box Plot. 

*note:* these figures is saved in the `results/figures` folder of the project directory.

### Home Run Predictions

**Validation Set Predictions Table:** run cell `8` from the `model.ipynb` notebook
**Detroit Tigers Predictions Table:** run cell `10` from the `model.ipynb` notebook

*note:* these tables is saved in the `results/predictions` folder of the project directory

**Validation Set Residuals Plot:** run cell `9` from the `model.ipynb` notebook

*note:* this figure is saved in the `results/figures` folder of the project directory


## Troubleshooting

**Python Requirements:** `3.11` or `3.12`
**Dependency Conflicts:** TensorFlow does work with Python versions 3.9 and 3.10; however, numpy has some conflict dependencies. So keep in mind if you switch Python versions to 3.9 or 3.10 that you will have to use a different version of nummpy