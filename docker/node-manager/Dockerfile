FROM node:15.3.0

RUN apt-get update && apt-get install -y mysql-server-8.0

RUN service mysql start && mysql -e "ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'motdepasse'; FLUSH PRIVILEGES;"

WORKDIR /app

COPY . .

RUN npm install

CMD ["node", "app.js"]