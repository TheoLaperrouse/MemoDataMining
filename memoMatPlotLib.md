# Memo MatPlotLib

## Fonctions classiques

### Import

import matplotlib.pyplot as plt

### Fonction de densité

df['col1'].plot.kde()

### Diagramme à secteurs

df['col1'].value_counts().plot.pie(figsize=(longueur, hauteur))

### Affichage Diagramme

plt.show()
