# Datascience Snippets

<table>
<tr>

</td>

<td style="width:300px">

```python
### Librerías Básicas
import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import seaborn as sns

from scipy import stats
```

</td>

<td style="width:300px">

```python
### Análisis Exploratorio
df.info()
df.describe()
df.stats.skew()
dfbl.stats.kurtosis()
```

</tr>
<tr>
<td>

```python
### Conectar con Google Drive
from google.colab import drive
drive.mount('/content/drive/')

ruta = "/content/drive/My Drive/"
df = pd.read_csv(ruta)
```

</td>
<td>

```python
### Train/Test Split
from sklearn.model_selection import train_test_split

X_train, X_test, y_train_, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
```

</td>
</tr>
</table>

```python
### Paleta de colores
# Catppuccin Mocha
colors = ['#f5e0dc', '#f2cdcd', '#f5c2e7', '#cba6f7', '#f38ba8', '#eba0ac',
          '#fab387', '#f9e2af', '#a6e3a1', '#94e2d5', '#89dceb', '#74c7ec',
          '#89b4fa', '#b4befe', '#cdd6f4', '#bac2de', '#a6adc8', '#9399b2',
          '#7f849c', '#6c7086', '#585b70', '#45475a', '#313244', '#1e1e2e',
          '#181825', '#11111b']
sns.set_palette(colors, n_colors=len(colors))
plt.style.use('dark_background')
```

```python
"""
<p align="center">
  <img src="https://www.inf.ucv.cl/wp-content/themes/escuelainformaticapucv/img/logo_smaller-01.png" alt="Logo" width="400" height="100"/>
</p>

 <p align="center"> <font color="white"><u> Título </u> </font> </p>


<p align="center">  Nombre </p>
<p align="center">  Fecha </p>
"""
```

