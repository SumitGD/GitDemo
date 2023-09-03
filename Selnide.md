# Planning
- [ ] [Learn Selenide tutorial](https://www.youtube.com/watch?v=wN45Qla66-o&list=PLFGoYjJG_fqrvWt1FfHqKoREQmSPxazBq)
      
# What is Selenide & Why to use Selenide?
- It is a Framework for test automation by Selenium web driver : [Officeal Selenide  Documentation](https://selenide.org/)
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
</details>

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


## For Gradel:
**Selenoid**
```Gradel
dependencies {
  testImplementation 'com.codeborne:selenide:6.17.2'
}
```

## First Script
- Create a maven or gradel project in Eclipse or IntelliJ Idea
- **Import required static class**
```Java
import static com.codeborne.selenide.Selenide.*;
import static com.codeborne.selenide.Condition.*;
```
- **Write Class**
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
2. Find the element and Do Action
3. 

