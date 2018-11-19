# Install Redis on MacOS

This procedure explains how to install **Redis** using **Homebrew** on **MacOS**

## Install Redis

* Install **Redis**: `$ brew install redis`
* Install **Homebrew services**: `$ brew tap homebrew/services`
* Load and start **Redis service**: `$ brew services start redis`
* Verify **Redis service** is up and running: `$ brew services list`

## Notes

- If you don't want/need a background service you can just run:  `redis-server /usr/local/etc/redis.conf`
- Check If the **Redis server** is running: `redis-cli ping`
