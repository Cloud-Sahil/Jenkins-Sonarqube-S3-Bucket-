# Jenkins + SonarQube S3 Bucket 

## 1. Create EC2 Instances
- **Instance 1:** Jenkins (instance type : c7i-flex.large or more) 
- **Instance 2:** SonarQube  (instance type : c7i-flex.large or more)

## 2. Setup Jenkins EC2 Server

### Go To Root 
```sh
sudo -i
```

### Update Instance
```sh
apt update
```
### Install Java 17
```bash
apt install openjdk-17-jdk -y
```
### Install Maven
```bash
apt install maven -y
```
### Install Jenkins

Follow official Jenkins documentation
👉 [Jenkins Installation](https://www.jenkins.io/doc/book/installing/linux/)

### Install AWS Cli
```sh
snap install aws-cli --classic
```
### Jenkins 
```sh
su - jenkins
```
### Aws Configure

## 3. Setup SonarQube EC2 Server

### Go To Root 
```sh
sudo -i
```

### Update Instance
```sh
apt update
```
### Install Docker
```bash
apt install docker.io -y
```
### Run SonarQube
```bash
docker run -d --name sonarqube-custom -p 9000:9000 sonarqube:10.6-community
```
```sh
docker ps
```
