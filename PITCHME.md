@size[1.5em](Test automation, TDD and all the things that worked for us)
---
@quote[Now I'm a pretty lazy person and am prepared to work quite hard in order to avoid work.]  (Martin Fowler)
---
### The Numbers
- 9 of 16 available SPAs.(>500 stories in 3 releases worth 1080 points )
- 5-6 daily deployments with average deployment time of 30 mins.
- 0 prod defects, <5 UAT defects, <4 defects found outside of sprint
- >200 automation PRs compared to our client team's number of 25.
- Automation script coverage : >90%, ~950 Selenium webdriver UI scripts
- Assessed at client agile maturity level of 1 closing down on 2.
---

### Team Background

- A fair mix of development experience(Low->Really Sound)
- 2 folks who have worked on Gherkin or BDD
- 2 who had used test automation tools
- QA turned Product Owner
- Scrum Master who kept us away from the noise
- Fair client space experience

---
### Why test automation

@ul
- Tests in excel which no one except the testers/Prod owner looked at
- Error prone manual test execution or results documentation
- Slow Feedback loop
- Hand it over to anyone who can click a button.
@ulend
---
### Toolset

- Gherkin for writing the acceptance criteria
- Selenium WebDriver for manipulating the DOM
- Cucumber-jvm to sew the above two pieces with steps written in Java
- Apache Maven as build tool
- Dockerised version of Selenium GRID running on a container as a service model

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
### Why Selenium/Cucumber-jvm

- Selenium vs Protractor
- Code in the language the team knows

---
### Approach we took
@ul
- Take one piece of functionality,write an automation script and make it work.
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
- Consensus on the UI elements structure
- Use the label or text in conjunction with xpath as the locator than classes or id
  - unless you have similar labels ( which we had..)

@ulend
---
### Lifecycle of a Jira card/story
@ul
- Acceptance criteria in Gherkin with TEST DATA which works
- Write the jUnits and run them and see them fail.
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
@ul
- Find the toolset that works for your team. Don't get stuck on the word "Framework"
- API tests are faster
- Automated test execution is a way to augment testing.
- Integrating with Devops tools
- Eliminate Waste
- Don't stop at automated functional test execution :
  - Accessibility tests
  - Performance Tests
@ulend
---

### What's Next?
- Virtualization of services invoked
- Setup parallel test case execution
- Abstraction of Selenium webdriver functions
