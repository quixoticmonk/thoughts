@size[1.5em](Test automation, TDD and all the things that worked for us)

@snap[south-west]
Now I'm a pretty lazy person and am prepared to work quite hard in order to avoid work.
Martin Fowler
@snapend
---

### Team Background

- A fair mix of development experience(Low->Really Sound)
- 2 folks who have worked on Gherkin or BDD
- 1 who had used test automation tools
- QA turned Product Owner
- Scrum Master who kept us away from the noise
- Fair client space experience

---
### Why test automation
@ul
- Longer Feedback loop
- Tests in excel which no one except the testers/Prod owner looked at
- Error prone manual test execution or results documentation
@ulend
---
### Toolset

- Gherkin for writing the acceptance criteria
- Selenium WebDriver for manipulating the DOM
- Cucumber-jvm to sew the above two pieces with steps written in Java
- Apache Maven as build tool
- Dockerised version of Selenium GRID

---
### Why Gherkin
- My version of Truth, Your version of Truth
- Where is my ECI ?
- We love a sequence to things..
```
Given I am here
When I do this
Then I should see this
```
---
### Approach we took
@ul
- Take one piece of functionality and create an automation script
- Make it work
- Take another story, Add another script ( 2 scripts now..Yaay)
- **REFACTOR !!!**
  - Reduce execution time
  - Run on a GRID , don't kill your VDI
  - Run as many tests as possible with as many types of data
  - Identify what cannot be automated
@ulend
---
### What Helped
@ul
- David, Joey, Ryan telling us one Friday that they are taking away our monitors and docking stations.
- Co-located team and pair programming
- Defining our app's html structure and adhering to it
- Use the label or text in conjuction with xpath as the locator than classes or id
  - unless you have similar labels ( which we had..)
- Quicker Feedback loop
@ulend
---
### Lifecycle of a Jira card/story
@ul
- Acceptance criteria in Gherkin with TEST DATA which works
- Write the jUnits and run them and see them fail.
- Launch the app server and run the acceptance criteria written in gherkin and see it fail.
- Write code to pass the jUnits and the UI Acceptance criteria
- Re-run all tests and see them pass.
- Refactor!!
@ulend
---
### Lifecycle of a Jira card/story..continued
@ul
- Commit the development code to the dev branch and automation code into automation branch for the same story.
- Submit the PR
- Move to Pending Test
- Re-run the automation tests and add any new ECIs or scenarios you noticed
- Run the regression scripts for the page, from the previous two sprints..
@ulend
---

### What we learnt
- Find the toolset that work for your team
- Automated test execution is a way to augment testing.
- Exploratory Testing  
- Avoid Waste
