# Cucumber Basics
## Why to learn cucumber
+ It is a BDD-based test management tool that uses the Gherkin language to write test cases under feature files.
+ It Easy to use and implement

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
  
## Cucumber Files 

### Feature file 
```
Feature: Search page
  Scenario: Search a movie
    Given User is on search
    When Search for movie
    And Hit Enter button
    Then Search result should display
    But Error should not display
```


