# Memo MatPlotLib

## Graphiques

### Import

import matplotlib.pyplot as plt

### Choisir les variables à utiliser

plt.plot(x, y...)

### Ajouter une légende aux axes

plt.xlabel('legende')

### Modifier les origines des axes

plt.axis([xmin, xmax, ymin, ymax])

### Fonction de densité

df['col1'].plot.kde()

### Diagramme à secteurs

df['col1'].value_counts().plot.pie(figsize=(longueur, hauteur))

### Affichage Diagramme

plt.show()
