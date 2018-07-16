# Mongo DB

## Linux

Create a default path for mongo data files:
```sh
mkdir -p /data/db && sudo chmod -R 775 /data/
````

Create a Startup File (**Mint 19 Only**)
```sh
# From this directory (Where this file is, run):
sudo cp ./mongodb/mongod.service /etc/systemd/system/ 
sudo chmod +x /etc/systemd/system/mongod.service
```

Ensure we have our dependencies.
```sh
sudo apt-get install libcurl3 openssl -y
```

Now we can add the Mongo key and APT repository (Yes, it says xenial); and install:

```sh
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 9DA31620334BD75D9DCB49F368818C72E52529D4
echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/4.0 multiverse" | \
  sudo tee /etc/apt/sources.list.d/mongodb-org-4.0.list
sudo apt-get update && sudo apt-get install -y mongodb-org
```

Start Service, check Status
```sh
sudo systemctl start mongodb
sudo systemctl status mongodb
```
