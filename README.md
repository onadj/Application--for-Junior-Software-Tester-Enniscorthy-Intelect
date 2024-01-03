# Application--for-Junior-Software-Tester-Enniscorthy-Intellect 


Junior Tester Spring Boot Project - Enniscorthy Intellect

Description
This repository contains a basic Spring Boot project for Intellect, designed specifically for Junior Software Testers in Enniscorthy.
presentation: https://www.youtube.com/watch?v=HCcsW-VOPik

Getting Started
Follow these steps to set up and run the project:

Step 1: Visit Spring Initializr
Go to Spring Initializr in your web browser.

Step 2: Configure Your Project
Fill in Project Metadata:

Group: Your company's domain name reversed (e.g., com.example).
Artifact: Name of your project (e.g., myproject).
Packaging: Leave it as the default (Jar is fine).
Java: Choose the Java version you want to use (e.g., 8, 11, 16).
Add Dependencies:

In the "Dependencies" section, type "Spring Web" in the search box.
Select "Spring Web" to include the necessary dependencies for building a web application.
Generate and Download:

Click on the "Generate" button.
Download the generated zip file.
Setup in GITPOD
Open GITPOD and create a new workplace.
Clone the repository: https://github.com/onadj/Junior-Software-Tester-Enniscorthy.
Extract the downloaded zip file and move the contents to the GITPOD workspace.


Update build.gradle and Build
Update build.gradle with the provided script.

bash
Copy code
plugins {
    id 'org.springframework.boot' version '2.7.0'
    id 'io.spring.dependency-management' version '1.0.11.RELEASE'
    id 'java'
}

group = 'com.example'
version = '0.0.1-SNAPSHOT'
sourceCompatibility = '11'

repositories {
    mavenCentral()
}

dependencies {
    implementation 'org.springframework.boot:spring-boot-starter-web'
    testImplementation 'org.springframework.boot:spring-boot-starter-test'
}

tasks.named('test') {
    useJUnitPlatform()
}


Make the Gradlew script executable:
bash
Copy code
chmod +x gradlew
Build the project:

bash
Copy code
./gradlew build


Test with Postman
Use Postman with the created URL from GITPOD. Append /api/hello to the end of the link.
The expected response in Postman should be: "Hello, this is a test from the Spring BasicBoot application developed with Oliver Nad."
