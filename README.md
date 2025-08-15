# Hello Java Maven Project

## Overview
This is a simple Java project demonstrating how to build a Maven project using Jenkins.  
It prints a "Hello, Jenkins + Maven!" message when run.

---

## Project Structure
hello-java-maven/
├── pom.xml
└── src/
└── main/
└── java/
└── HelloWorld.java

yaml
Copy
Edit

- **HelloWorld.java** – Main Java class that prints the message.  
- **pom.xml** – Maven configuration file defining project build settings.

---

## Prerequisites
- Java JDK 8 or 11  
- Maven (configured in Jenkins or installed locally)  
- Jenkins (installed locally or via Docker)  
- Git (optional, if using a remote repo)

---

## How to Build

### Using Maven locally:
```bash
mvn clean package
Using Jenkins:
Configure Maven in Manage Jenkins → Global Tool Configuration

Create a Freestyle Jenkins job

Add Build → Invoke top-level Maven targets

Set Goals:

go
Copy
Edit
clean package
Save and Build Now

Check the console output → You should see:

csharp
Copy
Edit
[INFO] BUILD SUCCESS
Output
After a successful build, the compiled JAR will be located in:

bash
Copy
Edit
target/hello-1.0.jar
Run it locally:

bash
Copy
Edit
java -cp target/hello-1.0.jar HelloWorld
Expected output:

Copy
Edit
Hello, Jenkins + Maven!
Author
Arun Raj

css
Copy
Edit
