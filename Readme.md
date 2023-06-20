# Installation of Dependencies

This guide covers the installation of necessary dependencies including OpenJDK and Maven.

<p>Install the OpenJDK 11 Java Runtime Environment (JRE).</p>

```
sudo apt update && sudo apt install -y openjdk-11-jre
```



<p>Install Maven, which is a build automation tool used primarily for Java projects.</p>

```
sudo apt install -y maven
```

# Setup and Build the Java Spring Boot Project

This guide covers cloning the repository, navigating to the project directory, and building the project.

## Cloning the Repository

Clone the desired git repository.
```
git clone https://github.com/Tushar-ops23/Jenkins-Zero-To-Hero.git
```
<p>Navigate to the Project Directory</p>

Change directories to the Spring Boot project directory.
```
cd Jenkins-Zero-To-Hero/springboot/
```
Building the Project

Use Maven to clean and package the project.
```
./mvnw clean package
```

Load Environment Variables

Source the ~/.bash_profile file to ensure that any necessary environment variables are loaded.

```
source ~/.bash_profile
```


### 03-configure-nginx-and-run.md

<p>Configure Nginx and Run the Application</p>

This guide covers configuring Nginx, running the Java Spring Boot application, and restarting the Nginx service.
```
sudo apt install nginx -y
```
## Navigate to the Target Directory
```
cd target/
```
Running the Application

Run the packaged jar file.

```
java -jar spring-boot-web.jar &
```
Configure Nginx

Navigate to the Nginx configuration directory and edit the default configuration file. Do this manually.
```
cd /etc/nginx/sites-available/
sudo nano default
```
Copy the Jar File to the Web Server Root Directory

```
sudo cp ~/Jenkins-Zero-To-Hero/springboot/target/spring-boot-web.jar /var/www/html/
```
Create a Symlink for the Nginx Configuration
```
sudo ln -s /etc/nginx/sites-available/default /etc/nginx/sites-enabled/
```
Restart Nginx Service
```
sudo systemctl service nginx restart
```
