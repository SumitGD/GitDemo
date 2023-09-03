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
[Follow the Guide to Quick start setup](https://selenide.org/quick-start.html)
** For Maven: **
```Maven
<!-- https://mvnrepository.com/artifact/com.codeborne/selenide -->
<dependency>
    <groupId>com.codeborne</groupId>
    <artifactId>selenide</artifactId>
    <version>6.17.2</version>
</dependency>
```
** For Gradel: **
```Gradel
dependencies {
  testImplementation 'com.codeborne:selenide:6.17.2'
}
```




