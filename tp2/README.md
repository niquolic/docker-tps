1 - docker volume create mysqltp2
2 - docker run --name mysql-container -e MYSQL_ROOT_PASSWORD=root -p 3306:3306 -v mysqltp2:/var/lib/mysql -d mysql:8.0
3 - docker cp ./tp1/app.sql mysql-container:/app.sql
4 - docker exec -it mysql-container mysql -u root -p
PASSWORD : root
5 - source /app.sql;
6 - USE beer;
7 - INSERT INTO `continent` VALUES (6, 'ANTARCTIQUE');
8 - SELECT * FROM `continent`;
9 - Supprimer le conteneur
10 - docker run --name mysql-container -e MYSQL_ROOT_PASSWORD=root -p 3306:3306 -v mysqltp2:/var/lib/mysql -d mysql:8.0
11 - docker cp ./tp1/app.sql mysql-container:/app.sql
12 - docker exec -it mysql-container mysql -u root -p
PASSWORD : root
13 - USE beer;
14 - SELECT * FROM `continent`;
Antarctique devrait toujours apparaitre