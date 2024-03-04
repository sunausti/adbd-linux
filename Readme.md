# Limitation
Openssl version < 1.1, must be 1.0, as the 1.1 has broken API

# Info
Base on:https://github.com/hadess/adbd

Modify for Yocto building and common Linux based OS.

# Compiling in normal Linux OS
```
RANLIB=ranlib AR=ar CXX=g++ CC=gcc make
```
# Compiling in Docker
## run docker
```
docker run -it -v <pwd>:<pwd> --network host --privileged --name adbd-linux-build ubuntu:16.04
```
## in docker install 
```
apt update && apt install openssl build-essential libssl-dev libcap-dev pkg-config libglib2.0-dev -y

```
 ## Compiling in normal Linux OS
```
RANLIB=ranlib AR=ar CXX=g++ CC=gcc make
```
