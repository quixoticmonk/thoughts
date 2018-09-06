# Test automation, TDD and all things that worked for us


---

### Team Background

- Fair Client space experience
- A fair mix of development experience(Low->Really Sound)
- 2 folks who have worked on Gherkin or BDD
- 1 who had used test automation tools
---
### Toolset

- Gherkin for acceptance criteria
- Selenium WebDriver for manipulating the DOM
- cucumber-jvm to sew the above two pieces
- Java, Apache Maven as build tool

---
### Why test automation

- Longer Feedback loop
- My version of Truth, Your version of Truth -> One Truth
- Tests in excel which no one except the testers/BA looked at

---
### Why Gherkin

- My version of Truth, Your version of Truth
- Where is my ECI ?
- We love a sequence to things..
'''
  Given I am here
  When I do this
  Then I should see this
'''
---
### Approach we took

- Take one piece of functionality and create an automation script
- Make it work and do what you need to do - report, screenshots and all the boring stuff.
- Take another story, Add another script ( 2 scripts now..Yaay)
- **REFACTOR !!!**
  - Reduce execution time
  - Run on a GRID , don't kill your VDI
  - Run as many tests as possible
  - Identify what cannot be automated
---
### What Helped

- David, Joey, Ryan telling us one Friday that they are taking away our monitors and docking stations.
- Co-located team and pair programming
- Defining our app's html structure
  -- tab, panel, field, fieldValue
  -- Plug and play

---
### Lifecycle of a Jira card/story
- [x] Requirements groomed with Acceptance criteria in Gherkin with TEST DATA which works
- [x] Write the jUnits and run them and see them fail.
- [x] Launch the app server and run the acceptance criteria written in gherkin and see it fail.
- [x] Write code to pass the jUnits and the UI Acceptance criteria
- [x] Re-run all tests.
- [x] Commit the development code to the dev branch and automation code into automation branch for the same story.
- [x] Submit a PR
- [x] Move to Pending Test
- [x] Re-run the automation tests and add any new ECIs or scenarios you noticed
- [x] Run the regression scripts for the page, from the previous two sprints..

---
### What we learnt
- There may be better frameworks for test automation. You need to find or write what works for your team.
- Expanded to 3 teams now.
- Challenges on how others approach a problem statement
