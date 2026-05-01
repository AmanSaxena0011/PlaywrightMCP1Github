# End-to-End Test Automation with Natural Language

## Workflow Overview

This prompt guides you through a complete 7-step Test Automation using MCP
servers and AI agents to go from user story to committed automated test
scripts.

<!-- ## STEP 1: Read User Story

Prompt:

I need to start a new testing workflow. Please fetch and read the user story from
the jira: // It would be my Project Specefic Jira URL in future

Summarize the key requirements, acceptance criteria, and testing scope.

Expected Output: - Summary of the user story - List of acceptance
criteria - Application URL and test credentials -->

## STEP 2: Create Test Plan

Please consider above '## STEP 2: Create Test Plan' as your starting point as Step 1 and proceed further based upon further instructions.

Prompt:

<!-- Based on the user story TD-1 that we just reviewed, use the
playwright-test-planner agent to: -->

I need to start a new testing workflow. Explore the app and create test plan for https://automationexercise.com/

If required login, login with below credentials:

Email Address: aman.saxena0011@gmail.com
Password: 123456789

1.  Read the application URL and test credentials from the user story
2.  Explore the application and understand all workflows mentioned in
    the acceptance criteria
3.  Create a comprehensive test plan that covers all acceptance criteria
    including:
    -   Happy path scenarios
    -   Negative scenarios (validation errors, empty fields, invalid
        data)
    -   Edge cases and boundary conditions
    -   Navigation flow tests
    -   UI element validation
4.  Save the test plan as: specs/ExerciseTestPlan.md

Ensure each test scenario includes: - Clear test case title - Detailed
step-by-step instructions - Expected results for each step - Test data
requirements

Expected Output: - Complete test plan markdown file saved to specs/ -
Organized test scenarios with clear structure - Browser exploration
screenshots (if needed)

## STEP 3: Perform Exploratory Testing

Prompt:

Now I need to perform manual exploratory testing using Playwright MCP
browser tools.

Please read the test plan from: specs/ExerciseTestPlan.md

Then execute the test scenarios defined in that plan: 1. Use Playwright
browser tools to manually execute each test scenario from the plan 2.
Follow the step-by-step instructions in each test case 3. Verify
expected results match actual results 4. Take screenshots at key steps
and error states 5. Document your findings: - Test execution results for
each scenario - Any UI inconsistencies or unexpected behaviors - Missing
validations or bugs discovered - Screenshots as evidence

Expected Output: - Manual test execution results - Screenshots of the
application at various states - List of observations and findings - Any
issues discovered during exploration

## STEP 4: Generate Automation Scripts

Prompt:

Now I need to create automated test scripts using the
playwright-test-generator agent.

Please review: 1. Test plan from: specs/ExerciseTestPlan.md
(for test scenarios and steps) 2. Exploratory testing results from Step
3 (for actual element selectors and UI insights)

Using insights from the manual exploratory testing: - Leverage the
element selectors and locators that were successfully used in Step 3 -
Use stable element properties (IDs, data attributes, roles) discovered
during exploration - Apply wait strategies and UI behaviors observed
during manual testing - Incorporate any workarounds for UI quirks
discovered

Generate Playwright JavaScript automation scripts: 1. Create scripts for
each test scenario from the test plan 2. Organize scripts into
appropriate test suite files in: tests/AutomationExercise/ 3. Use the
test case names and steps from the test plan 4. Use reliable selectors
and strategies from exploratory testing

Requirements for all scripts: - Follow Playwright best practices -
Include proper assertions using expect() - Use descriptive test names
matching the format in the test plan - Use robust element selectors
discovered during manual testing - Add comments for complex steps - Use
proper wait strategies based on actual application behavior - Add proper
test hooks (beforeEach, afterEach) - Configure for multiple browsers
(Chrome, Firefox, Safari)

After generating the scripts, run the tests to verify they pass.

Expected Output: - Test suite files created in tests/AutomationExercise/
based on test plan scenarios - Scripts using robust selectors discovered
during exploratory testing - All scripts follow Playwright best
practices - Initial test generation complete

## STEP 5: Execute and Heal Automation Tests

Prompt:

Now I need to execute the generated automation scripts and heal any
failures using the playwright-test-healer agent.

1.  Run all automation scripts in: tests/AutomationExercise/
2.  Identify any failing tests
3.  For each failing test, use the playwright-test-healer agent to:
    -   Analyze the failure (selector issues, timing issues, assertion
        failures)
    -   Auto-heal the test by fixing selectors, adding waits, or
        adjusting assertions
    -   Update the test script with the fixes
4.  Re-run the healed tests to verify they pass
5.  Repeat the heal process until all tests are stable and passing
6.  Document:
    -   Initial test results (pass/fail count)
    -   Healing activities performed
    -   Final test results after healing
    -   Any tests that couldn't be auto-healed

Expected Output: - All automation tests executed - Failing tests
identified and healed using test-healer agent - Healed test scripts
updated in tests/AutomationExercise/ - Final stable test execution
results - Summary of healing activities performed

## STEP 6: Create Test Report

Prompt:

Now I need to create a comprehensive test execution report based on
manual testing, automation execution, and healing activities.

Please compile results from: - Step 3: Manual exploratory testing
results - Step 4: Generated automation scripts - Step 5: Automated test
execution and healing results

Structure the report as: test-results/TD-101-test-report.md

Include: 1. Executive Summary 2. Manual Test Results 3. Automated Test
Results 4. Defects Log 5. Test Coverage Analysis 6. Summary and
Recommendations

Expected Output: - Comprehensive test execution report covering both
manual and automated testing - Clear PASS/FAIL status for all test
scenarios - Detailed bug reports for failures - Complete test coverage
analysis - Evidence and screenshots attached

## STEP 7: Commit to Git Repository

Git Repository URL:
"github-repo-url"

Prompt:

Now I need to commit all the test artifacts to the Git repository using
the GitHub MCP server.

Please perform the following Git operations: 1. Initialize Git
repository if not already initialized 2. Stage all files in the
workspace 3. Create commit 4. Push all changes 5. Provide summary


## Complete Workflow Execution

I want to demonstrate a complete end-to-end Test Automation using natural language and MCP servers.
