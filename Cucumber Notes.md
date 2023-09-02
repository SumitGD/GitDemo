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

## Setup 
### Create a maven project in Eclipse IDE


## Feature file
```
Feature: Search page
  Scenario: Search a movie
    Given User is on search
    When Search for movie
    And Hit Enter button
    Then Search result should display
    But Error should not display
```


![image](https://github.com/SumitGD/GitDemo/assets/69728301/64e7d422-01f6-4be5-a02e-48bb3b40057c)



