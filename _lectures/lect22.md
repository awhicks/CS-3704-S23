---
num: "Lecture 22"
lecture_date: 2022-11-15
desc: "Tue Lecture (LAUNCH Legacy Code projects!)"
ready: false
---

{% include drop_down_style.html %}

# Launching the legacy code projects!

Our goals for today:

* Make sure each team knows which project it is working on
* Make sure each team knows which repo it is working in
* Make sure each team knows which other team it is partnering with
* Make sure each individual is able to get the repo cloned on their own machine and working on localhost (or in a GitHub Codespace)

<details>
<summary>
New Seating Chart
</summary>
![SH1431-F22-Legacy](https://user-images.githubusercontent.com/1119017/201814308-6d2f933c-64e6-4f79-be36-ef1a020f78da.png)
</details>


# Your New Repo

The repo you'll be working in for the remainder of the quarter is shown in the table below.  

Note that your team may be listed in column 1, or column 2, since two teams share a repo.  When we say "partner team", we mean the team that you share a repo with.



<details>
<summary>
Your New Repos
</summary>


| Team      | Team      | Repo                                                   | Docs | Docs-qa |
|-----------|-----------|--------------------------------------------------------|------|---------|
| f22-5pm-1 | f22-5pm-2 | <https://github.com/ucsb-cs156-f22/f22-5pm-courses>    | [docs](https://ucsb-cs156-f22.github.io/f22-5pm-courses-docs) | [docs-qa](https://ucsb-cs156-f22.github.io/f22-5pm-courses-docs-qa) |
| f22-5pm-3 | f22-5pm-4 | <https://github.com/ucsb-cs156-f22/f22-5pm-happycows>  | [docs](https://ucsb-cs156-f22.github.io/f22-5pm-happycows-docs) | [docs-qa](https://ucsb-cs156-f22.github.io/f22-5pm-happycows-docs-qa) |
| f22-6pm-1 | f22-6pm-2 | <https://github.com/ucsb-cs156-f22/f22-6pm-courses>    | [docs](https://ucsb-cs156-f22.github.io/f22-6pm-courses-docs) | [docs-qa](https://ucsb-cs156-f22.github.io/f22-6pm-courses-docs-qa) |
| f22-6pm-3 | f22-6pm-4 | <https://github.com/ucsb-cs156-f22/f22-6pm-happycows>  | [docs](https://ucsb-cs156-f22.github.io/f22-6pm-happycows-docs) | [docs-qa](https://ucsb-cs156-f22.github.io/f22-6pm-happycows-docs-qa) |
| f22-7pm-1 | f22-7pm-2 | <https://github.com/ucsb-cs156-f22/f22-7pm-courses>    | [docs](https://ucsb-cs156-f22.github.io/f22-7pm-courses-docs) | [docs-qa](https://ucsb-cs156-f22.github.io/f22-7pm-courses-docs-qa) |
| f22-7pm-3 | f22-7pm-4 | <https://github.com/ucsb-cs156-f22/f22-7pm-happycows>  | [docs](https://ucsb-cs156-f22.github.io/f22-7pm-happycows-docs) | [docs-qa](https://ucsb-cs156-f22.github.io/f22-7pm-happycows-docs-qa) |
{:.table .table-sm .table-striped .table-bordered}

</details>

# New Workflow for legacy code projects 
 
Note that unlike in the previous phases of the course, you do NOT have `admin` access to these repos: only the staff do.

Therefore:
* You cannot push directly to the `main` branch (it has branch protection rules in place). 
* You can get changes into the `main` branch through PRs
* Only staff can merge PRs into `main` (this is similar to many real world shops where only QA merges code into `main`)
* When code gets merged into `main`, your entire team earns points.
* PRs are typically worth either 5, 10 or 20 points each, depending on the degree of complexity involved.

Note that each repo is starting "green on CI", and we want to keep it that way

That means maintaining 100% test coverage and mutation coverage, subject to exclusions authorized by the staff
- You can exclude code from test coverage or mutation coverage when needed
- For Java code, exceptions for both both Jacoco and Pitest are typically specified in the `pom.xml`
- Exceptions for jest (`npm run coverage`) are done in `package.json`
- Exceptions for stryker can typically be done inline using specially formatted comments
 

# What you must do before code can be merged into main
 
* PR, with good description
  - At a minimum, tell us briefly what the PR does.
  - When there are user facing changes, document those with screenshots or animations (Licecap is a good tool for animations)
  - Tell us how to test, if it is not obvious
  - If it's a frontend change, link to Storybook entries; that's what the `-docs-qa` repo is for!
* Must be green on CI; that means there should be good test coverage
* If there are new React components, there should be storybook entries
* Code review from a team member that didn't write the code
* Code review from a staff member.  Start with your mentor, but any staff member will do
* Deploy it on your team's QA site and actually test it there. Sometimes things work on `localhost` and then do *not* work on Heroku. 
 
 
# Kanban boards
 
<details>
<summary>
Kanban Boards
</summary>

Your team should have `admin` access to it's own Kanban board, and `read only` access to it's "partner" team's Kanban board.
 
Your Kanban board is empty now; we'll explain where you get your issues from shortly.
 
 
| Team      |  Kanban Board            |
|-----------|----------------------------------------------------------------|
| f22-5pm-1-courses | <https://github.com/orgs/ucsb-cs156-f22/projects/48>  |
| f22-5pm-2-courses | <https://github.com/orgs/ucsb-cs156-f22/projects/49>  |
| f22-5pm-3-happycows | <https://github.com/orgs/ucsb-cs156-f22/projects/54>  |
| f22-5pm-4-happycows | <https://github.com/orgs/ucsb-cs156-f22/projects/55>  |
| f22-6pm-1-courses | <https://github.com/orgs/ucsb-cs156-f22/projects/50>  |
| f22-6pm-2-courses | <https://github.com/orgs/ucsb-cs156-f22/projects/51>  |
| f22-6pm-3-happycows | <https://github.com/orgs/ucsb-cs156-f22/projects/56>  |
| f22-6pm-4-happycows | <https://github.com/orgs/ucsb-cs156-f22/projects/57>  |
| f22-7pm-1-courses | <https://github.com/orgs/ucsb-cs156-f22/projects/52>  |
| f22-7pm-2-courses | <https://github.com/orgs/ucsb-cs156-f22/projects/53>  |
| f22-7pm-3-happycows | <https://github.com/orgs/ucsb-cs156-f22/projects/58>  |
| f22-7pm-4-happycows | <https://github.com/orgs/ucsb-cs156-f22/projects/59>  |
{:.table .table-sm .table-striped .table-bordered}

 </details>

 
<details>
<summary>
Team QA Deployment on Heroku
</summary>

Each team has a QA deployment on Heroku.  Since you do not have admin access to the repos, we have set up these QA deployments for you.

Here are links to the QA deployments:

| Team | QA Deployment | 
|------|---------------|
| f22-5pm-1 | <https://f22-5pm-1-courses.herokuapp.com> |
| f22-5pm-2 | <https://f22-5pm-2-courses.herokuapp.com> |
| f22-5pm-3 | <https://f22-5pm-3-happycows.herokuapp.com> |
| f22-5pm-4 | <https://f22-5pm-4-happycows.herokuapp.com> |
| f22-6pm-1 | <https://f22-6pm-1-courses.herokuapp.com> |
| f22-6pm-2 | <https://f22-6pm-2-courses.herokuapp.com> |
| f22-6pm-3 | <https://f22-6pm-3-happycows.herokuapp.com> |
| f22-6pm-4 | <https://f22-6pm-4-happycows.herokuapp.com> |
| f22-7pm-1 | <https://f22-7pm-1-courses.herokuapp.com> |
| f22-7pm-2 | <https://f22-7pm-2-courses.herokuapp.com> |
| f22-7pm-3 | <https://f22-7pm-3-happycows.herokuapp.com> |
| f22-7pm-4 | <https://f22-7pm-4-happycows.herokuapp.com> |
{:.table .table-sm .table-striped .table-bordered}

</details>


# "Chores" to try to get done *today* in class:

## All Teams

* Introduce yourself to the folks on your "partner" team.
* Add all team members and staff members to the team's QA deployment on Heroku
  * Some teams already did this before class.
* Set up Google OAuth for the team's QA deployment on Heroku, and define `GOOGLE_CLIENT_ID` and `GOOGLE_CLIENT_SECRET`
* Add an "In Review" column to the team's Kanban board

## Courses Teams Only

* Get a value for UCSB_API_KEY from the instructor and add that as a config var on your team's qa deployment on Heroku.

# Personal Setup Tasks
 
The big picture task: make sure that you are able to clone the repo for your team to your own machine (or a GitHub Codespace) and get it working
on localhost, so that you have a development environment where you can work on the project.
 
If you can't do that, you can't even get started, so we really need to make sure that works before anything else.

* Clone the repo to your machine, or in a Google Codespace
* Set up a personal `.env` file (i.e. copy `.env.SAMPLE` to `.env` and put in values for `GOOGLE_CLIENT_ID`, `GOOGLE_CLIENT_SECRET`, `ADMIN_EMAILS`, and for courses search only, `UCSB_API_KEY`).
* Get the app to run on your localhost or GitHub Codespace platform

# Where do the issues come from?
 
The staff is putting together a "master" Kanban board of issues for each of the four epics.
 
You can use that as a reference to get issues that you can then add to your own team specific Kanban boards.
 
For now, those are a little sparse; we've needed a lot of time to just get all of the mechanics of setting up all of the repos, deployments, teams, etc. going.   But by section tomorrow, you should have plenty of issues to work on!
