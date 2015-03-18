##At the start of a project
- Create a recurring task in Asana for Deploying to production

##Schedule for deploy
Every day at 6 AM PST. Everyone who is able to be awake during this time is expected to be available.

##Deploy Checklist

**To be created the working day before the deploy**
- Title of the PR linking to the PR like this: [Attempt to upgrade ember-cli to 0.2.0](https://github.com/coderly/reissued-ember/pull/309)
- Links to the migrations like this: [20150304140930_add_slug_to_users](https://github.com/coderly/reissued-api/blob/development/db/migrate/20150304140930_add_slug_to_users.rb)
- Are there any incompatible changes in this PR?
- Testing checklist for PR (to be taken from the PR description)

##Day before deploy
- Everyone: create the deploy checklist for your PRs in a gist make sure the checklist is like
```
- [ ] item 1
- [ ] item 2
```
- Everyone: paste your checklist into the Deploy to Production recurring task
