# tp-docker-compose-2
tp docker compose 
## Excercice 

### 1 . Running the database and webapp 

- Créer un network séparer pour la database et le webapp ( nommer le docker-compose-webapp) 
- Créer un dockerfile dans le folder database, il faudra :
  - partir d'une image mysql
  - copier le fichier "database.sql" dans `/docker-entrypoint-initdb.d/`
- Lancer un conteneur en detached mode , il faudra: 
  - nommer le conteneur `database`
  - specifier le network que vous avez créer en amont
  - définir une variable d'environnement `MYSQL_ROOT_PASSWORD` 
- Créer un dockerfile dans webapp, il faudra : 
  - partir d'une image python slim
  - définir votre workspace /app
  - installer les packages python ( pip install - requirements.txt)
  - embarquer le contenu du folder webapp dans l'image
  - exposer le port 80
  - executer le script server.py au lancement de votre conteneur

- Lancer un conteneur en detached mode, il faudra :
  - nommer le conteneur webapp
  - specifier le network que vous avez créer en amont

- Vous pouvez lancer votre browser et aller dans http://localhost:8080 pour voir le résultat. 

## 2 . Running with Docker Compose 

Creer un docker-compose.yml pour lancer le webapp et la database.

