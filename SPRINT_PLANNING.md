## Deadlines
**By the time Monday morning arrives, we should have the following**
- We have clear user stories that describe the feature
- The client understands the user stories
- The developer understands the user stories
- We have an estimate of the entire sprint
- We have designs for everything needed on the sprint

**Because of this, clarifying the upcoming sprint is one of the highest priorities. Don't want to respond to questions and get things clarified. DO IT RIGHT AWAY.**

## Outcomes
- We know exactly what needs to get done for the sprint by the time it starts
- We are on the same page with the client about what is (and is not) getting done in the sprint
- We don't take on more work than we can handle
- Everyone on the team knows what they should be working on

## Process
### Ensure all of the high level stories are clarified
**Story clarification role**
- Go through each user story in the sprint
- If a task is unclear
  - Add the unclear tag
  - If you have question about the story, ask with one bullet point for each question.
  - Guess the simplest possible version of what they want are asking for and provide that as an option. **Make sure this is in the form of an acceptance test to avoid any confusion.**

> Ask them is this what you meant? Is there any functionality I am missing besides this?

- Write all your acceptance tests in the description area of each Asana user story task

### Estimate and assign stories
**Estimation and assign role**
- Estimate the number of points each story is worth. One point is 1 hour. Points must be of the Fibonacci sequence: 1, 2, 3, 5, 8, 13, 21.
- Assign the stories amongst everyone on the team like this:

> [6] User can search the site for products


### Break down the stories into tasks
**Done for each of the stories you are assigned**
- Create individual tasks in the dev section of Asana
- Reference the individual tasks in the description area of the user story task
- **Each task should have the granularity of 1 day max. If it doesn't break it down further.**

### What is an acceptance test?

**An acceptance test is a step-by-step example of a feature in action. If our client carried out the instructions of the test, he would agree that the feature works as expected**

Example for a search feature:
- Consumer clicks on the search bar
- Consumer types in "pants"
- Consumer sees a gallery of products with pants in the title or description

_If our client did what we describe above, he would agree that the feature was working_

Some features will require multiple acceptance tests. For example, a search feature might have a way to search within a category.

