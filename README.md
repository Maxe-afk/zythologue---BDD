Installation

1. Cloner le dépôt

bashgit clone https://[github.com/SIMPLON-DIST-CDA-260316/zythologue---BDD](https://github.com/Maxe-afk/zythologue---BDD).git
cd zythologue---BDD

2. Lancer PostgreSQL avec Docker

bashdocker compose up -d

Vérifier que le conteneur tourne :

bashdocker ps


Connexion avec DBeaver

Créer une nouvelle connexion PostgreSQL avec les paramètres suivants :

ParamètreValeurHostlocalhostPort5432DatabasezythologueUsernamepostgresPasswordpostgres


Exécution des scripts SQL

Depuis DBeaver, exécuter les scripts dans cet ordre :

sql/01_create_schema.sql   → création des tables
sql/02_seed.sql            → insertion des données de test
sql/03_queries.sql         → requêtes de démonstration


Commandes Docker utiles

bashdocker compose up -d       # Démarrer
docker compose stop        # Arrêter (données conservées)
docker compose start       # Relancer
docker compose down -v     # Supprimer l'environnement et les données
