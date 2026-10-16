# procedures-cli

Gere tes procedures stockees MySQL comme des migrations.

    composer require --dev mon-vendor/procedures-cli

    vendor/bin/procedures createdb      # cree la base (DB_DATABASE du .env)
    vendor/bin/procedures make nom      # cree database/procedures/xxxx_nom.sql
    vendor/bin/procedures status        # executees / en attente
    vendor/bin/procedures run           # execute seulement ce qui n'est pas execute

Reglages lus dans le .env du projet : DB_HOST, DB_PORT, DB_USERNAME, DB_PASSWORD, DB_DATABASE.
Dossier des fichiers .sql : database/procedures (change avec PROCEDURES_PATH dans .env).
Le suivi est stocke dans la table `sql_procedures` (creee automatiquement).
