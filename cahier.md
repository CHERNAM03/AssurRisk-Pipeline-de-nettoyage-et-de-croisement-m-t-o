
# JOUR 1 — LUNDI 9 : combien de fois faut-il cliquer ?

# Exercice 1 — Remise en main

# 1.Lancez rappel_22_octobre.py

# 2.Montrez à votre binôme
On a une liste de taille 4 dont le premier élement d'index 0 est Réinitialiser la base
Un dictionnaire des ensembles de clés valeur

# 3 Ajoutez une étape à la liste etapes avec append , et une paire au dictionnaire
# fichiers . Relancez. Où apparaissent-elles ?
 cela a été fait dans le code ci-dessus, cela apparait à la fin comme étant le dernier 
 élément de la liste et le dernier élément du dictionnaire.

# 4 Affichez etapes[0] , puis etapes[2] , puis etapes[12] . Lisez le message
# d’erreur de la troisième : dernière ligne, fichier, numéro de ligne.

On a un message d'erreur de type IndexError au niveau de la ligne 23 et au niveau de etapes
car une étape d'index 12 n'existe pas dans la liste que nous avons

# 5 Retirez .items() dans la dernière boucle, relancez, lisez l’erreur, remettez-le.
 On a un message d'erreur de type ValueError au niveau de la ligne 61 et au niveau de la boucle for.

# 6 Enlevez les quatre espaces devant une ligne de boucle, relancez, lisez le
# message, remettez-les.

On a un message d'erreur de type IndentationError au niveau de la ligne 62 et au niveau de la boucle for.

# 7. Écrivez dans votre cahier, en une phrase : à quoi sert une boucle ?

Une boucle sert à répéter automatiquement les mêmes instructions pour chaque élément d’une liste ou d’une collection, sans réécrire le code à chaque fois.

# Exercice 2 — L’inventaire, chronomètre en main

travail en binome, effectué avec Raoul Zamble, le rendu a été écrit dans son cahier

# 3. Ajoutez une étape
Avec la methode append, l’étape apparaîtra dans la liste et dans la boucle qui affiche les tâches.
la paire apparaîtra dans la boucle qui parcourt le dictionnaire.

# Exercice 2 — L’inventaire, chronomètre en main 

# Exercice 3
En deux secondes, le script m'a permis de me connecter à la base de données dans dbeaver et la base a été réinitilisée.
Une premiére vérification de la table fact sinitre dans Dbeaver avec un select count(*) from fact_sinistre me donne 12490 ligne ou enregistrements

2. Ce qui apparaît à l’écran est que la connexion est ouverte et que la base a été réinitialisée.
pas 
 3. Si on retire la ligne connexion.autocommit = True , j'ai pas remarqué de changement notoire , à par la connexion à dbeaver a pris plus de temps, mais les modifications ne seront pas enregistrées dans la base de données car on n'a pas validé la transaction.
# Exercice 4

Recopiez les trois lignes ci-dessus et répondez aux trois questions qu’elles posent.
Aprés avoir recopier les lgnes indiquées on a :
--- On a une liste class
--- avec 30 objets
--- des dictionnaires ayant comme clés
 dict_keys(['latitude', 'longitude', 'daily'])


 ## Les questions, et elles comptent plus que le code : 
 1. meteo.shape
donne deux nombres. Lequel est le nombre de lignes ? 
le premier donne le nombre de logne, ici on 21930 et 8 colonnes

 2. Vous attendiez-vous à ce nombre ? 30 villes × combien de
jours ?
 3. Qu’est-ce que morceaux.append(tableau) fait exactement ? Et
pourquoi morceaux est-il créé avant la boucle ?
 À chaque tour de boucle (pour chaque ville), le script fabrique un petit bout de tableau et le range dans la boîte nommée morceaux. À la fin des 30 tours, notre boîte va contenir 30 petits tableaux côte à côte.


01_init.sql
02_clean.sql
03_tables_meteo.sql
04_rattachement.sql
05_croisement.sql
06_controles.sql


# JOUR 2 — MARDI 10 : la chaîne s’enchaîne toute seule

## Exercice 1 — Ranger et numéroter 

Dans sql/ , mes fichiers des briefs précédents sont déjà là. Je les numérote dans l’ordre où ils doivent tourner, et je les ai renommé.

La question, et elle n’est pas technique : pourquoi 04_rattachement.sql
ne peut-il pas tourner avant que la météo soit chargée ?

Par ce que c'est un  fichier qui permet d'associer chaque couple latitude/longitude retourné par Open-Meteo
 à la ville de référence la plus proche.


 Et celle-ci : qu’est-ce qui se passerait si on lançait 02_clean.sql avant
01_init.sql ? Essayez. Lisez l’erreur. C’est une bonne erreur à avoir vue une
fois.
Pour tester l'execution avant l'initialisation, je me connecte, d'abord, dans Dbeaver, j'ouvre 02_clean.sql, puis je choisis SQL - Editor Execute SQL Script. LMe script a échoué  dés qu'il tente de lire dim_agence, car cette table n'existre pas. 

Pour que le nettoyage s’exécute correctement, lance d’abord 01_ini.sql, puis 02_clean.sql. Le fichier 02_clean.sql crée plusieurs tables clean_* à partir des tables sources; il ne peut donc pas fonctionner avant leur création.

## Exercice 2 — La liste et la boucle


# Puis ajoutez-en une quatrième. Combien de lignes avez-vous écrites pour ça ?

Pour effectuer cette tache j'ai ecris une seule ligne, on a une liste, pour ce faire on a utilisé la méthode append.

# Exercice 3 — Premier lancement complet
base reinitialisee
<class 'list'>
30
dict_keys(['latitude', 'longitude', 'daily'])
(21930, 8)
 [SQL] Reinitialiser la base
 [SQL] Construire la couche propre
 [SQL] Creer les tables qui attendent la meteo
 [SQL] Rattacher la météo aux sinistres
 [SQL] Croiser les sinistres et la météo
 [SQL] Contrôler le résultat

# Exercice 4 — Le journal : chaque étape dit ce qu’elle a fait

## Ouvrez journal_pipeline.csv dans Excel. Quelle étape prend le plus de temps ? Vous attendiez-vous à celle-là ?

La réinitialisation prend le plsunde temps avec !
01_init.sql;Reinitialiser la base;SQL;156,8
02_clean.sql;Construire la couche propre;SQL;36,1
03_tables_meteo.sql;Creer les tables qui attendent la meteo;SQL;0,0
04_rattachement.sql;Rattacher la météo aux sinistres;SQL;0,0
05_croisement.sql;Croiser les sinistres et la météo;SQL;0,1
06_controles.sql;Contrôler le résultat;SQL;0,0


# Exercice 5 — Contrôler après chaque étape, pas à la fin

Contexte
 Mise en place de contrôles intermédiaires (assertions / comptages de lignes) dans le pipeline SQL AssurRisk1
 (notamment après 02_clean.sql) pour valider la qualité et l'intégrité des données à chaque maillon de la chaîne de transformation.

### Trois questions :
#### 1. Combien de lignes attendiez-vous dans clean_fact_sinistre avant de lancer ? Et combien en avez-vous obtenu ? 
 
Q1 : Combien de lignes attendiez-vous dans clean_fact_sinistre avant de lancer ? Et combien en avez-vous obtenu ?je m'attendais à moins que ce que j'ai eu dés le départ dans fact_sinistre, c'est à dire  12490 lignes et aprés le controle on se retrouve avec 12098. En bref : le nettoyage a produit une table de 12 098 sinistres.

Attendu : Environ [12490] lignes (correspondant au nombre de lignes de la table brute de départ, moins les doublons évidents et les enregistrements présentant des valeurs aberrantes ou manquantes majeures).

Obtenu : [12098] lignes après l'exécution de 02_clean.sql.

Constat : Le résultat est conforme aux attentes, en effet aprées nettoyage 392 ( 100 doublons, 80 anomalies sur la date de survenance, 100 contrats non actifs au moment du sinistre, localisations manquantes 60, montants anormaux 50 et libellés non standardisés (correction appliquée)) lignes ont été exclues de la table.

#### 2.Si ce nombre était faux, quelle étape soupçonneriez-vous en premier ?
Q2 : Si ce nombre était faux, quelle étape soupçonneriez-vous en premier ?
Si le nombre de lignes s'avérait anormal (trop bas ou anormalement haut) :

Le script 02_clean.sql lui-même : En particulier les conditions de filtrage (WHERE), les critères de suppression des doublons (DISTINCT ou ROW_NUMBER), ou des jointures mal ficelées qui auraient créé un produit cartésien ou éliminé à tort des lignes valides (sur-filtrage).

La qualité de la source en amont (01_ini.sql) : Si les données brutes ont changé ou si le chargement initial a omis des données.



#### 3. Un contrôle placé seulement à la fin vous dirait qu’il y a un problème. Que ne vous dirait-il pas ?

Q3 : Un contrôle placé seulement à la fin vous dirait qu’il y a un problème. Que ne vous dirait-il pas ?
Un contrôle unique en fin de pipeline indique qu'il y a une anomalie dans le résultat final, mais il ne permet pas de localiser l'origine de l'erreur.

Plus précisément, il ne dit pas :

Où dans la chaîne de traitement le problème s'est produit (est-ce 02_clean.sql, l'intégration météo, ou le croisement final ?).

Pourquoi la règle de gestion a échoué (est-ce un problème de jointure, un filtre trop agressif, ou une corruption de données ?).

Cela oblige à reprendre le pipeline de zéro et à enquêter à l'aveugle, alors qu'un contrôle intermédiaire cloisonne l'erreur à une étape précise dès son apparition.

## Mise en commun — quel contrôle attrape quoi

#### Elle résume les différents types de contrôles que l'on peut placer dans un pipeline de données et le type d'anomalie spécifique que chacun permet d'intercepter.

|****************************************************************************************************|
|  Type de contrôle      | À quel moment / Où ?                 | Ce qu'il attrape (Anomalie ciblée) |
|****************************************************************************************************|
| Contrôle de volumétrie |  Après une étape de nettoyage        |Une table vide(rupture deflux)      |
|(Comptage de lignes)    |  (02_clean.sql) ou de transformation |                                    |
|****************************************************************************************************|
| Contrôle d'intégrité   |Après un croisement ou une jointure   | Des enregistrements perdus lors    |
| / Clés orphelines      | (ex: 03_croisement.sql)              | d'une jointure, doublons, etc..    |
|****************************************************************************************************|
| Contrôle de valeurs nulles| Sur des colonnes critiques ex:     | Des données corrompues ou mal     |
|                           | montants de sinistres,dates,Id     | formatées en amont                |
|****************************************************************************************************|
| Contrôle de cohérence     |Sur des métriques (ex: un montant   |Des erreurs de logique métier dans |
| Plages de valeurs         | négatif, une température aberrante)|les scripts SQL                    |
|*****************************************************************************************************       


# JOUR 3 — JEUDI 12 : la météo entre dans la chaîne

## 


# Exercice 1 — Du JSON à la base · 70 min

#### Faites la même chose pour villes_coordonnees_meteo.csv .
#### Puis, dans DBeaver, comptez les lignes des deux tables.

|*************************************|
|meteo_assurrisk              |	21930 |
|villes_coordonnees_meteo     |	31    |
|meteo_assurrisk_ville	      |21930  |
|fact_sinistre_meteo	      |12098  |
**************************************|

Effectivement on a une ligne de plus dans la table coordonnées villes avec 31 lignes au lieu de 30
Au niveau de ligne 30, on a Inconnu, NULL, NULL oubli ou erreur de saisie.

# Exercice 2 — La garde : 

#### Écrivez d’abord, en français, dans votre cahier : en une phrase, que doit faire
#### le script avant d’appeler l’API ?

Avant d’appeler l’API, le script doit lire les coordonnées des villes à interroger et créer 
les tables PostgreSQL qui recevront les données météo.

##### La question : vous êtes quinze dans la salle. Si chacun lance son pipeline
##### en même temps sans cette garde, que se passe-t-il ? Et avec la garde ?
L'api pourrait mettre du temps à répondre, trop de requetes en meme temps, et la garde nous permettrait 
d'échapper à cette lourdeur.


# Exercice 3 — Brancher la météo au bon endroit 

On peut techniquement tout mettre dans une seule boucle, mais la boucle du mardi suppose que chaque étape est un fichier SQL à lire puis à exécuter. L’étape météo est du Python (pandas et COPY via le curseur), pas un fichier SQL : elle ne suit donc pas la même procédure.
Séparer les boucles rend aussi explicite qu’elle doit se placer entre la création des tables et le rattachement.

# Exercice 4 — Le rattachement et le croisement rejoignent la chaîne 
Ils seront donc exécutés après le chargement Python des données météo et des coordonnées.



# JOUR 4 — VENDREDI 13 : livrer, et montrer

# Exercice 1 — Le pipeline range derrière lui

#### La question : pourquoi exist_ok=True ? (Retirez-le, lancez deux fois, lisez l’erreur, remettez-le.)
type d'erreur : FileExistsError: [WinError 183] Impossible de créer un fichier déjà existant: 'sorties'
drop table if exist en SQL



# Exercice 3 — Cassez une étape exprès:
## Trois questions : 
1. À quel moment le pipeline s’arrête-t-il ?
  Le journal_pipeline.csv ne contient que ses en-têtes : aucune étape n’y a été enregistrée. Le script écrit le journal seulement à la fin; il s’est donc probablement arrêté avant cette écriture. Le fichier seul ne permet pas de savoir à quelle ligne. Il faut regarder le traceback affiché dans le terminal pour trouver l’erreur et l’étape concernée.
  Ainsi, on note à la ligne 77  une erreur de type FileNotFoundError: [Errno 2] No such file or directory: 'sql/01_ini.sql'

2. Le journal permet-il de savoir quelle étape a échoué ? 
  Non. Il est vide parce qu’il n’est sauvegardé qu’à la fin. Les messages [SQL] affichés avant l’erreur dans le terminal peuvent toutefois montrer jusqu’où le script est allé.


3. Les étapes précédentes, elles, ont-elles été faites ? Donc dans quel état est la base ?
   Peut-être. Le script active connexion.autocommit = True, donc les commandes terminées avant l’erreur peuvent déjà être enregistrées dans la base. Comme 01_ini.sql réinitialise des tables, la base peut être dans un état partiel : certaines étapes faites, les suivantes non. Ne relance pas le pipeline avant d’avoir relevé le traceback; une nouvelle exécution pourrait réinitialiser encore la base.



 # ======================================================================================================
   Les deux journaux de deux lancements successifs, et une ligne disant ce qui est identique.

 Ainsi le premier lancement donne les resultats suivants:

   fichier;etape;outil;secondes
01_init.sql;Reinitialiser la base;SQL;65,7
02_clean.sql;Construire la couche propre;SQL;14,9
03_tables_meteo.sql;Creer les tables qui attendent la meteo;SQL;0,1
chargement_meteo.py;Charger les données météo et villes;Python;0,2
04_rattachement.sql;Rattacher la météo aux sinistres;SQL;0,1
05_croisement.sql;Croiser les sinistres et la météo;SQL;0,1
06_controles.sql;Contrôler le résultat;SQL;0,0:

# ************************************************************************************************
  le deuxiéme lancement donne les resultats suivants:

  fichier;etape;outil;secondes
01_init.sql;Reinitialiser la base;SQL;114,6
02_clean.sql;Construire la couche propre;SQL;26,6
03_tables_meteo.sql;Creer les tables qui attendent la meteo;SQL;0,1
chargement_meteo.py;Charger les données météo et villes;Python;0,3
04_rattachement.sql;Rattacher la météo aux sinistres;SQL;0,2
05_croisement.sql;Croiser les sinistres et la météo;SQL;0,3
06_controles.sql;Contrôler le résultat;SQL;0,1

La ligne de comparaison peut être : « Les deux lancements ont les mêmes étapes et les mêmes résultats de contrôle; les durées peuvent varier. » Les contrôles actuellement enregistrés sont 12 098 sinistres propres et finaux, 21 930 lignes météo, 30 villes rattachées, 0 sinistre sans météo et 0 doublon météo. Pour affirmer que ces résultats sont identiques sur les deux lancements, il faudra comparer aussi le second fichier controles.csv.




# Franchise : 

La franchise moyenne est d’environ 228,70 €, et la médiane est de 200 € ; elle semble souvent suivre un barème fixe.

# MA CONCLUSION, ET MA CONFIANCE │

confirmée  


# À noter dans le cahier avant de partir

## 1. Ma case 5 de l’enquête sur octobre

Les données confirment qu’octobre 2025 est un mois exceptionnellement chargé en sinistres et que les dégâts des eaux y occupent une part plus importante que le reste de la période. Cela rend mon hypothèse plausible, mais ne prouve pas que les fortes pluies ont causé le pic. Pour la vérifier, il faudrait comparer, pour chaque ville et chaque jour, les dégâts des eaux lors des journées très pluvieuses avec ceux des journées peu ou pas pluvieuses. Ma confiance dans le constat du pic est élevée; ma confiance dans son explication par la pluie reste limitée.

## 2. La phrase de la case 3 qui m’a le plus servi

« Si mon explication est vraie, je devrais voir beaucoup de sinistres liés aux dégâts des eaux concentrés à quelques dates ou dans certaines villes. »

Cette phrase m’a servi parce qu’elle transforme mon idée en un résultat que je peux chercher dans les données : vérifier si les dégâts des eaux se concentrent réellement à certaines dates ou dans certaines villes.

## 3. Une chose que je n’ai pas comprise aujourd’hui

Exemple à garder seulement s’il correspond à ce que je ressens : « Je ne sais pas encore comment comparer les dégâts des eaux des jours très pluvieux à ceux des jours peu ou pas pluvieux, ville par ville. »


# EXERCICE 2 du jeudi

Qu’est-ce qui change d’un appel à l’autre ?
Les valeurs enregistrées : le nom du fichier, le libellé de l’étape, l’outil utilisé ("SQL" ou "Python") et la durée. Ce sont les paramètres de la fonction :

def journaliser_etape(fichier, libelle, outil, duree):

Par exemple, l’appel depuis jouer_sql() fournit "SQL", tandis que celui depuis charger_table() fournit "Python"

Qu’est-ce qui reste identique ?
La structure de la ligne ajoutée au journal :

journal.append([fichier, libelle, outil, duree])

C’est le corps de la fonction : il construit une liste avec ces quatre valeurs et l’ajoute à journal.

## Comment savoir que c'est juste ?

- 1. Déja avec un ctrl + F , je me retrouve avec un journal.append au lieu de trois
- 2. Effectivement, les six contrôles sont identiques à ceux de l’exercice 1.

 contrôle final : sinistres_propres = 12098
 contrôle final : lignes_meteo = 21930
 contrôle final : villes_meteo = 30
 contrôle final : lignes_finales = 12098
 contrôle final : sans_meteo = 0
 contrôle final : meteo_en_double = 0

- 3. Ouvrez sorties/journal_pipeline.csv . La durée de 01_init.sql doit être de plus
de 20 secondes.
 j'ai cela comme resultats : 01_init.sql;Reinitialiser la base;SQL;58,2

