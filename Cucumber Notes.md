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

## Setup in Ecplise
#### Create a maven project in Eclipse IDE
#### Create a Feature file and run
1. Create a file in the project as a sample. feature
#### Install cucumber eclipse plugin

## Feature file
```Gherkin
Feature: Search page
  Scenario: Search a movie
    Given User is on search
    When Search for movie
    And Hit Enter button
    Then Search result should display
    But Error should not display
```










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



