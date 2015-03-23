# Coderly Process

[Creating a new task](#creating-a-new-task)

[You get assigned a new Asana task](#you-get-assigned-a-new-asana-task)

[A task you were assigned isn't clear enough](#a-task-you-were-assigned-isnt-clear-enough)

[You begin work on a new Asana task](#you-begin-work-on-a-new-asana-task)

[You have some questions for a task](#you-have-some-questions-for-a-task)

[You answered someones questions for a task](#you-answered-someones-questions-for-a-task)

[You need your code to be reviewed](#you-need-your-code-to-be-reviewed)

[You have code related questions about your task](#you-have-code-related-questions-about-your-task)
[You have questions about the functionality of a task](#you-have-questions-about-the-functionality-of-a-task)

[Code review process](#code-review-process)

[Tags](#tags)

[Daily Standup](#daily-standup)

## Creating a new task 
- Create the task in Asana
- Write a description that is clear. Someone else should be able to get started on the task without needing to ask you any further questions.

## You get assigned a new Asana task
- Make sure the task is clear enough. Run through the description and see if there are missing details.
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
- Write how the feature would have to be tested by hand in a bullet point list. *Make sure to do this before you write the feature*. Also make sure to keep this up to do date if you find that the requirements change. For example:
  - Login as a merchant
  - Go to account => products
  - Click on "import csv" and upload test_products.csv
  - Check that the products got imported properly

## You answered someones questions for a task
- Assign the task back to the person who asked you the question

## You need your code to be reviewed
**This means that the code is at a point where it is good to be merged. You just want a sanity check on what you have written.**
- Assign an `awaiting review` label to your PR
- Assign an `awaiting review` tag to your task and move it to the top of the section. All “awaiting review” tasks should be at the top of the section.

## You have code related questions about your task
- Create a checklist of unanswered question in your PR *at the top of the description*
- If the question requires a long architectural discussion, then create a separate issue and link to the issue in your checklist
- Assign the `question` label to your PR
- Assign the `question` label in Asana
- If you are blocked assign the `blocked` label. Consider what caused you to get blocked in the first place.

## You have questions about the functionality of a task
**Unrelated to the code itself**
- Assign the task to whoever is best suited to answer the question
- Write question as a comment in the Asana task and reference the person who can answer it (like @JoshSmith)

## Code review process
### High priority maintainance
**Expected turnaround time: 2 hrs**
- Go through all `question` PRs that are marked as `blocked`
- Go through all `awaiting review` PRs that are marked as `blocked`
- Merge all of your `reviewed and looks good` PRs and assign a `merged` label to the Asana task
- Process all of the `answered` labels
  - Check off the answered questions
  - If any questions have not been answered move from `answered` to `question` again
  - If all of the questions have been answered, remove the `answered` label
- Process all of the `reviewed and needs work` labels
  - If the changes take under 15 minutes, make them right away
  - If the changes take longer, use your judgement

### Regular review process
**Should be done 2-3 times per day**
- Go through all `question` PRs during every break
- Go through all remaining `awaiting review` PRs during every break

### Reviewing an awaiting review PR
- Read through the code and answer any questions
- Write comments on individual lines when giving feedback
- If the code looks good
  - Add `reviewed and looks good` label to the PR
  - Add `reviewed and looks good` tag to the Asana task
- If the code needs changes made before merging
  - Add `reviewed but needs work` label to the PR
  - Add `reviewed but needs work` tag to the Asana task
  
### Answering questions for a PR
- Reference the person in a GH comment
- Answer any related issues
- Mark the PR as `answered` and the Asana task as `answered`
- If the answer was sufficient
  - The submitter of the PR should remove the `answered` label
- If the answer wasn't enough
  - The submitter should remove the `answered` label and add the `question` label back

## You have a PR that will not be merged for some reason
- Type in a comment explaining the reason why
- Hit 'Close and comment' when submitting the comment


## Tags
Tags in Asana should always be in the following order:

- **Reviewed and Looks Good**

  The PR has been reviewed and everything looks good.

- **Reviewed but Needs Work**

  This PR needs has some required changes before merging.

- **Awaiting Review**

  The PR needs someone to take a look at it for feedback.

- **Question**

  The PR has questions that needs to be answered.
  
- **Answered**

  The PR had questions which are now answered. This needs to be approved by the one who asked the question.

- **Blocked**

  This PR is currently blocked. The person working on this needs something before he can continue.
  
- **Merged**

  The PR got merged into the development branch.
