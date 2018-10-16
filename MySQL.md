# Install MySQL on MacOS

This procedure explains how to install **MySQL** using **Homebrew** on **MacOS**

## Install MySQL

* Install **MySQL**: `$ brew install mysql`
* Install **Homebrew services**: `$ brew tap homebrew/services`
* Load and start **MySQL service**: `$ brew services start mysql`
* Verify **MySQL service** is up and running: `$ brew services list`
* Verify the installed MySQL instance : `$ mysql -V`.   

### MySQL Setup
Open Terminal and execute the following command to set the root password

 `mysqladmin -u root password 'yourpassword'`
