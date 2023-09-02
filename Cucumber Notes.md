# Planning 
Complete below tutorial to learn cucmber 
- [ ] [cucumber BDD tutroial](https://www.youtube.com/watch?v=InX5h3zBsqM)

# Cucumber Basics
## Why to learn cucumber
+ It is a BDD-based test management tool that uses the Gherkin language to write test cases under feature files.
+ It Easy to use and implement
Cucumber Doc: 
[Cucumber Official Documentation ](https://cucumber.io/docs/cucumber/).

## Gherkin Keywords
+ Feature
+ Scenario
+ Scenario Outline
+ Given
+ When
+ Then
+ And
+ But
+ Examples

# Setup
<details>
<summary><h3>Setup in Ecplise</h3></summary>

+ Install the cucumber Eclipse plugin
+ Create a maven project in Eclipse IDE
+ Add Maven libraries in the Pom.xml
  1. [Cucumber-java ](https://mvnrepository.com/artifact/io.cucumber/cucumber-java)
  2. [Cucumber-JUNIT ](https://mvnrepository.com/artifact/io.cucumber/cucumber-junit)
  3. [Cucumber-core ](https://mvnrepository.com/artifact/io.cucumber/cucumber-core)

</details>
<details>
<summary><H3>Setup in IntelliJ Idea</H3></summary>
  
+ Install the cucumber plugin IntelliJ idea
+ Create a maven project in IntelliJ idea 
+ Add Maven libraries in the Pom.xml
  1. [Cucumber-java ](https://mvnrepository.com/artifact/io.cucumber/cucumber-java)
  2. [Cucumber-JUNIT ](https://mvnrepository.com/artifact/io.cucumber/cucumber-junit)
  3. [Cucumber-core ](https://mvnrepository.com/artifact/io.cucumber/cucumber-core)

</details>

# Example
```Gherkin
#Author: your.email@your.domain.com
#Keywords Summary :
#Feature: List of scenarios.
#Scenario: Business rule through list of steps with arguments.
#Given: Some precondition step
#When: Some key actions
#Then: To observe outcomes or validation
#And,But: To enumerate more Given,When,Then steps
#Scenario Outline: List of steps for data-driven as an Examples and <placeholder>
#Examples: Container for s table
#Background: List of steps run before each of the scenarios
#""" (Doc Strings)
#| (Data Tables)
#@ (Tags/Labels):To group Scenarios
#<> (placeholder)
#""
## (Comments)
#Sample Feature Definition Template
@tag
Feature: Title of your feature
  I want to use this template for my feature file

  @tag1
  Scenario: Title of your scenario
    Given I want to write a step with precondition
    And some other precondition
    When I complete action
    And some other action
    And yet another action
    Then I validate the outcomes
    And check more outcomes

  @tag2
  Scenario Outline: Title of your scenario outline
    Given I want to write a step with <name>
    When I check for the <value> in step
    Then I verify the <status> in step

    Examples: 
      | name  | value | status  |
      | name1 |     5 | success |
      | name2 |     7 | Fail    |

```

# Practical
## Pom.xml required Dependencies
```xml
	<dependencies>
		<!-- https://mvnrepository.com/artifact/junit/junit -->
		<dependency>
			<groupId>junit</groupId>
			<artifactId>junit</artifactId>
			<version>4.13.2</version>
			<scope>test</scope>
		</dependency>

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
## Feature File 
```Gherkin
@feature1
Feature: Search page
@Scenario1
Scenario: Search check
Given User on the search bar
When User is enter search keyword
And Enter search button
Then User should get Results as per search
But no Error should display 
```
## Step defination File 
Write click on the feature file and run.
Copy the undefined scenarios for the scenarios.
Create stepdefination class file in the project.
paste the undefined scenarios in step definaition class.

```java
package featuers;

import io.cucumber.java.en.*;

public class stepDefinations {
	
	@Given("User on the search bar")
	public void user_on_the_search_bar() {
	   System.out.println(">> On the search Bar");
	}

	@When("User is enter search keyword")
	public void user_is_enter_search_keyword() {
		 System.out.println(">> Entered Search Keyword");
	}

	@When("Enter search button")
	public void enter_search_button() {
		 System.out.println(">> Clicked on Search");
	}

	@Then("User should get Results as per search")
	public void user_should_get_results_as_per_search() {
		 System.out.println(">> Search resuts displaying");
	}

	@Then("no Error should display")
	public void no_error_should_display() {
		 System.out.println(">> No Error Displaying");
	}

}
```

Other Way to generate step defination " tidy gherkin " plugin
1. Insall chrome extension and open [Tidy ghekin plugin](https://chrome.google.com/webstore/detail/tidy-gherkin/nobemmencanophcnicjhfhnjiimegjeo?hl=en-GB)
2. Copy Scenarios and paste in tidy editor
3. Select " Java Steps"
4. Copy and paste it in step defination class 

## Runner File
Running multiple feature file together using runner class. required **JUNIT dependency** for **@RunWith** Annotation.
```Java
package featuers;

import org.junit.runner.RunWith;

import io.cucumber.junit.Cucumber;

@RunWith(Cucumber.class)
public class runner {

}
```



## Tabs
## Quarterly Results { .tabset .tabset-fade .tabset-pills}
Content before the tabs.

### [Tab A](#tab/tab-a)
Tab A content.

### [Tab B](#tab/tab-b)
Tab B content.
***

Content after the tabs.


## precendence 
<ul>
<li>`one</li>
<li>two`</li>
</ul>

## Blocks
<hr />
<hr />
<hr />

## Table Block
<table><tr><td>
<pre>
**Hello**,

_world_.
</pre>
</td></tr></table>

<pre language="haskell"><code>
import Text.HTML.TagSoup

main :: IO ()
main = print $ parseTags tags
</code></pre>

## Collapsed block
<details>

<summary>Tips for collapsed sections</summary>

### You can add a header

You can add text within a collapsed section. 

You can add an image or a code block, too.

```ruby
   puts "Hello World"
```
</details>

## Fenced code blocks
```
function test() {
  console.log("notice the blank line before this function?");
}
```
## Syntax higlighting
```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```
## Creating Mermaid diagrams

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```
## Imprtant 

> [!NOTE]
> Highlights information that users should take into account, even when skimming.

> [!IMPORTANT]
> Crucial information necessary for users to succeed.

> [!WARNING]
> Critical content demanding immediate user attention due to potential risks.

# foo
## foo
### foo
#### foo
##### foo
###### foo

# foo *bar* \*baz\*

*** abc
--- abc
___ abc
→foo→baz→→bim

![image](https://github.com/SumitGD/GitDemo/assets/69728301/64e7d422-01f6-4be5-a02e-48bb3b40057c)



