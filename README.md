## Overview
Notebook: `textClassifer_nb.ipynb`  
This project is a Python notebook for text classification. Use a virtual environment on Windows and install dependencies there.

## Quick setup (Windows)
Create and activate a venv, then install required tools.

Brief explanation: create a virtual environment and activate it on Windows.
```bash
python -m venv .venv
.\.venv\Scripts\activate
```

Brief explanation: install jupyter and pipreqs inside the active venv.
```bash
python -m pip install --upgrade pip
python -m pip install jupyter pipreqs
```

## Generating `requirements.txt`
If `pipreqs` is not picking up imports from the notebook, convert the notebook to a script and run `pipreqs` on the directory.

Brief explanation: convert the notebook to a `.py` script.
```bash
jupyter nbconvert --to script textClassifer_nb.ipynb
```

Brief explanation: generate `requirements.txt` from the project directory (run while `.venv` is active).
```bash
pipreqs . --force
```

Notes:
- Install and run `pipreqs` inside the active virtual environment so it uses the venv's Python and packages.
- If you prefer not to convert, you can inspect the notebook for imports manually or use tools that parse notebooks directly.

## Running the notebook
Brief explanation: start Jupyter and open the notebook.
```bash
jupyter lab
# or
jupyter notebook
```
Open `textClassifer_nb.ipynb` in the browser or run cells in PyCharm's notebook support.



## Troubleshooting
- If `pipreqs` seems to ignore files, ensure you run it from the project root and the venv is active.
- If imports are inside notebook cells only, converting to a script before running `pipreqs` helps.
- For Windows path issues, run commands from PowerShell or CMD with the venv activated.