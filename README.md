# DL_project_traffic_signs

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Minetriforce/DL_project_traffic_signs/blob/main/project_traffic_signs.ipynb)

## Sommaire
<img src="https://upload.wikimedia.org/wikipedia/commons/f/f8/CY_Tech.svg" align="right"
     alt="Size Limit logo by Anton Lovchikov" width="170">
     
- [Présentation](#présentation)
- [Arborescence du projet](#arborescence-du-projet)
- [Lancer le Notebook dans Google Colab](#lancer-le-notebook-dans-google-colab)

---

## Présentation

**DL_project_traffic_signs** est un projet de Deep learning axé sur la reconnaissance automatique de panneaux de signalisation routière. Le projet s'appuie sur le jeu de données de référence **GTSRB (German Traffic Sign Recognition Benchmark)**, composé de plus de 51 800 images réelles réparties en 43 classes différentes (limitations de vitesse, interdictions, obligations, etc.).

Il suit une progression étape par étape :
1. **Classification multiclasse** sur des panneaux déjà découpés et extraits (Réseau Dense / MLP vs CNN)[cite: 2, 3, 8].
2. **Expérimentations et optimisations** pour maximiser les performances.
3. **Détection d'objets dans une scène complète (YOLO)** pour localiser et classifier dynamiquement plusieurs panneaux (Bounding boxes + scores de confiance)[cite: 3, 8, 9].
4. **Extension vidéo** pour valider la chaîne de traitement sur des séquences routières[cite: 3, 9].

Chaque historique et modèle est sauvegardé afin d'éviter à relancer l'entièreté du notebook.


## Arborescence du projet

```text
DL_project_traffic_signs/
│
├── README.md
├── DL_project_traffic_signs.ipynb  # Notebook principal
├── data
    ├── images/                     # Images de test pour YOLO
    └── videos/                     # Vidéos de test et de résultats pour YOLO
├── saves
    ├── history/                    # Sauvegardes des historiques
    └── models/                     # Sauvegardes des modèles
└── gtsrb-german-traffic-sign/      # Dataset téléchargé via Kaggle
    ├── Meta/                       # Images de référence / icônes par classe (.png)
    ├── Train/                      # 39 209 images d'entraînement réparties par dossiers de classe (0 à 42)
    ├── Test/                       # Images de test
    ├── Meta.csv                    # Métadonnées des icônes
    ├── Train.csv                   # Métadonnées et annotations d'entraînement
    └── Test.csv                    # Métadonnées et annotations de test
```
## Lancer le Notebook dans Google Colab
Cliquez sur le badge ci-dessus pour ouvrir le notebook directement dans Google Colab.

- Assurez-vous d'activer un accélérateur matériel GPU :

- Rendez-vous dans Exécution > Modifier le type d'exécution.

- Sélectionnez GPU T4 dans la liste des accélérateurs.

- Exécutez les cellules séquentiellement. Le téléchargement du dataset s'effectuera automatiquement lors de la première exécution.