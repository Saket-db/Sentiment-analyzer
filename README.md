# Sentiment Analyzer

This repository contains a Google Colab notebook that builds and evaluates an LSTM-based sentiment analysis model using the IMDb dataset. The notebook demonstrates data loading, preprocessing, model building (LSTM), training, and evaluation.

## Files
- `Sentiment_Analysis.ipynb` — Google Colab notebook with the full workflow.

## Libraries / Dependencies
- numpy
- tensorflow
- keras
- nltk
- re (Python standard library)

> Note: `re` is part of Python's standard library and does not require installation.

## Recommended environment
- Python 3.7+
- For reproducibility it's recommended to run inside a virtual environment or in Google Colab (Colab already provides most packages).

## Install (local)
Run these commands in PowerShell to set up a local environment:

```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1

pip install --upgrade pip
pip install numpy tensorflow keras nltk
```

If you need specific versions, pin them (example):

```powershell
pip install tensorflow==2.5.0 keras==2.4.3 numpy==1.19.5
```

## NLTK data
The notebook uses NLTK for tokenization / text processing. To download required NLTK corpora locally:

```python
import nltk
nltk.download('punkt')
nltk.download('stopwords')
```

## Notes / Caveats
- The notebook contains a malformed pip cell: `!pip install numpy = 1.16.1` — this will error. The correct pinned form is `!pip install numpy==1.16.1` if you must pin.
- The notebook uses Keras APIs (and the Keras imdb dataset). If you run with TensorFlow 2.x, you may prefer `tensorflow.keras` or ensure the standalone `keras` package is compatible with your TensorFlow version.
- Colab is the simplest place to run the notebook (open via the "Open in Colab" badge), and you can enable a GPU runtime there for faster training.

## How to run
- In Google Colab: open `Sentiment_Analysis.ipynb`, then run cells sequentially.
- Locally: install dependencies, download NLTK data, then open the notebook in Jupyter and run.
