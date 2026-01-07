# Lyon Airbnb Discrimination

Analyse NLP des biais discriminatoires dans les annonces Airbnb à Lyon.

## Objectif

Détecter automatiquement les formulations potentiellement discriminatoires dans ~11,000 annonces Airbnb à Lyon. Le projet croise analyse textuelle (NLP) et données géographiques pour identifier si certains quartiers concentrent plus de langage "exclusif" que d'autres.

## Structure du projet
```
lyon-airbnb-discrimination/
├── data/raw/          → Données brutes Airbnb (non modifiées)
├── data/processed/    → Données nettoyées et transformées
├── notebooks/         → Notebooks Jupyter d'exploration et analyse
├── src/               → Code Python réutilisable (fonctions, scripts)
├── models/            → Modèles ML entraînés sauvegardés
└── figures/           → Graphiques et cartes exportés
```

## Stack technique

- **NLP** : spaCy, scikit-learn (TF-IDF)
- **ML** : scikit-learn (Random Forest)
- **Géospatial** : Folium, Geopandas
- **Dashboard** : Streamlit
- **Data** : Pandas, NumPy

## Installation
```bash
git clone https://github.com/itloow/lyon-airbnb-discrimination.git
cd lyon-airbnb-discrimination

python -m venv env
source env/bin/activate  

# 3. Installer les dépendances
pip install -r requirements.txt

# 4. Télécharger le modèle spaCy français
python -m spacy download fr_core_news_md

# 5. Télécharger les données
python src/download_data.py
```

## Source des données

[Inside Airbnb](http://insideairbnb.com) - Lyon, France (~11,000 annonces)

## Statut

🟡 En cours - Semaine 1 : Setup et exploration

