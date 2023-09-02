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
<summary>Setup in Ecplise</summary>
  
+ Create a maven project in Eclipse IDE
+ Create a Feature file and run
+ Create a file in the project as a sample. feature
+ Install the cucumber Eclipse plugin
+ Create Scenarios in the feature file
```Gherkin
Feature: Search page
  Scenario: Search a movie
    Given User is on search
    When Search for movie
    And Hit Enter button
    Then Search result should display
    But Error should not displayYou can add text within a collapsed section. 
```
</details>

<details>

<summary>Setup in IntelliJ idea</summary>

### Feature file
You can add text within a collapsed section. 
You can add an image or a code block, too.

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
</details>

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



