# Coderly Handbook

## New incoming task 
- Create the task in Asana
- Write a description that is clear. Someone else should be able to get started on the task without needing to ask you any further questions.

## You get assigned a new Asana task
- Make sure the task is clear enough
- Assign a due date for yourself and commit to it

## A task you were assigned isn’t clear enough
- Assign the task to whoever is best suited to clarify the task
- Write question as a comment in the Asana task and reference the person who can answer it (like @JoshSmith)

## You begin work on a new Asana task
- Create a new feature branch like `code start update product photos`
- Make the smallest change possible to get started with the feature and commit
- Create a pull request `code pr`
- Add a link to the Asana task on the first line of the PR description
- Add a link to the Github PR on the first line of the Asana description

## You have some questions for a task
- Assign the task to whoever is best suited to answer the question
- Write question as a comment in the Asana task and reference the person who can answer it (like @JoshSmith)

## You answered someones questions for a task
- Assign the task back to the person who asked you the question
- You need your code to be reviewed
- Assign an `awaiting review` label to your PR
- Assign an `awaiting review` tag to your task and move it to the top of the section. All “awaiting review” tasks should be at the top of the section.

## Daily code review process
- Review all PRs that have the `awaiting review` label
- How to review a PR
- Remove the awaiting review label from Asana and GitHub
- If the code looks good
  - Add `reviewed` label to the PR
  - Add `reviewed` tag to the Asana task
- If the code needs work and you want to take a look after they make the changes, assign the `needs work` label
- If the code just needs a few changes made and you are fine with them merging without a second review
  - Add `reviewed` and `good after changes` labels to the PR
  - Add `reviewed` tag to the Asana task
  - Add the `reviewed` Asana just


## Tags
Tags in Asana should always be in the following order

### Reviewed
The PR has been reviewed and everything looks good
### Awaiting Review
The PR needs someone to take a look at it for feedback
### Needs Work
This PR needs has some required changes before merging
### Doing Now
This PR is currently being worked on
### Blocked
This PR is currently blocked. The person working on this needs something before he can continue.
