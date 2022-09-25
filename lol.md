**1. install jdk17**
```shell
sudo apt-get update
sudo apt-get upgrade
sudo apt-apt install openjdk-17-jdk-headless
```
**2. set `JAVA_HOME` path**
- copy these to `bashrc`
```shell
#set JAVA_HOME path
JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64/

export JAVA_HOME

PATH=$JAVA_HOME/bin:$PATH

export PATH" >> ~/.bashrc
```
- use nano 
```shell
nano ~/.bashrc
. ~/.bashrc
```
