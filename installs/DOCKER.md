# Install Docker

We can install docker on most platforms. We will install it locally to develop
with, and our server(s) later.

## Ubuntu

- This for `16 Xenial`, `17 Aardvark`, or `18 Bionic`.
- For Mac, visit [install Docker for Mac](https://docs.docker.com/docker-for-mac/install/)
- For Windows, visit [install Docker for Windows](https://docs.docker.com/docker-for-windows/install/)


```sh
sudo apt-get install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) stable"
sudo apt-get update && sudo apt-get install docker-ce
```

# Docker on Ubuntu Mint 19

There is no "Tara" release (the Mint release), but Mint 19 is built
on Ubuntu 18 LTS so we simple change the `lsb_release` command to `bionic`.

```sh
sudo apt-get install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   bionic stable"
sudo apt-get update && sudo apt-get install docker-ce
```

## User Permissions

Allow our user to run docker without sudo each time.

```sh
usermod -aG docker $USER
```

You have to re-login to the OS for this to take effect.
# Install Docker Compose

Docker compose is a useful tool for defining a docker-compose.yml file and
easily turning up a machine without having to know many commands.

- Mac: [Docker-Compose](https://docs.docker.com/docker-for-mac/install/)
- Windows: [Docker-Compose](https://docs.docker.com/docker-for-windows/install/)
  - If you still have issues try Docker Toolbox from [this page](https://docs.docker.com/compose/install/#prerequisites)
- Linux: Run the commands below...

```sh
sudo curl -L https://github.com/docker/compose/releases/download/1.21.2/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose
```

At any rate, you should be able to type `docker-compose` and get a long list.

