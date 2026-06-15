# 🔋 Dashboard d'analyse des véhicules électriques 2025

## Présentation du projet
Application web interactive développée avec Streamlit, utilisant DuckDB pour
le stockage et l'interrogation des données. Elle permet d'analyser les
spécifications de véhicules électriques (autonomie, capacité de batterie,
efficience, type de carrosserie) à partir d'un fichier CSV.

## Instructions d'installation et d'exécution

1. Cloner le dépôt :
\`\`\`bash
git clone https://github.com/c-antony/dashboard-vehicules-electriques.git
cd dashboard-vehicules-electriques
\`\`\`

2. Créer et activer un environnement virtuel :
\`\`\`bash
python -m venv venv
venv\\Scripts\\activate   # Windows
source venv/bin/activate  # Mac/Linux
\`\`\`

3. Installer les dépendances :
\`\`\`bash
pip install -r requirements.txt
\`\`\`

4. Lancer l'application :
\`\`\`bash
streamlit run src/app.py
\`\`\`

5. Téléverser le fichier `electric_vehicles_spec_2025.csv` via l'interface.

## Description des fonctionnalités
- **Téléversement de fichier CSV** des spécifications de véhicules électriques.
- **Stockage et requêtage via DuckDB** pour des analyses performantes.
- **4 indicateurs clés (KPI)** :
  1. Autonomie moyenne par marque (bar chart)
  2. Relation autonomie / capacité de batterie (scatter plot)
  3. Répartition par type de carrosserie (pie chart)
  4. Efficience énergétique moyenne par transmission (bar chart)
- **Filtres dynamiques** : marque, type de carrosserie, transmission, plage d'autonomie.
- **Tableaux complémentaires** : top 10 modèles par autonomie, données filtrées.

## Répartition des tâches (équipe de 3)
| Membre | Tâche |
|---|---|
|  Nous 3| Module DuckDB / chargement et nettoyage des données (`db.py`) |
| Christ Antony TCHOKOGUEU | Requêtes SQL et logique des KPI (`queries.py`) |
| David Agnimel | Interface Streamlit et visualisations (`app.py`) |
| Jade DELCOURT| Filtres dynamiques, tests, documentation (`README.md`) |

## Stack technique
- Python 3.13
- Streamlit
- DuckDB
- Pandas
- Plotly