# <img src="https://img.icons8.com/fluency/48/radar.png" width="35" align="top"> Sonar: Rock vs Mine Prediction <img src="https://img.icons8.com/fluency/48/rock.png" width="35" align="top">

This workspace contains a Jupyter Notebook that trains a Logistic Regression model to classify sonar signals as either a rock (R) or a mine (M). The notebook demonstrates data loading, preprocessing, training, evaluation, and a small predictive example.

## <img src="https://img.icons8.com/fluency/48/folder-invoices.png" width="28" align="top"> Files
- <img src="https://img.icons8.com/color/48/jupyter.png" width="18" align="top"> [Copy_of_Rock_vs_Mine_Prediction.ipynb](Copy_of_Rock_vs_Mine_Prediction.ipynb) — main notebook
- <img src="https://img.icons8.com/fluency/48/csv.png" width="18" align="top"> [data/Copy of sonar data.csv](data/Copy%20of%20sonar%20data.csv) — dataset (CSV, no header)

## <img src="https://img.icons8.com/fluency/48/settings.png" width="28" align="top"> Requirements
- Python 3.8 or newer <img src="https://img.icons8.com/color/48/python.png" width="20" align="top">
- Packages: `numpy`, `pandas`, `scikit-learn`, `jupyter` <img src="https://img.icons8.com/fluency/48/package.png" width="20" align="top">

## <img src="https://img.icons8.com/fluency/48/flash-on.png" width="28" align="top"> Quick setup

1. (Optional) Create and activate a virtual environment:

```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS / Linux
source .venv/bin/activate
```

2. Install dependencies:

```bash
pip install numpy pandas scikit-learn jupyter
```

## <img src="https://img.icons8.com/fluency/48/space-shuttle.png" width="28" align="top"> Running the notebook

1. Start Jupyter in the workspace folder:

```bash
jupyter notebook
```

2. Open [Copy_of_Rock_vs_Mine_Prediction.ipynb](Copy_of_Rock_vs_Mine_Prediction.ipynb) in your browser and run cells in order. <img src="https://img.icons8.com/fluency/48/play.png" width="20" align="top">

## <img src="https://img.icons8.com/fluency/48/note.png" width="28" align="top"> Notes
- Path note: the notebook currently uses an absolute Windows path to load the CSV: `D:\\sonar rock\\data\\Copy of sonar data.csv`. If you move the project, either update that path in the notebook or place the CSV at the same path. To avoid this, prefer a relative path like `data/Copy of sonar data.csv`.
- Prediction labels: the model outputs `R` (rock) or `M` (mine). The example prints a human-friendly message.

## <img src="https://img.icons8.com/fluency/48/test-tube.png" width="28" align="top"> How to use the predictive example (code excerpt)

```python
input_data_as_numpy_array = np.asarray(input_data)
input_data_reshaped = input_data_as_numpy_array.reshape(1, -1)
prediction = model.predict(input_data_reshaped)
if prediction[0] == 'R':
    print('The object is a Rock')
else:
    print('The object is a Mine')
```

## <img src="https://img.icons8.com/fluency/48/sparkling.png" width="28" align="top"> Extras
- If you'd like, I can also create a `requirements.txt` or convert the notebook into a standalone script for easier command-line use. Would you like that? <img src="https://img.icons8.com/fluency/48/checkmark.png" width="20" align="top">
