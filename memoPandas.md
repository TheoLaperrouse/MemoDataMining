# Memo Panda

## Fonctions classiques

### Lire CSV

df = pd.read_csv('nomFichier')

### Choisir une ou plusieurs colonnes

colonne = df['col1']

colonnes = df[['col1','col2']]

### Trier selon une colonne

tri = df.sort_values(by=['col1'], ascending=False)