# Radar-Rainfall-Tools
> Outils de traitement de données de pluie-radar horaire

### Lame d'eau radar COMEPHORE
Extraction des lames d'eau horaires pour un bassin versant.

Codage 100% python (ne nécessite pas de SIG, à part pour générer le fichier BV avec la bonne projection) - Python 3.

Données radar Météo France : https://donneespubliques.meteofrance.fr/?fond=produit&id_produit=291&id_rubrique=34

- Ce script traite tous les fichiers gtif contenus dans le dossier choisi (par exemple une année entière, avec 1 fichier par heure)
- Pour chaque pas de temps (chaque fichier raster), la lame moyenne est calculée pour les pixels à l'intérieur du pçolygone défini dans le fichier vecteur fourni.
- La série chronologique des lames horaires est enregistrée dans un fichier texte au format du logiciel GRP: 2 colonnes, date (yymmddhh) et Pluie en mm, avec un séparateur point-virgule
