# Inventaire des points d'entrée

Le livrable de l'atelier d'analyse. Il dit ce que l'API devra **permettre** — pas comment on
l'écrira.

Une règle : tout ce qui figure ici doit se justifier par la lettre de mission ou par un écran
des maquettes. Si vous ne savez plus d'où vient une ligne, c'est peut-être qu'elle n'en vient
pas. (Seule exception : la section bonus, si vous en ajoutez une.)

---

## Ce que l'utilisateur peut faire

Une action par ligne, en français. Pas encore de chemins.

- Consulter une ville desservie (Connecté ou non)
- Reserver un lancer (Connecté)
- Faire une recherche : Ville depart, Ville arrivée, date, nombre (Connecté ou non)
- Consulter ses informations personnelles (compte) (Connecté)
- Consulter le detail d'un lancer (Connecté ou non)
- Consulter son panier (Connecté)
- Acheter son billet (Connecté)
- Consulter son billet (Connecté)
- Se connecter
- Creer un compte

## Les points d'entrée
| Ce que ça fait | Chemin proposé | Qui peut l'appeler |
|---|---|---|
| Consulter une ville | GET cities/ID | tout le monde |
| Reserver un lancer | POST me/card/slot | user connecté |
| Faire une recherche |  | tout le monde |
| Consulter ses informations personnelles | Get me/account | user connecté |
| consulter le detail d'un lancer | GET launches/{id} | tout le monde |
| Consulter mon panier | GET me/cart | user connecté |
| Acheter un billet |  | user connecté |
| Consulter son billet | GET me/check/{id} | user connecté |
| S'inscrire | Post users | tout le monde |
| Se connecter | Post session | tout le monde |

## Les données qui circulent

Pour chaque point d'entrée : ce qu'il reçoit, ce qu'il renvoie. Nommez les données comme
l'Office les nomme — les traduire en identifiants techniques, c'est le travail de demain.

### <nom du point d'entrée>

## Ce dont on n'est pas sûrs

Les questions que la lettre et les maquettes ne tranchent pas. Une question notée vaut mieux
qu'une réponse inventée.

-
## Règles de gestion de l'Office

- Une seule catapulte par ville
- Pas d'arret en chemin, depart->arrivée
- Masse conditionne la trajectoire
- 1 billet par voyageur
- une fois payé, pas de modifications/remboursements et billet donnés
- Pas de coordonnées bancaires

