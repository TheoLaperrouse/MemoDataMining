# Memo Pandas

## Fonctions classiques

### Import 

import pandas as pd

### Lire CSV

df = pd.read_csv('nomFichier')

### Choisir une ou plusieurs colonnes

colonne = df['col1']

colonnes = df[['col1','col2']]

### Trier selon une colonne

tri = df.sort_values(by=['col1'], ascending=False)

### Compter des valeurs

valeurs = df['col1'].value_counts()

### Trier les valeurs d'une variable de manière croissante

print(df['col1'].sort_values())

### Lister les objets d'une colonne correspondant à une valeur

df.loc[df['col1']== "valeur" ,:]