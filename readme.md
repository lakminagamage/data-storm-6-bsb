# Kaggle Competition Environment Setup (Python)

## 1. Create a Virtual Environment (Optional but Recommended)

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

## 2. Install Essential Libraries

Adjust these based on the competition needs:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn xgboost lightgbm catboost jupyter notebook kaggle
pip install -U pip  # Upgrade pip to the latest version
```

## 3. Set Up Kaggle API Credentials

1. Go to [https://www.kaggle.com/account](https://www.kaggle.com/account).
2. Click **"Create New API Token"** to download `kaggle.json`.

### On Linux/macOS:

Move the file to your Kaggle configuration directory:

```bash
mkdir -p ~/.kaggle
mv /path/to/kaggle.json ~/.kaggle/
chmod 600 ~/.kaggle/kaggle.json
```

### On Windows:
1. Create a folder named `.kaggle` in your user directory (e.g., `C:\Users\<YourUsername>\.kaggle`).
2. Move the `kaggle.json` file into this folder.
3. Set the file permissions to read-only for your user account.
```bash


## 4. 📥 Download Competition Data

Replace `<competition-name>` with the actual competition name (ex: data-storm-6).

```bash
kaggle competitions download -c <competition-name>
unzip <competition-name>.zip -d data/
```