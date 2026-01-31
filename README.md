# Projet Deep Learning

Projet de prédiction de clicks avec des modèles de Machine Learning (LightGBM, RandomForest, XGBoost).

## Installation

### Prérequis
- Python 3.14
- Poetry

### Configuration de l'environnement

1. **Cloner le repository**
```bash
git clone <url-du-repo>
cd projet_deep_learning
```

2. **Installer les dépendances avec Poetry**
```bash
poetry install --no-root
```

3. **Activer l'environnement virtuel**

**Mac/Linux :**
```bash
source $(poetry env info --path)/bin/activate
```

**Windows (PowerShell) :**
```powershell
& ((poetry env info --path) + "\Scripts\activate.ps1")
```

**Windows (CMD) :**
```cmd
poetry env info --path
# Puis manuellement : <path>\Scripts\activate.bat
```

**Alternative (toutes plateformes) :**
```bash
poetry run jupyter lab
poetry run python script.py
```

### Configuration VS Code

**Mac :**
1. Ouvrir le projet dans VS Code
2. `Cmd+Shift+P` → "Python: Select Interpreter"
3. Sélectionner l'environnement Poetry

**Windows :**
1. Ouvrir le projet dans VS Code
2. `Ctrl+Shift+P` → "Python: Select Interpreter"
3. Sélectionner l'environnement Poetry

## Structure du projet
```
projet_deep_learning/
├── data/
│   └── Train_clicks.csv          # Données d'entraînement
├── src/
│   ├── notebook_final.ipynb      # Notebook principal
│   └── notebook.ipynb            # Notebook de travail
├── poetry.lock
├── pyproject.toml
└── README.md
```

## Utilisation
```bash
# Lancer Jupyter Lab
poetry run jupyter lab

# Ouvrir le notebook principal
# → src/notebook_final.ipynb

# Exécuter un script Python
poetry run python script.py
```

## Modèles implémentés

- **LightGBM** - Gradient boosting rapide
- **RandomForest** - Ensemble de decision trees  
- **XGBoost** - Gradient boosting optimisé

## Commandes utiles
```bash
# Voir les packages installés
poetry show

# Ajouter un package
poetry add package_name

# Voir l'environnement
poetry env info

# Mettre à jour les dépendances
poetry update
```

## Notes techniques

- **Gestion des NaN** : Les valeurs manquantes sont remplacées par -999
- **Validation** : Cross-validation temporelle avec PredefinedSplit
- **Horizons** : Prédictions à 0, 7, et 14 jours
- **Compatibilité** : LightGBM 4.6.0 requiert la conversion en numpy arrays
