Le mini projet de module Programation pour la formation doctoral 2024-2025 realise par: SAADA Nesrine / Doctorante en Élelectrotechnique industielle. BEZZOUH Sara / Doctorante en Élelectrotechnique industielle. ZOURDANI Fatima/ Doctorante en reseaux electriques.
Ce projet simule le suivi et l’analyse de la consommation énergétique des moteurs d’un drone. Il utilise la programmation orientée objet, la simulation de capteurs, la détection d’anomalies et le stockage des données dans MongoDB.
Fonctionnalités Simulation de 4 moteurs de drone avec génération aléatoire de consommation. Détection d’anomalies si la consommation est trop basse ou trop haute. Stockage de toutes les mesures dans une collection unique MongoDB, incluant les anomalies. Code testé avec Pytest et vérifié avec flake8 pour la qualité du code.

Structure du projet
energy_project/
│
├── main.py
├── requirements.txt
├── sensors/
│ └── energy_sensor.py
├── analysis/
│ └── anomaly_detector.py
├── database/
│ └── mongodb_handler.py
└── tests/
├── test_sensor.py
└── test_anomaly.py
modules/ → contient les classes du projet. tests/ → contient les tests unitaires. main.py → script principal pour exécuter la simulation.

Prérequis Python 3.8+ MongoDB Atlas (ou local) Bibliothèques Python : pip install pymongo pytest flake8

Utilisation Modifier le fichier modules/db.py pour renseigner votre username, password et cluster MongoDB. Lancer le script principal : python main.py Les mesures et anomalies sont stockées dans MongoDB dans la collection mesures. Les anomalies apparaissent dans le champ anomalie (ou null si aucune).

Tests unitaires Pour exécuter les tests : python -m pytest Vérifie que toutes les fonctionnalités des modules fonctionnent correctement.

Qualité du code Pour vérifier la conformité du code avec PEP8 : flake8 modules/ tests/ main.py Corrige les éventuelles erreurs de style et de formatage.
