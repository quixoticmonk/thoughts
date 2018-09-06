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
### What Made us to look at automation and Gherkin

- Longer Feedback loop
- My version of Truth, Your version of Truth -> One Truth
- Tests in excel which no one except the testers/BA looked at
- 1 who had used test automation tools

---
### Approach we took

- Take one piece of functionality and create an automation script
- Make it work and do what you need to do
- Take another story, Add another script ( 2 scripts now..Yaay)
- REFACTOR !!!
---
### What Helped

- David, Joey, Ryan telling us one Friday that they are taking away our monitors and docking stations.
- Co-located team and pair programming
- Defining our app's html structure
  -- tab, panel, field, fieldValue

---
### Lifecycle of a Jira card/story
- Requirements groomed with Acceptance criteria in Gherkin with TEST DATA which works
- Write the jUnits and run them and see them fail.
- Launch the app server and run the acceptance criteria written in gherkin and see it fail.
- Write code to pass the jUnits and the UI Acceptance criteria
- Re-run all tests.
- Commit the development code to the dev branch and automation code into automation branch for the same story.
- Submit a PR
