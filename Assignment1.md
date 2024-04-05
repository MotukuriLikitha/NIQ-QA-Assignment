# TODO Application Test Plan

## Contents
1. [Overview](#1-overview)
2. [Purpose](#2-purpose)
3. [Test Environment](#3-test-environment)
4. [Test Scope](#4-test-scope)
    - 4.1 [In-Scope](#41-in-scope)
    - 4.2 [Out-Of-Scope](#42-out-of-scope)
5. [Test Scenarios](#5-test-scenarios)
    - 5.1 [Functionality Testing](#51-functionality-testing)
    - 5.2 [Test Use Cases](#52-test-use-cases)
6. [Test Strategy](#6-test-strategy)
    - 6.1 [Test Objectives](#61-test-objectives)
    - 6.2 [Test Assumptions](#62-test-assumptions)
    - 6.3 [Types of Testing](#63-types-of-testing)
    - 6.4 [Test Entry and Exit Criteria](#64-test-entry-and-exit-criteria)
    - 6.5 [Automation](#65-automation)
7. [Bug Report](#bug-report)
8. [Enhancements](#enhancements)

## 1. Overview
The TODO application provides users with core functionalities such as task creation, editing, status management, and deletion.

## 2. Purpose
The purpose of this test plan is to outline the approach, scope, and test strategy for testing the TODO web application main functionalities in critical happy scenarios.

## 3. Test Environment
- **Browser:** Chromium family
- **Operating System:** Ubuntu

## 4. Test Scope
### 4.1 In-Scope
This test plan covers the testing of only happy paths for the below functionalities of TODO application. 
- Task creation
- Task Edit
- Task Status
- Task Deletion
- Task Status views

### 4.2 Out-Of-Scope
This test plan doesn’t cover the testing of negative scenarios for the below functionalities of TODO application. 
- Task creation
- Task Edit
- Task Status
- Task Deletion
- Task Status views

## 5. Test Scenarios
### 5.1 Functionality Testing
1. **Task Creation**
   - User should be able to add a new task.
   - Newly created task should be visible under the All and Active status tabs.
   - Count of the items left should be increased.
2. **Task Edit**
   - User should be able to edit an existing task by double clicking on it.
   - Changes made to the task should be saved and reflected in the task list.
3. **Task Status**
   - User should be able to mark an active task as complete.
   - Completed tasks should be displayed only under completed status tab.
   - User should be able to change the status of a completed task as active.
   - Task status changed from complete to active should be displayed only under all and active status tabs.
4. **Task Deletion**
   - User should be able to delete any tasks by clicking on “X” mark.
   - User should be able to delete all the completed tasks at once by clicking on “Clear Completed” button.
   - Deleted tasks should not be displayed under All/Active/Completed status tabs.
   - Count of the items left count should be decreased.
5. **Task Status Views**
   - User should be able to view all (active and completed) tasks under all status tab.
   - User should be able to view only active tasks under active status tab.
   - User should be able to view only completed tasks under completed status tab.

### 5.2 Test Use Cases
**Feature: Task Deletion**
**Scenario: Deleting an existing task**
- Given the user is logged in to the TODO application
- And there is a task "Walk the dog" in the task list
- When the user clicks on the cross mark for "Walk the dog" task
- Then "Walk the dog" task should be deleted from the task list
- And the count of the items left displayed at the bottom of each status tab should be decreased by one

**Feature: Task Edit**
**Scenario: Editing an existing task**
- Given there is a task "Pay electric bill" in the task list
- When the user edits “Pay electric bill" with new description as “Pay latest electricity bill”
- Then “Pay electric bill” task should be updated as “Pay latest electricity bill”
- And the changes should be reflected in the task list

## 6. Test Strategy
### 6.1 Test Objectives
- Verify that tasks can be created, edited and deleted successfully
- Verify that tasks are displayed under respective status tabs
- Verify application performance under load

### 6.2 Test Assumptions
- Test environment is deployed without any issues before start testing
- Test data is available for performing functional testing
- Testers have access to necessary tools and software required for testing

### 6.3 Types of Testing
Below tests are advisable to have for TODO application:
- **Functional Testing:**
  - Component testing
  - Smoke testing
  - Integration testing
  - Regression testing
  - Sanity testing
  - System testing
  - Acceptance testing
- **Non-Functional Testing:**
  - Performance – Load and Stress testing
  - Compatibility testing

### 6.4 Test Entry and Exit Criteria
**Entry criteria to start the execution phase of the test and Exit criteria for completing the test.**
1. **Entry criteria:**
   - Test environment(s) is available
   - Test data is available
   - Integration is completed
   - Test scripts are completed, reviewed and approved by the product owner
2. **Exit criteria:**
   - 100% Test Scripts executed
   - Test execution report with all expected and actual results are captured and documented with the test script for regression and SIT
   - All the failed test cases are re run after fixing and retesting of the bugs
   - No open Critical and High severity defects
   - Any outstanding defects should be low prioritized and moved to future release after approval of product owner
   - Any observations/clarifications are marked as enhancements and moved to future release
3. **Test suspension criteria:**
   - On executing smoke test suite, if defects are found which blocks happy path, QA team can hold the execution until the blocker defects are fixed by the development team.
   - QA signoff - If Regression test suite execution status is 40% failed, then QA team can suspend the execution until the failed test cases are addressed by the Development team.

### 6.5 Automation
Main functionality tests of the TODO application like Task creation, editing, deletion, and status management can be automated to minimize testing efforts required for regression testing.

## 7. Bug Report
| Description | Steps to Reproduce | Severity | Priority |
|-------------|---------------------|----------|----------|
| Select all icon is showing pointer. Should be changed to hand glove as it is clickable | - | Low | High |
| Checkbox is showing pointer. Should be changed to hand glove as it is clickable | - | Low | High |
| Select/Unselect all icon should be changed to checkbox instead of down arrow mark, as down mark is giving a sense of collapsible/expandable functionality | - | Low | High |
| Count of items left under completed tab is not accurate | Step1: Under All tab, mark an active task as completed Step2: Navigate to completed tab Step3: View the items left count at the bottom of the tab Expected Behaviour: “1 item completed” should be displayed Actual Behaviour: “1 item left” is displayed | High | High |

## 8. Enhancements
- Status view buttons background can be color filled to give more clear visibility to the user
- User responsive message for task creation, deletion and update can be added to give confirmation o the user after each action is performed
- Edit icon/on hover tooltip can be added for each task instead of double click for better UX
- On hover tooltips can be added for each status view buttons to give a clear information to the user about each status
- Camel casing can be changed for todos title
