# CHALLENGE-TENNIS

# Accès aux données

La base de données est accessible à travers mySQL. Les informations d’accès aux données sont fournies sur Piazza (pour des raisons de sécurité)

Notés que, depuis phpmyadmin, vous pouvez exporter les tables en fichiers CSV

# Structure de la base de données

La base de données est structurées en plusieurs tables décrites ici

# games_atp

C’est la base d’entrainement. Chaque ligne correspond à un match.

ID1_G : L’identifiant du joueur qui a gagné le match
ID2_G : L’identifiant du joueur qui a perdu le match
ID_T_G : L’identifiant du tournoi (voir tours_atp)
ID_R_G : L’identfiant du round dans le tournoi (voir rounds)
RESULT_G ; Le résultat du match
DATE_G:  La date du match

# games_atp_public
C’est la table des matches pour lesquels vous devez prédire le résultat. Les résultats du leaderboard seront calculés sur une partie de ces matches. A la fin du challenge, les résultats sur l’ensemble des matches seront publiés.

# facts_atp
ID1 : L’identifiant du joueur qui a gagné le match
ID2 : L’identifiant du joueur qui a perdu le match
ID_T : L’identifiant du tournoi (voir tours_atp)
ID_R : L’identfiant du extit{round} dans le tournoi (voir rounds)
FS_1 : Nombre de premiers services réussis (joueur 1)
FS_OF1 : Nombre de premiers services (joueur 1)
ACES_1 : Aces (joueur 1)
DF_1 : Double Fautes (joueur 1)
UE_1 : textit{Unforced errors} (erreurs directes ?)
W1S_1: Nombre de points gagnés sur premier service
W1SOF_1: Nombre de points joués sur premier service
W2S_1: Nombre de points gagnés sur second service
W2SOF_1: Nombre de points joués sur second service
WIS_1 : Nombre de points gagnés en tout
BP_1 : Nombre de balles de break gagnées
BPOF_1 : Nombre de balles de break obtenues
RPW_1 : Nombre de points gagnés
RPW_OF1 : Nombre de points jouées
.._2 : Les mêmes pour le joueur 2

# players_atp
La mapping entre les identifiants et les noms des joueurs. Contient aussi quelques informations additionnelles.

# ratings_atp
Contient le classement et le nombre de points ATP des jours à différentes dates

# rounds
Permet de matcher un identifiant de round à un type de round

# courts
Permet d’associer une type court à sa surface réelle

# tours_atp
Description des différents tournois. NB: la date du tournoi peut être utilisée comme date de match si un matche n’est pas associè à une date

# Soumission sur le leaderboard
Le site du leaderboard se trouve à l’adresse suivante: (voir PIAZZA)

Le fichier de soumission est CSV (valeurs séparées par des ‘,’) de 5 colonnes:

ID Joueur 1
ID Joueur 2
ID Tournoi
ID Round
Résultat prédit (1 si joueur gagne, 2 si joueur 2)
