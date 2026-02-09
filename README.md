Ce notebook réalise un fine-tuning du modèle YOLOv8, et non un entraînement complet à partir de zéro.

Voici les détails techniques identifiés dans le document qui confirment cette approche :

Utilisation de poids pré-entraînés : Le notebook charge le modèle yolov8n.pt (YOLOv8 nano), qui contient des poids déjà entraînés sur le dataset COCO.

Transfert d'apprentissage : Lors du lancement de l'entraînement, le système indique explicitement avoir transféré 319/355 éléments (poids) depuis le modèle pré-entraîné.

Configuration de l'entraînement :

Modèle de base : YOLOv8n.

Nombre d'époques : L'entraînement est configuré pour 100 époques.

Taille d'image : Les images sont redimensionnées à 320x320 pixels pour l'entraînement et la validation.

Optimiseur : Utilisation automatique d'AdamW avec un taux d'apprentissage initial (lr0) de 0.002.

Le notebook est structuré pour effectuer deux tâches distinctes basées sur ce fine-tuning : la détection des plaques d'immatriculation (LP) et la reconnaissance de caractères (OCR) sur ces mêmes plaques.