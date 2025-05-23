# Hello Java Maven Jenkins Build 🚀

This project is part of my DevOps internship task to demonstrate building a simple Java application using **Maven** and **Jenkins** (via Freestyle job). It shows how to automate a basic build process using Continuous Integration principles.

---

## 📂 Project Structure

hello-java-maven/
├── pom.xml
├── src/
│ └── main/
│ └── java/
│ └── HelloWorld.java
└── jenkins-build-success.png

yaml
Copy
Edit

---

## 🧠 Objective

✅ Learn how to:
- Set up a Jenkins Freestyle job
- Run a Java Maven build job
- Use Jenkins to automate `clean package` build
- Interpret Jenkins Console Output

---

## 🛠 Tools Used

| Tool      | Version    |
|-----------|------------|
| Java JDK  | 8 or 11    |
| Maven     | 3.8.1      |
| Jenkins   | LTS (via Docker) |
| Git       | Latest     |

---

## 📌 Steps Performed

### 1. Java HelloWorld App
```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, Jenkins + Maven!");
    }
}
2. pom.xml for Maven Build
Includes maven-compiler-plugin to compile Java 1.8 source and generate a JAR.

3. Jenkins Setup via Docker
bash
Copy
Edit
docker run -d --name jenkins-devops -p 8080:8080 -p 50000:50000 jenkins/jenkins:lts

4. Jenkins Configuration
Installed Maven in Global Tool Configuration

Created a Freestyle Project named hello-java-maven

Build Step:

Invoke top-level Maven targets

Goals: clean package

5. Built the Job
Triggered build manually via Build Now

Build completed successfully ✅

