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

#### Third Party Resources
<b>AWS Lightsail</b> - Server Instance <br>
Apache HTTP Server / Mod_WSGI - Web Server
