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

4. Run the Notebook!

Open the notebook is VSCode and click kernel on the top right. Select the Python interpreter associated with this directory and run the notebook!

## Reproducing a Result

