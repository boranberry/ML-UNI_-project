# ML-UNI-project
## part three of project machine
## Dataset Download and Loading

### Dataset Information
- **Dataset Name:** SANAD
- **Source:** [Hugging Face – Mouwiya/SANAD](https://huggingface.co/datasets/Mouwiya/SANAD)
- **File Format:** Parquet
- **File Path:** `data/train-00000-of-00001.parquet`
- **File Size:** Approximately 80 MB
- **Loading Method:** Direct loading from Hugging Face into a Pandas DataFrame.

### 1. Install Required Libraries

Install the required Python libraries:

```bash
pip install pandas numpy pyarrow huggingface_hub fsspec
```

### 2. Import Required Libraries

```python
import pandas as pd
import numpy as np
import pyarrow
```

### 3. Load the Dataset

Load the Parquet file directly from Hugging Face without manually downloading it:

```python
dataset = pd.read_parquet(
    "hf://datasets/Mouwiya/SANAD/data/train-00000-of-00001.parquet"
)
```

### 4. Verify the Dataset

Check that the dataset was loaded successfully:

```python
print("Dataset Shape:", dataset.shape)
print("Dataset Columns:", dataset.columns.tolist())

display(dataset.head())
```

### 5. Check Dataset Information

```python
dataset.info()
```

### Notes
- An active internet connection is required to access the dataset.
- PyArrow is required to read Parquet files through Pandas.
- The dataset is loaded directly into memory as a Pandas DataFrame.
- No manual file download is required.


