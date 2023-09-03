# Planning
- [ ] [Learn Selenide tutorial](https://www.youtube.com/watch?v=wN45Qla66-o&list=PLFGoYjJG_fqrvWt1FfHqKoREQmSPxazBq)
      
# What is Selenide & Why to use Selenide?
- It is a Framework for test automation by Selenium web driver : [Officeal Selenide  Documentation](https://selenide.org/)
- [Selenide Java DOc](https://selenide.org/javadoc/current/)
**Advantages:**
  1. Concise fluent API for Tests
  2. Stable Tests
  3. Powerful Selectors
  4. Simple Configuration
- It will solve problems like shutting down the browser, Handel timeouts, and stale element exceptions or searching for relevant log lines, debugging your tests
  
# Initial Setup and First Script
## For Maven:
Add Dependencies in POM.xml File[Follow the Guide to Quick Start setup](https://selenide.org/quick-start.html)

**Selenide**
```Maven
<!-- https://mvnrepository.com/artifact/com.codeborne/selenide -->
<dependency>
    <groupId>com.codeborne</groupId>
    <artifactId>selenide</artifactId>
    <version>6.17.2</version>
</dependency>
```
<details >
<summary> Testing Framework</summary>

**For TestNG**
``` XML
<!-- https://mvnrepository.com/artifact/org.testng/testng -->
<dependency>
    <groupId>org.testng</groupId>
    <artifactId>testng</artifactId>
    <version>7.8.0</version>
    <scope>test</scope>
</dependency>
```
**For JUNIT**
``` XML
<!-- https://mvnrepository.com/artifact/junit/junit -->
<dependency>
    <groupId>junit</groupId>
    <artifactId>junit</artifactId>
    <version>4.13.2</version>
    <scope>test</scope>
</dependency>
```

**for Cucumber**
```XML
<dependencies>
		<!-- https://mvnrepository.com/artifact/io.cucumber/cucumber-java -->
		<dependency>
			<groupId>io.cucumber</groupId>
			<artifactId>cucumber-java</artifactId>
			<version>7.4.1</version>
		</dependency>
		<!-- https://mvnrepository.com/artifact/io.cucumber/cucumber-junit -->
		<dependency>
			<groupId>io.cucumber</groupId>
			<artifactId>cucumber-junit</artifactId>
			<version>7.3.3</version>
			<scope>test</scope>
		</dependency>
		<!-- https://mvnrepository.com/artifact/io.cucumber/cucumber-core -->
		<dependency>
			<groupId>io.cucumber</groupId>
			<artifactId>cucumber-core</artifactId>
			<version>7.13.0</version>
		</dependency>

	</dependencies>
```

</details>

## For Gradel:
**Selenoid**
```Gradel
dependencies {
  testImplementation 'com.codeborne:selenide:6.17.2'
}
```

## First Script
Create a maven or gradel project in Eclipse or IntelliJ Idea and 
**Import required static class**
```Java
import static com.codeborne.selenide.Selenide.*;
import static com.codeborne.selenide.Condition.*;
```
**Write Class**
```Java
@Test
public void userCanLoginByUsername() {
  open("/login");
  $(By.name("user.name")).setValue("johny");
  $("#submit").click();
  $(".loading_progress").should(disappear); // Waits until element disappears
  $("#username").shouldHave(text("Hello, Johny!")); // Waits until element gets text
}
```
**Three Simple Things:**
1. Open the page
2. Find an element and Do the Action
3. Find an Element and Assert

```Java
open("/login")
$("#submit").click();
$(".message").shouldHave(text("Hello"));
```


## Example
Selenide Test class
```java

import org.openqa.selenium.By;
import org.testng.annotations.Test;

import static com.codeborne.selenide.Selenide.*;
import static com.codeborne.selenide.Condition.*;

public class Selenide_Practice {

    @Test
    public void selenide_method(){
        // 1. Open the URL
        open("https://www.google.com/");
        // 2. Find element and perform Action
        $(By.id("APjFqb")).setValue("Selenide").pressEnter();
        // 3. Find Element and assert
       $(By.id("logo")).shouldHave(appear);
    }

    @Test
    public void selenide_method1(){
        // 1. Open the URL
        open("https://www.google.com/");
        // 2. Find element and perform Action
        $(By.id("APjFqb")).setValue("Selenide").pressEnter();
        // 3. Find Element and assert
        $(By.id("logo")).shouldHave(appear);
    }
}
```
Selenide POM File
```xml
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>org.Selenide_Learn</groupId>
    <artifactId>SelenideLearn</artifactId>
    <version>1.0-SNAPSHOT</version>

    <dependencies>
        <!-- https://mvnrepository.com/artifact/com.codeborne/selenide -->
        <dependency>
            <groupId>com.codeborne</groupId>
            <artifactId>selenide</artifactId>
            <version>6.17.2</version>
        </dependency>

        <!-- https://mvnrepository.com/artifact/org.testng/testng -->
        <dependency>
            <groupId>org.testng</groupId>
            <artifactId>testng</artifactId>
            <version>7.7.1</version>
            <scope>test</scope>
        </dependency>
        <!-- https://mvnrepository.com/artifact/org.seleniumhq.selenium/selenium-java -->
        <dependency>
            <groupId>org.seleniumhq.selenium</groupId>
            <artifactId>selenium-java</artifactId>
            <version>4.12.0</version>

    </dependencies>

    <properties>
        <maven.compiler.source>11</maven.compiler.source>
        <maven.compiler.target>11</maven.compiler.target>
        <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
    </properties>

</project>
```



# Learning Github Markdown 
#### Example

<details open>
<summary>Maven</summary> <blockquote>
<details Open>
<summary> Selenoid</summary> <blockquote>

**For Selenoid**
``` XML
<!-- https://mvnrepository.com/artifact/org.testng/testng -->
<dependency>
    <groupId>org.testng</groupId>
    <artifactId>testng</artifactId>
    <version>7.8.0</version>
    <scope>test</scope>
</dependency>
```
</blockquote></details>
<details Open>
<summary> TestNG</summary> <blockquote>

**For TestNG**
``` XML
<!-- https://mvnrepository.com/artifact/org.testng/testng -->
<dependency>
    <groupId>org.testng</groupId>
    <artifactId>testng</artifactId>
    <version>7.8.0</version>
    <scope>test</scope>
</dependency>
```
</blockquote></details>

<details>
<summary>Junit</summary><blockquote>
	
**For Junit**
``` XML
<!-- https://mvnrepository.com/artifact/org.testng/testng -->
<!-- https://mvnrepository.com/artifact/junit/junit -->
<dependency>
    <groupId>junit</groupId>
    <artifactId>junit</artifactId>
    <version>4.13.2</version>
    <scope>test</scope>
</dependency>
```
</blockquote></details>
<details>
<summary>Cucumber</summary><blockquote>
	
**For Cucumber**
``` XML
<!-- https://mvnrepository.com/artifact/io.cucumber/cucumber-java -->
		<dependency>
			<groupId>io.cucumber</groupId>
			<artifactId>cucumber-java</artifactId>
			<version>7.4.1</version>
		</dependency>
		<!-- https://mvnrepository.com/artifact/io.cucumber/cucumber-junit -->
		<dependency>
			<groupId>io.cucumber</groupId>
			<artifactId>cucumber-junit</artifactId>
			<version>7.3.3</version>
			<scope>test</scope>
		</dependency>
		<!-- https://mvnrepository.com/artifact/io.cucumber/cucumber-core -->
		<dependency>
			<groupId>io.cucumber</groupId>
			<artifactId>cucumber-core</artifactId>
			<version>7.13.0</version>
		</dependency>

```
</blockquote></details>
</blockquote></details>

