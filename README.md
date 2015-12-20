# TTPR:  TTP Registry
This is a small application built for our institution's pathology department to store and easily search for TTP patients for data analysis.  Feel free to use it if you would like.

## A Note on Installation
The system only needs a web server running PHP (we use PHP-FPM specifically) and a MySQL compatible database (we use MariaDB).  After that, follow the steps below:

1. Copy files in this repository to your web root
2. Load the 'ttpr.sql' file  into your database.  For MariaDB and MySQL in Linux distros, the following command will work:

  ```bash
  mysql -u root -p < ttpr.sql
  ```
3. Load the 'php-login-admin/_installation/01-create-database.sql' and 'php-login-admin/_installation/02-create-user-table.sql' files (in that order) into your database.  Again, for MariaDB and MySQL in Linux distros, the following commands will work:

  ```bash
  mysql -u root -p < 01-create-database.sql
  mysql -u root -p < 02-create-user-table.sql
  ```

4. Change the information in 'php-login-admin/config.php.default' and 'includes/db.php.default' to meet your system's credentials and rename to 'php-login-admin/config.php' and 'includes/db.php' respectively
