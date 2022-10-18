---
num: "Lecture 10"
lecture_date: 2022-10-13
desc: "(Tue Lecture): First Standup meeting on team01, continue work on team01"
ready: true
---

Today, we will:

* Go over some details about how to approach team01
  - Managing branches
  - Managing Pull Requests
  - Why you should *freeze* a branch once you do a PR from it
* Discuss what a "standup meeting is" 
* Hold our first "standup meeting"

We'll then continue work on team01.

* <https://ucsb-cs156.github.io/f22/lab/team01/>

# Some Details about team01

A student asked this question in their team channel on Slack:

* How are we approaching the team project?

This was my answer:

Great question.

For now: each of you has a "category": One of:

* PublicHolidays
* University
* Reddit
* Zip Code
* Location
* Tides

Each of you should work first on the service / service tests for your part, in their own branch.
e.g. 

`git checkout -b chris-location`  or `git checkout -b ab-tides`


The branch naming convention is up to you all to work out: I only suggest that you have one.

Could be `firstname-topic` or `initials-topic` or whatever you decide.

Once you have finished the *service*, you should do a *pull request* from that branch.

And this is important: THEN LEAVE THAT BRANCH ALONE.   Don't continue working in that branch if there's an open pull request for it.

Instead, as you work on the Controller and Controller tests next, make a new branch off of that branch.

For example:

```
git checkout chris-location
git pull origin chris-location
git checkout -b chris-location-controller
```

That checks out the `chris-location` branch

# What happens if you continue making changes to your branch after you do a PR?

Remember that: 
* A branch is a pointer to a commit
* A PR is a request to pull from one branch into another
* Every time you make a commit to a branch, you update where that branch points
* Meaning: if you continue to make commits to a branch that is the basis of an open PR, that *PR will continue to change*
* That's not good!  You want a PR to be a fixed target.
  - You change the branch that a PR is pointing to if and only if the code review process suggests you need changes
  - Then, branches that branched off of that will need to be *rebased*
  - Rebasing means: clipping off all of the later commits that came after the *old* base, and reapplying them *on top of* the new base.

# What is a standup meeting?

# Holding our first standup meeting

# Work time on team01

