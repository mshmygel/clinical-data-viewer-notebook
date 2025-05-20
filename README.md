# Clinical Data Viewer - Jupyter Version (for Colab or local use)

This project provides an interactive notebook for browsing clinical datasets in SDTM/ADaM formats. It supports `.sas7bdat`, `.xpt`, `.csv`, and `.xlsx` files and runs in Google Colab or locally via Jupyter Notebook.

---

## ✨ What It Does

* Lists all dataset files from a `data/` folder
* Allows you to select and preview a file
* Displays:

  * First few rows
  * DataFrame structure
  * Descriptive statistics
  * Null-value summary
* Allows export to `.csv` or `.xlsx`
* Includes automatic validation:

  * Checks for `data/` folder
  * Verifies file exists and is readable
  * Ensures DataFrame is not empty

---

## ⚡ Run in Google Colab (Recommended)

> No installation required. Just follow these steps:

### 1. Open the notebook:

[Open in Colab](https://colab.research.google.com/github/mshmygel/clinical-data-viewer-notebook/blob/dev/notebooks/viewer.ipynb)

### 2. Upload your data:

1. In the left panel (**Files**), right-click in an empty area → **New folder** → name it `data`
2. Hover over `data/`, click the **three dots** → **Upload**
3. Upload your `.sas7bdat`, `.xpt`, `.csv`, or `.xlsx` files

### 3. Run the notebook:

1. In the top menu, click **Runtime** → **Run all** (or press `Ctrl+F9`)
2. Required packages (like `pyreadstat`) will be installed automatically
3. When prompted, type the file name, e.g.:

```
dm.xpt
```

4. The notebook will validate and display the dataset
5. At the end, you can enter a filename like:

```
output.xlsx
```

to export the data

---

## 💻 Local Usage (Optional)

### Requirements:

* Python 3.11+
* Poetry or pip

### 1. Clone the repo:

```bash
git clone https://github.com/mshmygel/clinical-data-viewer-notebook.git
cd clinical-data-viewer-notebook
```

### 2. Install dependencies:

With Poetry:

```bash
poetry install
```

With pip:

```bash
pip install pandas pyreadstat openpyxl jupyterlab
```

### 3. Run Jupyter:

```bash
poetry run jupyter notebook
```

### 4. Open `notebooks/viewer.ipynb` and place files in `data/`

---

## 📂 Project Structure

```
clinical-data-viewer-notebook/
├── notebooks/
│   └── viewer.ipynb       # Main notebook with logic and validation
├── data/                  # Folder for input datasets
├── pyproject.toml         # Poetry config
├── poetry.lock
├── README.md
└── .gitignore
```

