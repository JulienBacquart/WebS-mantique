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

Executer la commande suivante :

`tarql-1.2/bin/tarql --dedup 100000 transform.sparql > output.ttl`