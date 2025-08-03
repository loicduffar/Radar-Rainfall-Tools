# Radar-Rainfall-Tools
> Outils de traitement de l'ancienne version des données payanes de pluie-radar horaire
> OBSOLETE depuis la sortie en 2025 des images geotif horaire en open-data sur meteo.data.gouv.fr
> Voir le code adapté au nouveau format dans le dépôt meteo.data

### Lame d'eau radar COMEPHORE (Météo France)
Extraction des lames d'eau horaires pour un bassin versant.

Traitement 100% python ne nécessitant pas de SIG (à part pour convertir le fichier BV dans la même projection que les images Météo-France) - Python 3.

Données radar Météo France : https://donneespubliques.meteofrance.fr/?fond=produit&id_produit=291&id_rubrique=34

- Ce script traite tous les fichiers gtif contenus dans le dossier choisi (par exemple une année entière, avec 1 fichier par heure)
- Pour chaque pas de temps (chaque fichier raster), la lame moyenne est calculée pour les pixels à l'intérieur du polygone défini dans le fichier vecteur fourni.
- La série chronologique des lames horaires est enregistrée dans un fichier texte au format du logiciel GRP: 2 colonnes date (yymmddhh) + Pluie (mm), séparées par un point-virgule.
