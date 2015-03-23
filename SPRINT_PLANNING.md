## Deadlines
- Client needs to provide the user stories the week before the sprint on Thursday morning
- We need to have plan the sprint the by EOD Friday. This includes dealing with not being able to fit everything in the current sprint.

## Outcomes
- We know exactly what needs to get done for the sprint by the time it starts
- We are on the same page with the client about what is (and is not) getting done in the sprint
- We don't take on more work than we can handle
- Everyone on the team knows what they should be working on

## Process
### Ensure all of the high level stories are clarified
**Josh and Venkat are responsible for this**
- Go through each user story in the sprint
- If a task is unclear
  - Add the unclear tag
  - Ask for a description in a comment
  - If you are able to guess what they want, write an acceptance test. Ask them the following:

> Is this what you meant? Is there any functionality I am missing besides this?

- Write all your acceptance tests in the description area of each Asana user story task

### Estimate and assign stories
**Josh and Venkat are responsible for this**
- Estimate the number of points each story is worth
- Assign the stories amongst everyone on the team

> [6] User can search the site for products

- If we can't handle the number of points we give them, we can provide some options on how to reduce the scope for the week.


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

