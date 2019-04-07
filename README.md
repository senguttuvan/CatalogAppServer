# CatalogAppServer


## Description
Set up a Apache HTTP Web server to deploy the Catalog web application. Also installed and configured a Postgres Database server to work with the web app. 


## Accessing the server

#### IP Address
52.42.245.189

#### SSH Port
2200

#### Public URL
http://catalog.52.42.245.189.nip.io/

#### Software Dependecies
The major required software packages to be installed are PostgreSQL, Python3, flask and sqlalchemy

    apt-get -qqy install make zip unzip postgresql
    apt-get -qqy install python3 python3-pip
    pip3 install --upgrade pip
    pip3 install flask packaging oauth2client redis passlib flask-httpauth
    pip3 install sqlalchemy flask-sqlalchemy psycopg2 bleach requests

#### Setting up server
   Update packages <br>
1. sudo apt-get update
2. sudo apt-get upgrade
3. sudo apt-get autoremove

<br> Set up fire wall<br>
1. sudo ufw allow ssh
2. sudo ufw allow 2222/tcp
3. sudo ufw allow www
4. sudo ufw enable

<br> Set up Apache WSGI server <br>
1. sudo apt-get install apache2
2. sudo apt-get install libapache2-mod-wsgi

<br>Open /etc/apache2/sites-enabled/000-default.conf
<br>Add the following line at the end of the <VirtualHost *:80> block, right before the closing </VirtualHost> line: WSGIScriptAlias / /var/www/html/myapp.wsgi

#### Third Party Resources
https://lightsail.aws.amazon.com/ls/docs/en/articles/lightsail-how-to-set-up-putty-to-connect-using-ssh
https://www.ssh.com/ssh/key/
https://www3.ntu.edu.sg/home/ehchua/programming/sql/PostgreSQL_GetStarted.html
https://knowledge.udacity.com/
https://stackoverflow.com/questions/7695962/postgresql-password-authentication-failed-for-user-postgres
https://serverfault.com/questions/262751/update-ubuntu-10-04/262773#262773
