# Projet Deep Learning

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
```bash
source $(poetry env info --path)/bin/activate
```

Ou utiliser directement :
```bash
poetry run python script.py
poetry run jupyter lab
```

### Configuration VS Code

1. Ouvrir le projet dans VS Code
2. `Cmd+Shift+P` → "Python: Select Interpreter"
3. Sélectionner l'environnement Poetry

## Utilisation
```bash
# Lancer un notebook
poetry run jupyter lab

# Exécuter un script
poetry run python script.py
```

## Structure du projet
```
projet_deep_learning/
├── pyproject.toml
├── README.md
└── notebooks/
```

## Commandes utiles
```bash
# Voir les packages installés
poetry show

# Ajouter un package
poetry add package_name

# Voir l'environnement
poetry env info
```
