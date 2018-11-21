# Install MongoDB on MacOS

This procedure explains how to install **MongoDB** using **Homebrew** on **MacOS**

## Install MongoDB

* Install **MongoDB**: `$ brew install mongodb`
* Install **Homebrew services**: `$ brew tap homebrew/services`

## MongoDB Setup (Where Mongo data files will live)

* Create the directory where you want to store the data files (In my case I choose my Home folder): `$ mkdir -p /data/db`
* Assign correct permissions: ```$ sudo chown -R `id -un` /data/db
                                 $ # Enter your password```

## Run MongoDB and configure Auto Start MongoDB on System Startup

* Load and start **MongoDB service**: `$ brew services start mongodb`
* Verify **MongoDB service** is up and running: `$ brew services list`

## Run MongoDB

* Run the Mongo Shell `$ mongo`
* Exit the Mongo shell run `> quit()`

## Notes

- If you don't want/need a background service you can just run: `mongod --config /usr/local/etc/mongod.conf`
  - To stop the Mongo daemon hit ctrl-c
