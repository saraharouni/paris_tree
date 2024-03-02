# Data Challenge - "Végétalisons la Ville"

## Introduction
Pour ce nouveau projet de la Plateforme, nous allons reprendre un des projet de Data for Good sponsorisé par la ville de Paris et pluss précisement ces arbres ! 

## Objectif
L'objectif principal de notre analyse est de réduire le nombre de trajets d'entretien des arbres à Paris, tout en veillant à ce que chaque arbre reçoive les soins nécessaires. Moins de tournées signifie moins de trajets et, par conséquent, plus d'arbres bien entretenus.

## Données
Le jeu de données des arbres de la ville de Paris peut être téléchargé [ici](https://www.google.com/url?q=https://s3-eu-west-1.amazonaws.com/static.oc-static.com/prod/courses/files/AI%2BEngineer/Project%2B2%2BParticipez%2B%25C3%25A0%2Bun%2Bconcours%2Bsur%2Bla%2BSmart%2BCity/p2-arbres-fr.csv&sa=D&source=apps-viewer-frontend&ust=1709476640434254&usg=AOvVaw1LdrJ_ZgEccdHmQkeimmcS&hl=fr). Vous pouvez également le consulter sur [opendata.paris.fr](https://opendata.paris.fr/explore/dataset/les-arbres/map/?dataChart=eyJxdWVyaWVzIjpbeyJjb25maWciOnsiZGF0YXNldCI6Imxlcy1hcmJyZXMiLCJvcHRpb25zIjp7fX0sImNoYXJ0cyI6W3siYWxpZ25Nb250aCI6dHJ1ZSwidHlwZSI6ImNvbHVtbiIsImZ1bmMiOiJBVkciLCJ5QXhpcyI6ImlkYmFzZSIsInNjaWVudGlmaWNEaXNwbGF5Ijp0cnVlLCJjb2xvciI6IiMwMDMzNjYifV0sInhBeGlzIjoidHlwZWVtcGxhY2VtZW50IiwibWF4cG9pbnRzIjo1MCwic29ydCI6IiJ9XSwidGltZXNjYWxlIjoiIiwiZGlzcGxheUxlZ2VuZCI6dHJ1ZSwiYWxpZ25Nb250aCI6dHJ1ZX0%3D&disjunctive.typeemplacement&disjunctive.arrondissement&disjunctive.libellefrancais&disjunctive.genre&disjunctive.espece&disjunctive.varieteoucultivar&disjunctive.stadedeveloppement&disjunctive.remarquable&location=13,48.86844,2.30945&basemap=jawg.streets).

## Présentation Générale du Jeu de Données
Le jeu de données comprend des informations détaillées sur les arbres de la ville.  
**Premières observations**  

**Variables qualitatives**:  

* La colonne **'type_emplacement'** ne contient qu'une valeur **'arbre'**
* La colonne domanialite correspond aux types d'espaces publics :
    * Jardin : espace vert, parc
    * Alignement : espaces le long des rues
    * DJS : Equipements sportifs
    * DFPE : Crèches
    * Cimetiere : cimetière
    * DASC : 	Ecole
    * DAC	Equipements culturels
    * ASES	Action sociales
  
* La colonne arrondissement comprend tous les arrondissements (1er au 20eme ainsi que le bois de Boulogne, le bois de Vincennes, les Hauts-de-Seine, le Val de Marne et la Seine-Saint-Denis.
* La colonne **complément d'adresse** contient beaucoup de valeurs manquantes.
* Les colonnes **lieu, id_emplacement** ne contiennent pas de valeurs manquantes et désignent un lieu.
* La colonne **libelle_francais** affiche le nom de l'arbre en français. Elle comprend 192 types et 1497 valeurs manquantes.
* Les colonnes **genre, espece et variété** donnent plus d'informations sur le type d'arbre. Elles correspondent à trois niveaux de classification des plantes.
* La colonne **stade_developpement** indique les différents stades de développement des arbres (4 valeurs )

**Variables quantitatives :**  

* La colonne id correspond à l'id de l'arbre et semble contenir 2 doublons.
* La colonne **numero** est **vide**.
* Les colonnes **circonference_cm et hauteur** donne des informations sur la taille de l'arbre et ne contiennent pas de valeurs manquantes.
* La colonne **remarquable** indique quel arbre est dit *remarquable* (Un arbre remarquable est un arbre qui est considéré comme exceptionnel en raison de ses caractéristiques particulières, de son âge, de sa taille, de sa rareté, de son histoire ou de son importance écologique, culturelle ou historique). Elle comprend 63098 valeurs manquantes.
* La colonne geometry indique la présence de 94 doublons (il ne peut pas y avoir 2 arbres à les mêmes coordonnées).
* Les deux dernières colonnes sont des données spatiales qui vont me permettrent d'afficher mes données via Geopandas.

## Démarche Méthodologique d'Analyse de Données
1. **Exploration initiale :** Comprendre la structure des données, identifier les variables clés.
2. **Nettoyage des données :** Gérer les valeurs manquantes, éliminer les doublons, etc.
3. **Analyse descriptive :** Visualiser la distribution des variables, identifier les tendances.
4. **Analyse par espèce :** Examiner les spécificités liées à chaque espèce d'arbre.
5. **Géolocalisation :** Utiliser des outils de cartographie pour comprendre la répartition spatiale des arbres.

## Synthèse de l'Analyse de Données
Notre analyse détaillée mettra en lumière des opportunités pour optimiser les tournées d'entretien, en prenant en compte des facteurs tels que la répartition géographique, l'état de développement des arbres, etc.

## Présentation Finale
En tant que binôme, nous aurons 15 minutes pour présenter nos résultats et nos recommandations pour une gestion plus efficace des arbres de la ville de Paris.

## Notebook Jupyter
Le deuxième livrable consistera en un Notebook Jupyter documenté. Chaque étape, traitement et graphique seront expliqués de manière à être compréhensibles par un public non technique. Nous nous efforcerons de rendre notre analyse transparente et accessible.

## Clonage du Répertoire Git pour les Données
Si vous souhaitez accéder au jeu de données, vous pouvez cloner notre répertoire Git en utilisant la commande suivante dans votre terminal :
```bash
git clone https://github.com/saraharouni/paris_tree.git)https://github.com/saraharouni/paris_tree.git
