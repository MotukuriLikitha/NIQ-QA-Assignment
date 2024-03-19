# Test Plan for TODO Application

## 1. Test Environment
- Browser: Chromium family
- Operating System: Ubuntu

## 2. Test Scope
### 2.1 In-Scope
This test plan covers the testing of only happy paths for the following functionalities of the TODO application:
- Task creation
- Task Edit
- Task Status
- Task Deletion
- Task Status views

### 2.2 Out-Of-Scope
This test plan doesn’t cover the testing of negative scenarios for the below functionalities of TODO application:
- Task creation
- Task Edit
- Task Status
- Task Deletion
- Task Status views

## 3. Test Approach
### 3.1 Functionality Testing
1. **Task Creation**
   - User should be able to add a new task.
   - Newly created task should be visible under the All and Active status tabs.
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
5. **Task Status Views**
   - User should be able to view all (active and completed) tasks under all status tab.
   - User should be able to view only active tasks under active status tab.
   - User should be able to view only completed tasks under completed status tab.

### 3.2 Test Use Cases
**Feature: Task Deletion**
- Given there is a task "Walk the dog" in the task list
- When the user deletes "Walk the dog" task
- Then "Walk the dog" task should be removed from the task list

**Feature: Task Edit**
- Given there is a task "Pay electric bill" in the task list
- When the user edits “Pay electric bill" with new description as “Pay latest electricity bill”
- Then “Pay electric bill” task should be updated as “Pay latest electricity bill”
- And the changes should be reflected in the task list

## 4. Test Strategy
### 4.1 Types of Testing
Below tests are advisable to have for TODO application:
- Component testing
- Integration testing
- System testing
- Acceptance testing
- Smoke testing
- Sanity testing
- Regression testing

### 4.2 Test Entry and Exit Criteria
**Entry criteria:**
- Test environment(s) is available
- Test data is available
- Code has been merged successfully
- Development has completed unit testing
- Test scripts are completed, reviewed and approved by the Project Team

**Exit criteria:**
- 100% Test Scripts executed
- 90% pass rate of Test Scripts
- No open Critical and High severity defects
- All remaining defects are either cancelled or documented as Change Requests for a future release
- Test execution report with all expected and actual results are captured and documented with the test script

**Test suspension criteria:**
- On executing smoke test suite, if defects are found which blocks happy path, QA team can hold the execution until the blocker defects are fixed by the development team.
- If Regression test suite execution status is 40% failed, then QA team can suspend the execution until the failed test cases are addressed by the Development team.

## Bug Report
| Description                                                                                              | Type    | Severity | Priority |
|----------------------------------------------------------------------------------------------------------|---------|----------|----------|
| Select all icon is showing pointer. Should be changed to hand glove as it is clickable                  | Bug     | Low      | High     |
| Radio button is showing pointer. Should be changed to hand glove as it is clickable                      | Bug     | Low      | High     |
| Select/Unselect all icon should be changed to checkbox instead of down arrow mark                        | Bug     | Low      | High     |
| Checkbox should be used instead of radio button for the tasks as they are multi select                    | Bug     | Low      | High     |
| Status view buttons background can be color filled to give more clear visibility to the user             | Enhancement |          |          |
| User responsive message for task creation, deletion and update can be added                               | Enhancement |          |          |
| Edit icon/on hover tooltip can be added for each task instead of double click for better UX              | Enhancement |          |          |
| On hover tooltips can be added for each status view buttons to give a clear information to the user      | Enhancement |          |          |
```
