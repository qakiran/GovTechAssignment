# GovTechAssignment
### Project Name: THE OPPENHEIMER PROJECT
##### Team Name: Citizen Disbursement System (CDS) Team


<h4>This is a software system that has to support 3 features:</h4>

 - [x] Enable Clerks to populate a list of working class heroes to the system
 - [x] Enable Bookkeepers to retrieve the payable taxation relief for each working class
 - [x] Enable Governor to dispense the money to each working class hero at her discretion

**How to Run**
```cmd
 git clone "https://github.com/afsarali273/GovTechAssignment.git"

 cd /path/to/project/GovTechAssignment

 mvn clean test
```

Below Test Scenarios being covered in this Project

   > ClerksActions.feature
  ```gherkin
    Feature: Addition of working class hero by Clerk
    
      As a Clerk ,I shall be able to add working hero's to the Database by using API and UI
    
      Scenario: TC-001 Addition of Single Working class hero
    
      Scenario: TC-002 Addition of Multiple Working class hero
              
      Scenario: TC-003 Addition of Multiple Working class hero using csv file
       
          @UI
      Scenario: TC-004 Addition of working class hero using csv file from UI
           
```
  
  > BookkeepersActions.feature
  
  ```gherkin
  Feature: Access Data from Database by Bookkeeper
  
    As a Bookkeeper,I want to retrieve data from Database and validate to report it to my Bookkeeping Manager
  
    Scenario: TC-001 Get list of working hero's from Database
    
    Scenario: TC-002 validate natid masked with $ from 5th character
    
    Scenario: TC-003 calculate tax relief using formula
    
    Scenario: TC-004 validate when tax relief amount is less than 50.00

```  

> GovernorActions.feature

```gherkin

Feature: Verify Governor actions on UI

  Scenario: Verify Governor actions on UI
    Given I navigate to baseurl in chrome browser
    And Verify UI button with its color and text
    When I click on the Dispense button
    Then I Shall navigate to a page which says "Cash dispensed"


```


    
**Test Results**
![Test Results](https://github.com/afsarali273/GovTechAssignment/blob/master/Govtech_RunFromIDE.png)

![Test Results](https://github.com/afsarali273/GovTechAssignment/blob/master/Govtech_report.png)


**Bug**
```html
Seems csv upload functionality is not working .
Expected: "/calculator/uploadLargeFileForInsertionToDatabase" should upload csv file to Database
Actual: Getting 500 response while uploading with CSV file 

Same issue with UI as well.
```
