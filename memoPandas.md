# Memo Pandas

## Démarche de travail

1. Définir un objectif mesurable
2. Analyse des Données :

- Identification de la target
- Nombre de lignes et de colonnes
- Types de variables
- Identifications des valeurs manquantes
- Visualiser la target (discrete --> Boxplot, continue --> Histogramme)

3. Pré Traitement des données ( Normaliser, Encoder, Sélection de Variables)
4. Travailler sur le modèle

## Fonctions classiques

### Import

import pandas as pd

### Lire CSV

df = pd.read_csv('nomFichier')

### Récupérer les infos du Set de Data

df.info() pour avoir les infos globales

df.shape pour avoir la taille du dataFrame

df.dtypes pour avoir les types des variables du dataFrame

df.dtypes.value_counts().plot.pie()

df.isna() renvoie True si NaN, False si non

(df.isna().sum()/df.shape[0]).sort_values() pour compter le pourcentage de valeur manquante par colonne

Si valeurs manquantes supérieures à 90%, on enlève les colonnes car inutilisables :

df[df.columns[df.isna().sum()/df.shape[0] < 0.9]]

On peut visualiser les valeurs manquantes en dessinant une heatMap

plt.figure(figsize=(20,10))
cns.heatmap(df.isna(), cbar=False)

### Remplir les NaN avec une valeur donnée

df.fillna(0)
### Enlever une colonne inutile

df.drop('', axis=1)

### Montrer les 5 premières valeurs du Set de Data

df.head()

### Choisir une ou plusieurs colonnes

colonne = df['col1']

colonnes = df[['col1','col2']]

### Trier selon une colonne

tri = df.sort_values(by=['col1'], ascending=False)

### Compter des valeurs

valeurs = df['col1'].value_counts()

### Regrouper les lignes par valeur et faire la somme/moyenne de leur valeur

df.groupby('beer_name').mean() et fait la moyenne des autres colonnes
df.groupby('beer_name').sum() et fait la somme des autres colonnes

### Lister les objets d'une colonne correspondant à une valeur

df.loc[df['col1']== "valeur",:]
