# Spring Boot based Java web application
# Installation of Dependencies This guide covers the installation of necessary dependencies including OpenJDK and Maven.

<p>Install the OpenJDK 11 Java Runtime Environment (JRE). </p>

```
sudo apt update
sudo apt install -y openjdk-11-jre
```

#Install Maven, which is a build automation tool used primarily for Java projects.
```
sudo apt install -y maven
```
Checkout the repo and move to the directory

```
git clone https://github.com/Tushar-ops23/Jenkins-Zero-To-Hero.git

```
Change directories to the Spring Boot project directory.

```
cd Jenkins-Zero-To-Hero/springboot/
```

Execute the Maven targets to generate the artifacts

```
mvn clean package
```
Load Environment Variables

Source the ~/.bash_profile file to ensure that any necessary environment variables are loaded.
```
source ~/.bash_profile
```


The above maven target stroes the artifacts to the `target` directory. You can either execute the artifact on your local machine.

### Execute locally (Java 11 needed) and access the application on http://localhost:8080

```
java -jar target/spring-boot-web.jar
```
