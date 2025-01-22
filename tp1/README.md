SE PLACER DANS LE DOSSIER DOCKER-TPS DANS LE TERMINAL
1 - docker pull mysql:8.0
2 - docker run --name mysql-container -e MYSQL_ROOT_PASSWORD=root -p 3306:3306 -d mysql:8.0
3 - docker cp ./tp1/app.sql mysql-container:/app.sql
4 - docker exec -it mysql-container mysql -u root -p
PASSWORD : root
5 - source /app.sql;
VERIFICATIONS :
- SHOW DATABASES;
- USE beer;
- SHOW TABLES;