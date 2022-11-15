---
num: "Lecture 22"
lecture_date: 2022-11-14
desc: "Thu Lecture (LAUNCH Legacy Code projects!)"
ready: false
---

{% include drop_down_style.html %}


# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET


<details>
<summary>
New Seating Chart
</summary>
![SH1431-F22-Legacy](https://user-images.githubusercontent.com/1119017/201814308-6d2f933c-64e6-4f79-be36-ef1a020f78da.png)
</details>


# Your New Repo

The repo you'll be working in for the remainder of the quarter is shown in the table below.  Note that your team may be listed in column 1, or column 2, since two teams share a repo.  Note that unlike in the previous phases of the course, you do NOT have `admin` access to these repos: only the staff do.

Therefore:
* You cannot push directly to the `main` branch (it has branch protection rules in place). 
* You can get changes into the `main` branch through PRs
* Only staff can merge PRs into `main` (this is similar to many real world shops where only QA merges code into `main`)
* When code gets merged into `main`, your entire team earns points.

<details>
<summary>
Your New Repos
</summary>


| Team      | Team      | Repo                                                   |
|-----------|-----------|--------------------------------------------------------|
| f22-5pm-1 | f22-5pm-2 | <https://github.com/ucsb-cs156-f22/f22-5pm-courses>    |
| f22-5pm-3 | f22-5pm-4 | <https://github.com/ucsb-cs156-f22/f22-5pm-happycows>  |
| f22-6pm-1 | f22-6pm-2 | <https://github.com/ucsb-cs156-f22/f22-6pm-courses>    |
| f22-6pm-3 | f22-6pm-4 | <https://github.com/ucsb-cs156-f22/f22-6pm-happycows>  |
| f22-7pm-1 | f22-7pm-2 | <https://github.com/ucsb-cs156-f22/f22-7pm-courses>    |
| f22-7pm-3 | f22-7pm-4 | <https://github.com/ucsb-cs156-f22/f22-7pm-happycows>  |
{:.table .table-sm .table-striped .table-bordered}

</details>


<details>
<summary>
Kanban Boards
</summary>

Your team should have `admin` access to it's own Kanban board, and `read only` access to it's "partner" team's Kanban board.
 
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


 
# Team QA Deployment on Heroku



# "Chores" to try to get done *today* in class:

## All Teams

* Add all team members and staff members to the team's QA deployment on Heroku
  * Some teams already did this before class.
* Set up Google OAuth for the team's QA deployment on Heroku, and define `GOOGLE_CLIENT_ID` and `GOOGLE_CLIENT_SECRET`
* Add an "In Review" column to the team's Kanban board

## Courses Teams Only

* Get a value for UCSB_API_KEY from the instructor and add that as a config var on your team's qa deployment on Heroku.

# Personal Setup Tasks

* Clone the repo to your machine, or in a Google Codespace
* Set up a personal `.env` file (i.e. copy `.env.SAMPLE` to `.env` and put in values for `GOOGLE_CLIENT_ID`, `GOOGLE_CLIENT_SECRET`, `ADMIN_EMAILS`, and for courses search only, `UCSB_API_KEY`).
* Get the app to run on your localhost or Google Codespace platform

