---
title: "How to Setup Aspose.Email Cloud SDK for Java"
type: docs
url: /how-to-setup-aspose-email-cloud-sdk-for-java/
weight: 10
---

You can directly include the source code of Aspose.Email Cloud SDK for Java in your own project, the source code is available from <https://github.com/aspose-email/Aspose.Email-for-Cloud>.

Alternatively, you can use Maven to include in your Java project. Below are the steps for Maven.
## **Aspose Maven Repository**
```java

<repositories>

    <repository>

        <id>aspose-maven-repository</id>

        <name>Aspose Maven Repository</name>

        <url>http://repository.aspose.cloud/repo/</url>

    </repository>

</repositories>

```
## **Maven Dependency**
```java

<dependency>

      <groupId>com.aspose</groupId>

      <artifactId>aspose-email-cloud</artifactId>

      <version>latest</version>

</dependency>

```
## **Get Sources and Javadocs**
### **Maven**
```java

$ mvn dependency:sources

$ mvn dependency:resolve -Dclassifier=javadoc

```
### **Eclipse IDE**
```java

$ mvn eclipse:eclipse -DdownloadSources=true

$ mvn eclipse:eclipse -DdownloadSources=true -DdownloadJavadocs=false

```
### **pom.xml**
```java

  <build>

    <plugins>

      <plugin>

        <groupId>org.apache.maven.plugins</groupId>

        <artifactId>maven-eclipse-plugin</artifactId>

        <configuration>

            <downloadSources>true</downloadSources>

            <downloadJavadocs>false</downloadJavadocs>

        </configuration>

      </plugin>

    </plugins>

   </build>

```
## **Direct Download**
<http://repository.aspose.cloud/repo/com/aspose/aspose-email-cloud/>
