# Web Sémantique

## Groupe

| Groupe 1         |
| ---------------- |
| Thomas Giraud    |
| Maëlle Le Lannic |
| Julien Bacquart  |

## Dataset

- **Intitulé** : OlympicsGoNUTS  
- **Taille** : 2202 lignes, 46 colonnes, 1462 ko  
- **Source** : https://github.com/EDJNet/OlympicsGoNUTS  
- **Publisher** : Giorgio Comai (OBCT/CCI) for the [European Data Journalism Network](https://www.europeandatajournalism.eu/)
- **Licence** : CC-BY license (Giorgio Comai/OBCT/EDJNet)

## Slides

[WebSemantique - Presentation](https://docs.google.com/presentation/d/1KLYlVwpXp00OIlhzkgwN0bMuaWH4ockdj4gNZlJnpXo/edit?usp=sharing)

## Sémantisation des données

Cloner le repository :

`git clone https://github.com/JulienBacquart/WebSemantique.git`

`cd WebSemantique`

Executer au choix une des commandes suivantes suivant le dataset choisi :

- Pour le fichier **2024_medalists_nuts_only.csv** :

`tarql-1.2/bin/tarql --dedup 30000 transform.sparql ./dataset/2024_medalists_nuts_only.csv > 2024_medalists_nuts_only.ttl`

Retourne environ 30 000 triplets.

- Pour le fichier **2024_medalists_all.csv** :

`tarql-1.2/bin/tarql --dedup 60000 transform.sparql ./dataset/2024_medalists_all.csv > 2024_medalists_all.ttl`

Retourne environ 60 000 triplets.

## Serveur SPARQL avec Docker Compose

Un fichier `compose.yaml` est fourni pour facilement déployer un serveur SPARQL Jena Fuseki, pour le lancer utiliser la commande suivante :

`docker compose up`

Le serveur sera disponible à l'adresse : http://localhost:3030/.⁠

L'utilisateur par défaut est `admin`, le mot de passe par défaut se situe dans le fichier `compose.yaml` et peut être modifié.

Les datasets sont persistés automatiquement dans le volume `fuseki-data`.