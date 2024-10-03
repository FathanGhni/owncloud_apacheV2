# OWNCLOUD BY DJNCLOUD
# TUTORIAL INSTALLATION
Bangun container nya :
```
docker compose up -d --build
```
setelah itu :
```
docker exec -it php_cloud bash
```
setelah itu atur dulu pada folder config/config.sample.app
```
/**
 * Define the database server host name
 * For example `localhost`, `hostname`, `hostname.example.com`, or the IP address.
 * To specify a port use: `hostname:####`;
 * To specify a Unix socket use: `localhost:/path/to/socket`.
 */
'dbhost' => 'db_cloud',

/**
 * Define the ownCloud database name
 * The name of the ownCloud database which is set during installation.
 * You should not need to change this.
 */
'dbname' => 'owncloud',

/**
 * Define the ownCloud database user
 * This must be unique across ownCloud instances using the same SQL database.
 * This is set up during installation, so you shouldn't need to change it.
 */
'dbuser' => 'root',

/**
 * Define the password for the database user
 * This is set up during installation, so you shouldn't need to change it.
 */
'dbpassword' => '123',

/**
 * Define the prefix for the ownCloud tables in the database
 */
'dbtableprefix' => 'oc_',

```

setelah itu silahkan ekskusi : 
```
# Buat direktori data jika belum ada
mkdir -p /var/www/html/data

# Buat direktori apps-external jika belum ada
mkdir -p /var/www/html/apps-external

# Berikan izin yang tepat setelah membuat direktori
chown -R www-data:www-data /var/www/html/data
chmod -R 755 /var/www/html/data

chown -R www-data:www-data /var/www/html/apps-external
chmod -R 755 /var/www/html/apps-external
```

setelah itu sebelum ekskusi ini: 
```
chown -R www-data:www-data /var/www/html/config
chmod -R 755 /var/www/html/config
```



