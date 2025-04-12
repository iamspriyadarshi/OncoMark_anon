## Usage

OncoMark provides a Python API and a web interface to quantify hallmark activity from transcriptomics data. This page outlines how to use both interfaces effectively.

---

### Python API

The Python API allows you to directly process data and predict hallmark scores using the pre-trained model provided with the package.

#### Step 1: Import Required Libraries

Before using OncoMark, ensure you have your transcriptomics data in a pandas `DataFrame`.

```python
import pandas as pd
from OncoMark import predict_hallmark_scores
```

#### Step 2: Load Input Data

Load your transcriptomics data into a pandas `DataFrame`. The data should be formatted with samples as rows and genes as columns.

```python
# Load input data as a pandas DataFrame
input_data = pd.read_csv('path_to_your_data.csv', index_col=0)
```

#### Step 3: Predict Hallmark Scores

Use the `predict_hallmark_scores` function to process the data and generate hallmark activity predictions.

```python
# Predict hallmark scores
predictions = predict_hallmark_scores(input_data)

# Display the predictions
print(predictions)
```

#### Step 4: Save Results (Optional)

You can save the predictions as a CSV file for further analysis.

```python
# Save predictions to a CSV file
predictions.to_csv('predictions.csv')
```

---

### Web Interface

OncoMark also provides a user-friendly web interface for those who prefer not to write code.

You can use the hosted web server to upload your data and obtain hallmark activity predictions:

[OncoMark Web Server](https://oncomark-ai.hf.space/)

---

### Example Data

You can find example input data for testing in the `test` directory of the GitHub repository or use the following snippet to create a sample DataFrame:

```python
import pandas as pd
import numpy as np

# Generate random example data
genes = ['Gene1', 'Gene2', 'Gene3', 'Gene4']
samples = ['Sample1', 'Sample2', 'Sample3']
data = np.random.rand(len(samples), len(genes))

# Create a DataFrame
example_data = pd.DataFrame(data, index=samples, columns=genes)
print(example_data)
```

---

### Notes and Tips

- Ensure your input data contains genes matching the feature names used during model training.
- Ensure that the genes is in the columns of the datasets.
- Genes missing from the input data but used during model training will be filled with zeros, while additional genes not used in training will be ignored.
- Check the [Documentation](https://oncomark.readthedocs.io/en/latest/) for troubleshooting tips and advanced usage.

---

With this guide, you are ready to start exploring OncoMark's capabilities to quantify hallmark activity from your transcriptomics data.

---
