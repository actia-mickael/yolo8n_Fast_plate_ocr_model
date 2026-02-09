Ce notebook réalise un fine-tuning du modèle YOLOv8, et non un entraînement complet à partir de zéro.

Paramètre           | Valeur par défaut      |         Description
Optimiseur          |auto (souvent AdamW)    |S'adapte en fonction du dataset.
Learning Rate (lr0) |0.01                    |Taux d'apprentissage initial.
Époques             |100                     |Nombre de cycles complets sur le dataset.
Patience            |50                      |Arrêt précoce si aucune amélioration après 50 époques.
Batch Size          |16                      |Nombre d'images traitées simultanément.
Augmentation        |Activée                 |"Inclut hsv_h, hsv_s, hsv_v, degrees, translate, scale, shear, perspective, flipud, fliplr, mosaic, mixup, copy_paste."


Voici les détails techniques identifiés dans le document qui confirment cette approche :

Utilisation de poids pré-entraînés : Le notebook charge le modèle yolov8n.pt (YOLOv8 nano), qui contient des poids déjà entraînés sur le dataset COCO.
Transfert d'apprentissage : Lors du lancement de l'entraînement, le système indique explicitement avoir transféré 319/355 éléments (poids) depuis le modèle pré-entraîné.

Configuration de l'entraînement :
Modèle de base : YOLOv8n.
Nombre d'époques : L'entraînement est configuré pour 100 époques.
Taille d'image : Les images sont redimensionnées à 320x320 pixels pour l'entraînement et la validation.
Optimiseur : Utilisation automatique d'AdamW avec un taux d'apprentissage initial (lr0) de 0.002.
Le notebook est structuré pour effectuer deux tâches distinctes basées sur ce fine-tuning : la détection des plaques d'immatriculation (LP) et la reconnaissance de caractères (OCR) sur ces mêmes plaques.








## 📜 Licence et Crédits

### Dataset
Ce projet utilise le **License Plate Recognition Dataset** hébergé sur Roboflow Universe.
- **Auteur :** Roboflow Universe Projects
- **Source :** [Roboflow Universe](https://universe.roboflow.com/roboflow-universe-projects/license-plate-recognition-rxg4e)
- **Type :** Open Source Dataset

### Citation BibTeX
Si vous utilisez ce travail, merci de citer le dataset original :

```bibtex
@misc{license-plate-recognition-rxg4e_dataset,
    title = { License Plate Recognition Dataset },
    type = { Open Source Dataset },
    author = { Roboflow Universe Projects },
    howpublished = { \url{ [https://universe.roboflow.com/roboflow-universe-projects/license-plate-recognition-rxg4e](https://universe.roboflow.com/roboflow-universe-projects/license-plate-recognition-rxg4e) } },
    url = { [https://universe.roboflow.com/roboflow-universe-projects/license-plate-recognition-rxg4e](https://universe.roboflow.com/roboflow-universe-projects/license-plate-recognition-rxg4e) },
    journal = { Roboflow Universe },
    publisher = { Roboflow },
    year = { 2026 },
    month = { jan },
    note = { visited on 2026-02-09 },
}