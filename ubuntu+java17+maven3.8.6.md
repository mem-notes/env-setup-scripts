**1. install jdk17**
```shell
sudo apt-get update
sudo apt-get upgrade
sudo apt-apt install openjdk-17-jdk-headless
```

**2. install maven 3.8.6**
- download from from official site https://maven.apache.org/download.cgi
```shell
wget https://dlcdn.apache.org/maven/maven-3/3.8.6/binaries/apache-maven-3.8.6-bin.tar.gz
#extract file to /opt/
sudo tar -xvf apache-maven-3.8.6-bin.tar.gz -C /opt/
#give current user permission to excute maven
sudo chown -R $USER:$USER /opt/apache-maven-3.8.6
```

**3. set `JAVA_HOME` and `MAVEN_HOME` path**
- copy these to `bashrc`
```shell
#set JAVA_HOME and MAVEN_HOME path
JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64
MAVEN_HOME=/opt/apache-maven-3.8.6

export JAVA_HOME
export MAVEN_HOME

PATH=$JAVA_HOME/bin:$MAVEN_HOME/bin:$PATH

export PATH
```
- use nano 
```shell
nano ~/.bashrc
#then reload
. ~/.bashrc
```
- check new env path using 
```shell
echo $JAVA_HOME
#should output "/usr/lib/jvm/java-17-openjdk-amd64"
echo $MAVEN_HOME
#should output "/opt/apache-maven-3.8.6"
```
- check installations
```shell
mvn -v
```