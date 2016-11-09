# CHALLENGE-TENNIS

# Accès aux données

La base de données est accessible à travers mySQL. Les informations d’accès aux données sont fournies sur Piazza (pour des raisons de sécurité)

Notés que, depuis phpmyadmin, vous pouvez exporter les tables en fichiers CSV


# Structure de la base de données

La base de données est structurées en plusieurs tables décrites ici


# games_atp

C’est la base d’entrainement. Chaque ligne correspond à un match.

ID1_G : L’identifiant du joueur qui a gagné le match <br />
ID2_G : L’identifiant du joueur qui a perdu le match <br />
ID_T_G : L’identifiant du tournoi (voir tours_atp) <br />
ID_R_G : L’identfiant du round dans le tournoi (voir rounds) <br />
RESULT_G ; Le résultat du match <br />
DATE_G:  La date du match <br />


# games_atp_public
C’est la table des matches pour lesquels vous devez prédire le résultat. Les résultats du leaderboard seront calculés sur une partie de ces matches. A la fin du challenge, les résultats sur l’ensemble des matches seront publiés.


# facts_atp
ID1 : L’identifiant du joueur qui a gagné le match <br />
ID2 : L’identifiant du joueur qui a perdu le match <br />
ID_T : L’identifiant du tournoi (voir tours_atp) <br />
ID_R : L’identfiant du extit{round} dans le tournoi (voir rounds) <br />
FS_1 : Nombre de premiers services réussis (joueur 1) <br />
FS_OF1 : Nombre de premiers services (joueur 1) <br />
ACES_1 : Aces (joueur 1) <br />
DF_1 : Double Fautes (joueur 1) <br />
UE_1 : textit{Unforced errors} (erreurs directes ?) <br />
W1S_1: Nombre de points gagnés sur premier service <br />
W1SOF_1: Nombre de points joués sur premier service <br />
W2S_1: Nombre de points gagnés sur second service <br />
W2SOF_1: Nombre de points joués sur second service <br />
WIS_1 : Nombre de points gagnés en tout <br />
BP_1 : Nombre de balles de break gagnées <br />
BPOF_1 : Nombre de balles de break obtenues <br />
RPW_1 : Nombre de points gagnés <br />
RPW_OF1 : Nombre de points jouées <br />
.._2 : Les mêmes pour le joueur 2 <br />


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

ID Joueur 1 <br />
ID Joueur 2 <br />
ID Tournoi <br />
ID Round <br />
Résultat prédit (1 si joueur gagne, 2 si joueur 2)
