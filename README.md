# JHACH_tutorials
Jupyter notebook tutorials for the center for pediatric data science and analytic methodology seminar series

# Python 3.11 and Machine Learning Libraries Installation Tutorial

This tutorial will guide you through installing Python 3.11 and essential libraries for these ML tutorials including NumPy, Pandas, scikit-learn, Matplotlib, Jupyter, and datafold.

---

## Step 1: Download and Install Python 3.11

### Windows:
1. Go to [python.org/downloads](https://www.python.org/downloads/)
2. Download **Python 3.11** (latest 3.11.x version)
3. Run the installer
4. **Important**: Check "Add Python to PATH" during installation
5. Click "Install Now"

### macOS:
```bash
# Using Homebrew (recommended)
brew install python@3.11

# Or download from python.org
# Visit: https://www.python.org/downloads/macos/
```

### Linux (Ubuntu/Debian):
```bash
sudo apt update
sudo apt install software-properties-common
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
sudo apt install python3.11 python3.11-venv python3.11-dev
```

### Verify Installation:
```bash
python3.11 --version
# Should output: Python 3.11.x
```

---

## Step 2: Create a Virtual Environment (Recommended)

Creating a virtual environment keeps your project dependencies isolated.

```bash
# Create a virtual environment
python3.11 -m venv ml_env

# Activate the virtual environment

# On Windows:
ml_env\Scripts\activate

# On macOS/Linux:
source ml_env/bin/activate
```

You should see `(ml_env)` at the beginning of your command prompt.

---

## Step 3: Upgrade pip

Before installing packages, upgrade pip to the latest version:

```bash
python -m pip install --upgrade pip
```

---

## Step 4: Install Required Libraries

### Install NumPy (specific version)
```bash
pip install numpy==1.26.3
```

### Install Pandas
```bash
pip install pandas
```

### Install scikit-learn
```bash
pip install scikit-learn
```

### Install Matplotlib
```bash
pip install matplotlib
```

### Install Jupyter
```bash
pip install jupyter
```

### Install datafold
```bash
pip install datafold
```

---

## Step 5: Install All at Once (Alternative Method)

You can install all packages in one command:

```bash
pip install numpy==1.26.3 pandas scikit-learn matplotlib jupyter datafold
```

Or create a `requirements.txt` file:

```txt
numpy==1.26.3
pandas
scikit-learn
matplotlib
jupyter
datafold
```

Then install from the file:
```bash
pip install -r requirements.txt
```

---

## Step 6: Verify Installation

Check that all packages are installed correctly:

```bash
pip list
```

Or test imports in Python:

```bash
python -c "import numpy; print('NumPy:', numpy.__version__)"
python -c "import pandas; print('Pandas:', pandas.__version__)"
python -c "import sklearn; print('scikit-learn:', sklearn.__version__)"
python -c "import matplotlib; print('Matplotlib:', matplotlib.__version__)"
python -c "import jupyter; print('Jupyter: OK')"
python -c "import datafold; print('datafold:', datafold.__version__)"
```

---

## Step 7: Launch Jupyter Notebook

Start Jupyter Notebook to begin working:

```bash
jupyter notebook
```

This will open a browser window where you can create and run Python notebooks.

---

## Troubleshooting

### Issue: "python3.11 not found"
- **Solution**: Use `python` or `python3` instead, or add Python to your PATH

### Issue: Permission denied (Linux/macOS)
- **Solution**: Use `pip install --user <package>` or use a virtual environment

### Issue: Import errors
- **Solution**: Make sure your virtual environment is activated

### Issue: Conflicting dependencies
- **Solution**: Create a fresh virtual environment:
  ```bash
  deactivate  # if in a venv
  rm -rf ml_env
  python3.11 -m venv ml_env
  source ml_env/bin/activate  # or ml_env\Scripts\activate on Windows
  pip install --upgrade pip
  pip install -r requirements.txt
  ```

---

## Quick Reference Commands

```bash
# Create virtual environment
python3.11 -m venv ml_env

# Activate (Windows)
ml_env\Scripts\activate

# Activate (macOS/Linux)
source ml_env/bin/activate

# Install all packages
pip install numpy==1.26.3 pandas scikit-learn matplotlib jupyter datafold

# Launch Jupyter
jupyter notebook

# Deactivate virtual environment
deactivate
```

---

## Next Steps

Once everything is installed, you can:
1. Create a new Jupyter notebook
2. Test the toy examples (GPR, PCA)
3. Explore the datafold library for diffusion maps and manifold learning
