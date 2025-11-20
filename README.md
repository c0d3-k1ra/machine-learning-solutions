# ML Project

This is a standard structure for a Python machine learning project.

## Setup Instructions

### 1. Clone the Repository
```bash
git clone <repository-url>
cd ML
```

### 2. Create and Activate Virtual Environment

The project uses a Python virtual environment to manage dependencies.

**Create the virtual environment** (if not already created):
```bash
python3 -m venv venv
```

**Activate the virtual environment:**

- On macOS/Linux:
  ```bash
  source venv/bin/activate
  ```

- On Windows:
  ```bash
  venv\Scripts\activate
  ```

You should see `(venv)` in your terminal prompt when the environment is activated.

### 3. Install Dependencies

With the virtual environment activated, install all required packages:

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Set Up Jupyter Kernel

To use the virtual environment in Jupyter notebooks:

```bash
python -m ipykernel install --user --name=ml-venv --display-name="Python (ML venv)"
```

### 5. VSCode Setup (Recommended)

The repository includes VSCode configuration files in `.vscode/`:

- **settings.json**: Configures Python interpreter, Jupyter settings, and file exclusions
- **extensions.json**: Lists recommended extensions

**Recommended Extensions:**
- Python (ms-python.python)
- Jupyter (ms-toolsai.jupyter)
- Jupyter Notebook Renderers
- Jupyter Keymap
- Jupyter Cell Tags

VSCode will prompt you to install these extensions when you open the project.

**Using Notebooks in VSCode:**
1. Open any `.ipynb` file
2. VSCode will automatically detect the `venv` Python interpreter
3. Select the **"Python (ML venv)"** kernel from the kernel picker (top right)
4. Start coding!

**Or Launch Jupyter Manually:**

```bash
# For Jupyter Notebook
jupyter notebook

# For JupyterLab
jupyter lab
```

When you open a notebook, select the kernel **"Python (ML venv)"** from the kernel menu.

## Dependencies

Main libraries included:
- **NumPy**: Numerical computing
- **Pandas**: Data manipulation and analysis
- **Matplotlib & Seaborn**: Data visualization
- **Scikit-learn**: Machine learning algorithms
- **Jupyter**: Interactive notebooks
- **Kagglehub**: Kaggle dataset integration

See `requirements.txt` for the complete list with versions.

## Deactivating the Environment

When you're done working, deactivate the virtual environment:

```bash
deactivate
```

## Notes

- Always activate the virtual environment before working on the project
- The `venv/` directory is excluded from version control
- If you add new packages, update `requirements.txt`:
  ```bash
  pip freeze > requirements.txt
  ```