# Sonar: Rock vs Mine Prediction

This workspace contains a Jupyter Notebook that trains a Logistic Regression model to classify sonar signals as either a rock (`R`) or a mine (`M`). The notebook demonstrates data loading, preprocessing, training, evaluation, and a small predictive example.

Files
- [Copy_of_Rock_vs_Mine_Prediction.ipynb](Copy_of_Rock_vs_Mine_Prediction.ipynb) — main notebook
- [data/Copy of sonar data.csv](data/Copy%20of%20sonar%20data.csv) — dataset (CSV, no header)

Requirements
- Python 3.8 or newer
- Packages: `numpy`, `pandas`, `scikit-learn`, `jupyter`

Quick setup

1. (Optional) Create and activate a virtual environment:

```bash
python -m venv .venv
\t# Windows
.venv\Scripts\activate
\t# macOS / Linux
source .venv/bin/activate
```

2. Install dependencies:

```bash
pip install numpy pandas scikit-learn jupyter
```

Running the notebook

1. Start Jupyter in the workspace folder:

```bash
jupyter notebook
```

2. Open [Copy_of_Rock_vs_Mine_Prediction.ipynb](Copy_of_Rock_vs_Mine_Prediction.ipynb) in your browser and run cells in order.

Notes
- The notebook uses an absolute Windows path to load the CSV: `D:\\sonar rock\\data\\Copy of sonar data.csv`. If you move the project, either update that path in the notebook or place the CSV at the same path.
- The predictive example at the end converts an input tuple to a NumPy array, reshapes it, then calls `model.predict(...)` and prints `R` (rock) or `M` (mine).

How to use the predictive example (code excerpt)

```python
input_data_as_numpy_array = np.asarray(input_data)
input_data_reshaped = input_data_as_numpy_array.reshape(1, -1)
prediction = model.predict(input_data_reshaped)
if prediction[0] == 'R':
    print('The object is a Rock')
else:
    print('The object is a Mine')
```

If you'd like, I can also create a `requirements.txt` or convert the notebook into a standalone script for easier command-line use.
