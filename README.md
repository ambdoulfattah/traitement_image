# 🖼️ Image Processing Toolkit — Python & MATLAB

> Bibliothèque de traitement d'images implémentée from scratch en Python et MATLAB, couvrant les opérations fondamentales sur les images en niveaux de gris et RGB.

---

## 📌 Présentation

Ce projet implémente **manuellement** (sans librairies de haut niveau type OpenCV ou scikit-image) un ensemble d'opérations classiques de traitement d'images. L'objectif est de comprendre les mécanismes internes du traitement d'images en travaillant directement sur les matrices de pixels.

Le projet est développé en deux langages complémentaires :

- **Python** — avec NumPy et PIL pour la manipulation matricielle
- **MATLAB** — pour les mêmes fonctionnalités, en environnement scientifique

---

## ⚙️ Fonctionnalités implémentées

### Images en niveaux de gris

| Fonction               | Description                                                 |
| ---------------------- | ----------------------------------------------------------- |
| `lectureImage`         | Chargement et conversion en niveaux de gris (matrice NumPy) |
| `image_noir_blanche`   | Génération d'un damier binaire                              |
| `negatif / inverser`   | Inversion des niveaux de gris (négatif)                     |
| `flipH`                | Symétrie verticale (axe gauche-droite)                      |
| `symetrie_horizontale` | Symétrie horizontale (axe haut-bas)                         |
| `symetrie_verticale`   | Symétrie verticale vectorisée                               |
| `poserV`               | Concaténation verticale de deux images                      |
| `poserH`               | Concaténation horizontale de deux images                    |
| `luminance`            | Calcul de la luminance moyenne (pixel moyen)                |
| `constrast`            | Calcul du contraste (variance des niveaux de gris)          |
| `profondeur`           | Valeur maximale de pixel dans l'image                       |

### Images RGB

| Fonction         | Description                                                   |
| ---------------- | ------------------------------------------------------------- |
| `initImageRGB`   | Génération d'une image RGB aléatoire (format `3 x H x W`)     |
| `grayscale`      | Conversion RGB → niveaux de gris (moyenne min/max des canaux) |
| `afficher_image` | Affichage unifié niveaux de gris et RGB                       |

---

## 🗂️ Structure du projet

```
image-processing/
│
├── python/
│   ├── traitement_image.py      # Toutes les fonctions + menu interactif
│   └── image1.png               # Image de sortie sauvegardée
│
├── matlab/
│   └── traitement_image.m       # Implémentation équivalente en MATLAB
│
└── README.md
```

---

## 🚀 Lancement (Python)

### Prérequis

```bash
pip install numpy matplotlib Pillow
```

### Exécution

```bash
python traitement_image.py
```

Un menu interactif s'affiche dans le terminal avec toutes les opérations disponibles.

---

## 🧠 Concepts clés mis en œuvre

- Représentation matricielle des images (tableau 2D pour niveaux de gris, 3D pour RGB)
- Manipulation directe des pixels sans fonctions de haut niveau
- Calculs statistiques sur images : luminance, contraste, profondeur
- Transformations géométriques : symétries, concaténations
- Conversion d'espaces colorimétriques (RGB → Grayscale)

---

## 📷 Exemples visuels

| Opération                         | Résultat                                     |
| --------------------------------- | -------------------------------------------- |
| Image originale (niveaux de gris) | Chargée via PIL, convertie en matrice NumPy  |
| Négatif                           | Inversion pixel par pixel                    |
| Symétrie horizontale              | Image retournée haut-bas                     |
| Damier                            | Grille binaire générée algorithmiquement     |
| RGB → Gris                        | Conversion via moyenne (max+min)/2 par canal |

---

## 🛠️ Technologies

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![MATLAB](https://img.shields.io/badge/MATLAB-R2022+-orange)
![NumPy](https://img.shields.io/badge/NumPy-matriciel-lightblue)
![Pillow](https://img.shields.io/badge/Pillow-lecture%20image-green)
![Matplotlib](https://img.shields.io/badge/Matplotlib-affichage-red)

---

## 👤 Auteur

Étudiant en classe préparatoire (2ème année) — profil mathématiques & informatique.  
Projet réalisé dans le cadre du cours de traitement d'images.
