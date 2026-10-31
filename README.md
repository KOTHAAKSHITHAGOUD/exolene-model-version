# exolene-model-version

# EXOLENE – Environment Setup

## Requirements
- Python 3.14
- Visual Studio Code
- Python extension for VS Code
- Jupyter extension for VS Code

## 1. Clone the repository

```bash
git clone <your-repository-url>
cd EXOLENE
```

## 2. Create a virtual environment

```powershell
python -m venv .venv-exolene
```

## 3. Activate the environment (Windows PowerShell)

```powershell
.\.venv-exolene\Scripts\Activate.ps1
```

## 4. Install dependencies

```powershell
python -m pip install --upgrade pip setuptools wheel
python -m pip install -r requirements.txt
```

## 5. Install PyTorch (CPU version)

```powershell
python -m pip install torch torchvision --index-url https://download.pytorch.org/whl/cpu
```

## 6. Register the Jupyter kernel

```powershell
python -m pip install ipykernel
python -m ipykernel install --user --name exolene --display-name "Python (EXOLENE)"
```

## 7. Open the notebook in VS Code

- Install the Python and Jupyter extensions.
- Open the `.ipynb` notebook.
- Select the `Python (EXOLENE)` kernel.

## 8. Verify the environment

```python
import torch
import numpy
import pandas
import matplotlib
import rasterio

print("Environment setup successful!")
print("PyTorch:", torch.__version__)
```

**Note:** The documented setup uses CPU-based PyTorch. CUDA acceleration is not configured.
