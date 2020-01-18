# IAW_Project1_OnlineClothingStore
IAW - Project 1 - Online Clothing Store

## Permisos fitxers
sudo chmod -R go+w .
Perque els crea l'usuari www-data, i no tenim Permisos

## Fer mysql persistent
volumes: ['./db_data:/var/lib/mysql']

## Canviar domini
https://wpengine.com/resources/change-domains-wordpress/

A wp-config.php, afegir:
define('WP_HOME','https://8080-dot-4382183-dot-devshell.appspot.com');
define('WP_SITEURL','https://8080-dot-4382183-dot-devshell.appspot.com');

A wp-config.php, afegir, per evitar redirecció a 127.0.0.1 (https://stackoverflow.com/questions/37149842/redirect-to-127-0-0-1-when-access-a-wordpress-hosted-with-apache-and-nginx-in-pr):
$_SERVER['HTTP_HOST'] = $_SERVER['HTTP_X_FORWARDED_HOST'];