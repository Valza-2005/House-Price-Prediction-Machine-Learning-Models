# House Price Prediction - Machine Learning Models

Ky projekt analizon te dhenat e shitjeve te shtepive ne King County dhe
krahason disa metoda klasifikimi dhe clustering:

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Random Forest
- Neural Network
- K-Means Clustering

Kodi eshte organizuar ne Jupyter Notebooks. Dataset-i fillestar gjendet ne
`data/raw/kc_house_data.csv`.

## Kerkesat

- Python 3.11 (64-bit)
- Rekomandohen te pakten 8 GB RAM
- Lidhje interneti vetem gjate instalimit te bibliotekave

Python 3.11 rekomandohet sepse versionet e bibliotekave ne `requirements.txt`,
vecanerisht TensorFlow, jane te pajtueshme me kete version.

## Instalimi

Hapni terminalin ne dosjen kryesore te projektit dhe ekzekutoni:

### Windows PowerShell

```powershell
py -3.11 -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### macOS ose Linux

```bash
python3.11 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
```

## Ekzekutimi manual me Jupyter

Nisni Jupyter nga dosja kryesore:

```bash
jupyter lab
```

Ekzekutoni notebook-et ne kete rend:

1. `notebooks/data_processing/01_data_exploration.ipynb`
2. `notebooks/data_processing/02_data_cleaning.ipynb`
3. `notebooks/data_processing/03_feature_engineering.ipynb`
4. `notebooks/data_processing/04_scaling_train_val_test_split.ipynb`
5. Notebook-et ne `notebooks/models/`
6. `notebooks/final_comparison.ipynb`

Hapni secilin notebook nga JupyterLab dhe ekzekutoni te gjitha qelizat me
`Run All`. Prisni qe nje notebook te perfundoje para se te vazhdoni me
notebook-un pasardhes.

Per notebook-et 1-4 dhe modelet KNN, Logistic Regression dhe Clustering,
working directory duhet te jete dosja ku ndodhet notebook-u.

## Krahasimi perfundimtar dhe raporti

Skedari `notebooks/final_comparison.ipynb` eshte notebook-u kryesor per
krahasimin perfundimtar te modeleve dhe sherben si raport i rezultateve te
projektit. Ai mbledh rezultatet e modeleve te trajnuara, krahason performancen
e tyre dhe paraqet perfundimet kryesore.

Ky notebook duhet te ekzekutohet pasi te jene perfunduar notebook-et e
perpunimit te te dhenave dhe te gjitha modelet ne `notebooks/models/`.

## Struktura

```text
.
|-- data/
|   |-- raw/                    # Dataset-i origjinal
|   `-- processed/              # Te dhena dhe rezultate te gjeneruara
|-- notebooks/
|   |-- data_processing/        # Eksplorim, pastrim dhe pergatitje
|   |-- models/                 # Trajnimi dhe vleresimi i modeleve
|   `-- final_comparison.ipynb  # Krahasimi perfundimtar
|-- requirements.txt            # Bibliotekat dhe versionet
`-- README.md
```

## Shenime

- `data/processed/` gjenerohet nga notebook-et e perpunimit.
- `data/processed/model_results/` gjenerohet nga notebook-et e modeleve.
- Random seeds jane vendosur ne modelet ku perdoret rastesi, per rezultate sa
  me te riprodhueshme.
- Trajnimi i Neural Network mund te jape ndryshime te vogla numerike sipas
  procesorit dhe sistemit operativ.
