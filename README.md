<div align="center">
  <img src="https://github.com/user-attachments/assets/4da8fdff-41dd-49aa-b4f0-32ed1806a3bc" alt="Oncomark Poster">
</div>
<br>

**OncoMark** is a deep learning tool designed to systematically quantify hallmark activity using transcriptomics data from routine tumor biopsies. Ideal for applications in oncology research, personalized medicine, and biomarker discovery.

---

## Usage

### Python API

```python
import pandas as pd
from OncoMark import predict_hallmark_scores

# Load input data as a pandas DataFrame. Genes must be in column.
input_data = pd.read_csv('input_data.csv', index_col=0)

# Predict hallmark scores
predictions = predict_hallmark_scores(input_data)

# Display the predictions
predictions
```

### Web Server

OncoMark also provides a web server for easy interaction.

#### Access the Online Web Server

You can use the hosted web server directly:

[OncoMark Web Server](https://oncomark-ai.hf.space/)

---
