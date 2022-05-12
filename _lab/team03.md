---
desc: "Team Project: FrontEnd CRUD, part 1: Index Page, and Delete Column"
assigned: 2022-05-12 14:00
due: 2022-05-18 23:59
github_org: ucsb-cs156-s22
layout: lab
num: team03
ready: false
gauchospace_url: update_this_url
starter: git@github.com:ucsb-cs156-s22/STARTER-team03.git
---

{% include drop_down_style.html %}


# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET


## Big Picture: what is team03 all about?

From a high-level standpoint, you'll be doing these things:

Set up Tasks:

* Setting up qa and prod deployments on Heroku 
  - If your team02 is graded, you may reuse your team02 heroku deployment
  - No need to rename it; just deploy the new code base to it
  - This will save you time, since you wont have to update the Google OAuth secrets
* Configuring the `-docs` and `-docs-qa` repos
  - You will need to do this, and it will actually matter, since we'll be using Storybook
* Configuring Codecov
* Setting up your own Kanban board
  - In this project, you'll create a Kanban board from scratch
  - You'll also be responsible for creating your own issues and adding the acceptance criteria

Coding Tasks:
* Adding the index page and table components for each of your six database tables
* Adding tests for these

In team04, we'll add the create and edit functions as well.  For team03, you'll continue to create and edit through the Swagger endpoints directly.

For this assignment, we are still dealing directly with the backend via Swagger.

# Set up Tasks

There are several set up tasks.  I suggest that you divide these up among your team, and indicate on the team slack channel who is doing what.

Here's the full list, followed by more detail about each one (in the dropdown boxes indicated by the triangles;  **_click the triangle_** (▶) to reveal the steps for each one.

Ideally, if you have six team members available to help out, each team member will do one of these.  If you have fewer than six team members available, I suggest combining either (3,4) or (5,6) since they  are quite similar, and can easily be done quickly by the same person.


<details>
<summary>
Setup Task 1: Creating your team's Kanban board
</summary>

1. Tell the rest of the team (via your Slack channel) that you are setting up the Kanban board.

2. Go to your team03 repo.  At this stage, it doesn't matter whether it's still empty, or whether it already has stuff in it.

   | Section | 1 | 2| 3| 4| 
   |-|-|-|-|-|
   | 4pm | [team03-s22-4pm-1](https://github.com/ucsb-cs156-s22/team03-s22-4pm-1) | [team03-s22-4pm-2](https://github.com/ucsb-cs156-s22/team03-s22-4pm-2)    | [team03-s22-4pm-3](https://github.com/ucsb-cs156-s22/team03-s22-4pm-3) | [team03-s22-4pm-4](https://github.com/ucsb-cs156-s22/team03-s22-4pm-4) | 
   | 5pm | [team03-s22-5pm-1](https://github.com/ucsb-cs156-s22/team03-s22-5pm-1) | [team03-s22-5pm-2](https://github.com/ucsb-cs156-s22/team03-s22-5pm-2)    | [team03-s22-5pm-3](https://github.com/ucsb-cs156-s22/team03-s22-5pm-3) | [team03-s22-5pm-4](https://github.com/ucsb-cs156-s22/team03-s22-5pm-4) | 
   | 6pm | [team03-s22-6pm-1](https://github.com/ucsb-cs156-s22/team03-s22-6pm-1) | [team03-s22-6pm-2](https://github.com/ucsb-cs156-s22/team03-s22-6pm-2)    | [team03-s22-6pm-3](https://github.com/ucsb-cs156-s22/team03-s22-6pm-3) | [team03-s22-6pm-4](https://github.com/ucsb-cs156-s22/team03-s22-6pm-4) | 
   {:.table .table-sm .table-striped .table-bordered}

3. Click on the Projects tab. It should look like this:

   <img width="593" alt="image" src="https://user-images.githubusercontent.com/1119017/167972688-04403c2b-65cf-4790-9a22-b7e8bc850061.png">

4. Click on the bottom `Projects` button (not the `Beta` one, but the other one). Your screen should then look like this:

   <img width="1183" alt="image" src="https://user-images.githubusercontent.com/1119017/167972869-361f8df9-3d0b-4ede-bf38-df3fee636135.png">

5. Click the green `New Project` button, at upper right.  Your screen should then look like this:

   <img width="990" alt="image" src="https://user-images.githubusercontent.com/1119017/167972920-a8a0eb57-102e-43d1-baa6-f3cf2e964b2d.png">

6. Fill in the project name with your team name (e.g. `s22-4pm-1`).  You can leave the description blank. Then select `Automated Kanban with Reviews` from the dropdown menu (as shown), and finally click the `Create Project` button.
   <img width="472" alt="image" src="https://user-images.githubusercontent.com/1119017/167973020-b9d862b4-3dc9-4110-8da5-6afb145a15b4.png">

7. In the `To Do` column, you'll now have some annoying starter cards, as shown below.  Click in the three dots at upper right on
   each of them to get rid of them, so that you have an empty board:

   <img width="438" alt="image" src="https://user-images.githubusercontent.com/1119017/167973169-b79f2879-cab8-4f2e-8f8d-ace42d1675cf.png">

   When done, it should look like this:

   <img width="1720" alt="image" src="https://user-images.githubusercontent.com/1119017/167973263-66ee283e-7289-4d6d-8ac0-491cf367343c.png">

8. Congratulations: your team can now start adding issues to your Kanban board.

</details>
  
<details>
<summary>
Setup Task 2: Populating team03 repo with starter code
</summary>
  
One team member should clone the team03 repo, which should be found here:
  
| Section | 1 | 2| 3| 4| 
|-|-|-|-|-|
| 4pm | [team03-s22-4pm-1](https://github.com/ucsb-cs156-s22/team03-s22-4pm-1) | [team03-s22-4pm-2](https://github.com/ucsb-cs156-s22/team03-s22-4pm-2)    | [team03-s22-4pm-3](https://github.com/ucsb-cs156-s22/team03-s22-4pm-3) | [team03-s22-4pm-4](https://github.com/ucsb-cs156-s22/team03-s22-4pm-4) | 
| 5pm | [team03-s22-5pm-1](https://github.com/ucsb-cs156-s22/team03-s22-5pm-1) | [team03-s22-5pm-2](https://github.com/ucsb-cs156-s22/team03-s22-5pm-2)    | [team03-s22-5pm-3](https://github.com/ucsb-cs156-s22/team03-s22-5pm-3) | [team03-s22-5pm-4](https://github.com/ucsb-cs156-s22/team03-s22-5pm-4) | 
| 6pm | [team03-s22-6pm-1](https://github.com/ucsb-cs156-s22/team03-s22-6pm-1) | [team03-s22-6pm-2](https://github.com/ucsb-cs156-s22/team03-s22-6pm-2)    | [team03-s22-6pm-3](https://github.com/ucsb-cs156-s22/team03-s22-6pm-3) | [team03-s22-6pm-4](https://github.com/ucsb-cs156-s22/team03-s22-6pm-4) | 
{:.table .table-sm .table-striped .table-bordered}  

Steps (illustrated below)
  
| Explanation | Command |
|-|-|  
| (1) Add the starter code repo ({{page.starter}}) as a remote | <tt>git remote add starter {{page.starter}}</tt> |
| (2) Checkout branch `main` locally  | <tt>git checkout -b main</tt> |
| (3) Pull from the main branch of the starter | <tt>git pull starter main</tt> |
| (4) Push to the main branch of your repo | <tt>git push origin main</tt> |
{:.table .table-sm .table-striped .table-bordered}  
  

That should establish the main branch of your repo so that everyone on the team can then clone it and use it as a starting point.  
  
</details>  
  
<details>
<summary>
Setup Task 3: Set up -docs and -docs-qa repos (must be done after 2)
</summary>
 
In this task, you'll set up a GitHub Pages site for documentation of your code base; for now, that just consists of the published Storybook, which is
an interactive catalog of all of your React components.

To do this, follow these steps:

1.  Create a new repo under the course organization <tt>{{page.github_org}}</tt> that has the same name as your team03 repo (e.g. `team03-s22-4pm-1`) but 
    with `-docs` appended to the end of the name (for example, `team03-s22-4pm-1-docs`.)
2.  Now do the same step again, creating a repo with `-docs-qa` (for example, `team03-s22-4pm-1-docs`.)
3.  In each of these repos, create a file called `/docs/README.md`.  This is necessary to establish the main branch, and the `/docs` folder.  The contents are not important for now, since they will be overridden later.
4.  In each of these repos, go to the `Settings` page for the repo, then look for `Pages` in the left navigation. You want to enable GitHub pages, so that the settings look like this:

    <img width="640" alt="image" src="https://user-images.githubusercontent.com/1119017/168149276-6ebbf519-48ed-4f2e-8137-f7d68dedbb78.png">


5.  Go to the settings page for your personal GitHub account, like this:
  
    <img width="237" alt="image" src="https://user-images.githubusercontent.com/1119017/168149677-706a468e-85e8-4186-8265-7e4a90fbb511.png">

6.  Find the Developer Settings in the left navigation, near the bottom.
  
    <img width="228" alt="image" src="https://user-images.githubusercontent.com/1119017/168149892-44de1722-3416-4378-b78a-c3928b0ccb6d.png">

7.  On the developer settings, choose `Personal Access Token`
    <img width="274" alt="image" src="https://user-images.githubusercontent.com/1119017/168149966-7d4fdc82-2bb8-4d18-8f20-57fddbc04e08.png">

8.  Click `Generate New Token`.  You'll need to confirm your password.
    <img width="693" alt="image" src="https://user-images.githubusercontent.com/1119017/168150055-f221a3ac-a8f3-4cd6-aacb-f7fbd8f33fc2.png">

9.  Fill in the description with your team03 repo name (like shown below). Note that the description is just for humans, so the formatting doesn't have to be exact.  This is just so you can remember what the token is for.

    Select 90 days for the expiration, and then select `repo` as the only scope (it includes all the detailed scopes underneath).
  
    <img width="668" alt="image" src="https://user-images.githubusercontent.com/1119017/168150417-f7d096ee-b3a7-4403-8d55-ca0337a561f1.png">

    Finally, scroll down and click `Generate Token`.

    <img width="299" alt="image" src="https://user-images.githubusercontent.com/1119017/168150606-427be326-828c-47ef-af04-f399254d06c5.png">

     You'll be shown a token value (this one is fake and has been deactivated).  Copy it, because once you close the window it's gone, but
     DO NOT PASTE IT ANYWHERE except in the secrets portion of your team03 repo (next step).  This value can be used in place of your 
     GitHub password, so you need to protect it.
  
     <img width="667" alt="image" src="https://user-images.githubusercontent.com/1119017/168150856-e3623eae-e041-4a02-814c-417566ff1d3a.png">

  
10. Return to your main team03 repo, and go to Settings page for `Secrets: Actions`  (This is done on the regular `team03-s22-4pm-1` repo, NOT on the `-docs` and `-docs-qa` repos.)

     <img width="270" alt="image" src="https://user-images.githubusercontent.com/1119017/168151099-7508f238-c9f2-4e2a-8721-8cbeb610cc30.png">

     On the Secrets page click `New Repository Secret` then add a secret called `DOCS_TOKEN`.  Be careful here, because the name must be 
     *exactly* `DOCS_TOKEN`, not `DOC_TOKEN` or anything else; this value is referenced in the GitHub workflow scripts.

     <img width="716" alt="image" src="https://user-images.githubusercontent.com/1119017/168151417-37955809-9710-4c28-837d-ba5a7ba0fc12.png">

     After you are done, it should look like this:

     <img width="661" alt="image" src="https://user-images.githubusercontent.com/1119017/168151474-1b17b540-0968-470c-bb8f-ec5c891daa5c.png">

     If you need to replace the secret (e.g. for debugging reason), you can overwrite it, but once you store it, you can't look at it.
     So if you get it wrong, you just have to create a new one; you can't edit the old value.
  
     
      
11. Now, once `DOCS_TOKEN` is updated, and till in your main team03 repo, and go to the page for GitHub Actions (the `Actions` tab).   You should see these workflows in the list on the left:

    <img width="244" alt="image" src="https://user-images.githubusercontent.com/1119017/168151802-c6e22e2f-dd63-49e0-ab06-3d641c75a8e6.png">

    Click on the job that starts with `02-publish-docs-to-GitHub` and you should see this:

    <img width="1090" alt="image" src="https://user-images.githubusercontent.com/1119017/168151888-dcc54aeb-bbf9-4f3d-97e8-5448a065c9ba.png">

    On the right hand side of the screen, find where it says `Run Workflow`, and click it.  That should expose this box:
  
    <img width="335" alt="image" src="https://user-images.githubusercontent.com/1119017/168152002-c51f67c2-57f7-4291-a856-4daa9ac3cb63.png">

    Click `Run Worfklow`
  
12. Repeat this step for the job that starts with `04-publish-docs-to-GitHub`.
  
13. When each of these two jobs is finished, you should be able to navigate to your GitHub Pages sites at URLs like this (subsitute your own team name):

    * <https://ucsb-cs156-s22.github.io/team03-s22-5pm-3-docs>
    * <https://ucsb-cs156-s22.github.io/team03-s22-5pm-3-docs-qa>
  
    And these links should show a Storybook page like the ones shown below (except your team name will show instead of `STARTER-team03`.  The branches
    listed may be different two, but this is the general idea of what the pages should look like.

    <img width="629" alt="image" src="https://user-images.githubusercontent.com/1119017/168152477-28391f6f-489a-4ff7-82e8-27699d6c2b4c.png">

    <img width="694" alt="image" src="https://user-images.githubusercontent.com/1119017/168152556-1247a9e2-a15b-4dfb-8169-1daf056ec755.png">

14. Go into the `README.md` file of your main team03 repo, and edit the links to the documentation.  They will look like this when you start:
  
    ```
    TODO: Add correct links to the -docs and -docs qa GitHub pages sites

    * Storybook (production): <https://ucsb-cs156-s22.github.io/STARTER-team03-docs>
    * Storybook (development/qa): <https://ucsb-cs156-s22.github.io/STARTER-team03-docs-qa>
    ```
  
    After you edit, it should look like this (with links appropriate for your team). Note that you should *remove* the part that says `TODO`.
  
    ```
    * Storybook (production): <https://ucsb-cs156-s22.github.io/team03-s22-6pm-4-docs>
    * Storybook (development/qa): <https://ucsb-cs156-s22.github.io/team03-s22-6pm-4-docs-qa>
    ```
 
That's it for this task.  
</details>  
  
<details>
<summary>
Setup Task 4: Set up Codecov (must be done after 2)
</summary>
  

In this task, you'll make sure that Codecov is set up to track the `main` branch instead of master, and you'll add the correct Codecov badge to
your repo's `README.md` file.
  
Task 2 needs to be done first, so that the main repo has code in it, and the CI/CD jobs for the first push of code have finished running.
  
1. Visit the link <https://app.codecov.io/gh/ucsb-cs156-s22/team03-s22-5pm-3> (where `s22-5pm-3` is replaced with your team name)
2. Navigate to `Settings`. It should look like this. (Note that the token shown has been regenerated; it's no longer valid.)
  
   <img width="1213" alt="image" src="https://user-images.githubusercontent.com/1119017/168153563-986766e3-fe00-4635-bb16-7f741223b93f.png">

3. If the `Default Branch` shows `master`, change it to `main` and click `Update`.
4. Click where it says `Badge` at left, and you should see something like this:
  
   <img width="1218" alt="image" src="https://user-images.githubusercontent.com/1119017/168153791-b4302245-74d1-4755-a9a7-1be4c9e912a7.png">

   Click the button to copy the markdown for the Badge.
 
5. Go to your team03 README.and edit it to find where the Codecov badge needs to be replaced.  It should look like this:
  
   ```
   TODO: Add a codecov badge for the main branch here.  What's shown is an example, but you need to visit codecov to get the markdown for your repo; don't just try to edit the markdown in the example below.  The token value won't match your repo.  Be sure to adjust the default branch from `master` to `main`.

   [![codecov](https://codecov.io/gh/ucsb-cs156-s22/STARTER-team03/branch/main/graph/badge.svg?token=s3OvSANaki)](https://codecov.io/gh/ucsb-cs156-s22/STARTER-team03)
   ```
   
   Replace that by pasting in the correct markdown for the badge, and removing the `TODO` text:
  
6. That's it for this task.   
  
</details>  
  
  
  
<details>
<summary>
Setup Task 5: Push main branch to team02 heroku prod (must be done after 2)
  
To save time, we are going to reuse the Heroku prod instance from team02 for team03.
  
A link to the dashbaord of your team02 Heroku Prod insttance appears below. Check that it's still active.
  

| Section | 1 | 2 | 3 | 4 |
|-|-|-|-|-|
| 4pm | [s22-4pm-1-team02](https://dashboard.heroku.com/apps/s22-4pm-1-team02) | [s22-4pm-2-team02](https://dashboard.heroku.com/apps/s22-4pm-2-team02) |  [s22-4pm-3-team02](https://dashboard.heroku.com/apps/s22-4pm-3-team02) | [s22-4pm-4-team02](https://dashboard.heroku.com/apps/s22-4pm-4-team02) | 
| 5pm | [s22-5pm-1-team02](https://dashboard.heroku.com/apps/s22-5pm-1-team02) | [s22-5pm-2-team02](https://dashboard.heroku.com/apps/s22-5pm-2-team02) |  [s22-5pm-3-team02](https://dashboard.heroku.com/apps/s22-5pm-3-team02) | [s22-5pm-4-team02](https://dashboard.heroku.com/apps/s22-5pm-4-4team02) | 
| 6pm | [s22-6pm-1-team02](https://dashboard.heroku.com/apps/s22-6pm-1-team02) | [s22-6pm-2-team02](https://dashboard.heroku.com/apps/s22-6pm-2-team02) |  [s22-6pm-3-team02](https://dashboard.heroku.com/apps/s22-6pm-3-team02) | [s22-6pm-4-team02](https://dashboard.heroku.com/apps/s22-6pm-4-team02) | 
{:.table .table-sm .table-striped .table-bordered}  
 
Make sure that the application is still up, and that you can use Google OAuth to login.
  
If so, then to save time: *do not change the name of the app*.  If you do, then OAuth will break, since it depends on exactly the name you already have.
  
Since team03 builds on team02, it's fine for us to use the same deployment.
  
<em>Note: At the time of this exercise, 05/12/2022,  the Heroku/GitHub interface in the web dashboard is disabled, due to a security breach at Heroku. If/when it's restored, the following instructions could be simplified.  For now, we have to do this at the command line. </em>
  
Next, you'll want to clone the repo on your local system. 

Change directory (`cd`) into the repo, and then issue this command, substituting in your Heroku app name:
  
```
heroku git:remote -a s22-4pm-2-team02
```
  
Then, do this command to push the main branch to the Heroku deployment:
  
```
git push heroku main
```
  
This should deploy the starter code to the Heroku app.  
  
If it works, you have just one more step: Edit the `README.md` of your main repo to fix the link to the production deployment.

It will start out looking like this:

```
TODO: Add a link to the deployed Heroku app for your team here, e.g.

* <https://s22-7pm-3-team02.herokuapp.com>  
```

Change it so it looks like this (removing the TODO, and replacing `s22-7pm-3` with your team name:

```
* Production deployment: <https://s22-7pm-3-team02.herokuapp.com>  
```  

That's it for this task.
  
</summary> 
</details>  

<details>
<summary>
Setup Task 6: Push main branch to team02 heroku qa (must be done after 2)
</summary> 
  
This is the same as Setup Task 5, except for the qa deployment instead of prod.
  
To save time, we are going to reuse the Heroku prod instance from team02 for team03.
  
A link to the dashbaord of your team02 Heroku qa insttance appears below. Check that it's still active.
  

| Section | 1 | 2 | 3 | 4 |
|-|-|-|-|-|
| 4pm | [s22-4pm-1-team02-qa](https://dashboard.heroku.com/apps/s22-4pm-1-team02-qa) | [s22-4pm-2-team02-qa](https://dashboard.heroku.com/apps/s22-4pm-2-team02-qa) |  [s22-4pm-3-team02-qa](https://dashboard.heroku.com/apps/s22-4pm-3-team02-qa) | [s22-4pm-4-team02-qa](https://dashboard.heroku.com/apps/s22-4pm-4-team02-qa) | 
| 5pm | [s22-5pm-1-team02-qa](https://dashboard.heroku.com/apps/s22-5pm-1-team02-qa) | [s22-5pm-2-team02-qa](https://dashboard.heroku.com/apps/s22-5pm-2-team02-qa) |  [s22-5pm-3-team02-qa](https://dashboard.heroku.com/apps/s22-5pm-3-team02-qa) | [s22-5pm-4-team02-qa](https://dashboard.heroku.com/apps/s22-5pm-4-4team02-qa) | 
| 6pm | [s22-6pm-1-team02-qa](https://dashboard.heroku.com/apps/s22-6pm-1-team02-qa) | [s22-6pm-2-team02-qa](https://dashboard.heroku.com/apps/s22-6pm-2-team02-qa) |  [s22-6pm-3-team02-qa](https://dashboard.heroku.com/apps/s22-6pm-3-team02-qa) | [s22-6pm-4-team02-qa](https://dashboard.heroku.com/apps/s22-6pm-4-team02-qa) | 
{:.table .table-sm .table-striped .table-bordered}  
 
Make sure that the application is still up, and that you can use Google OAuth to login.
  
If so, then to save time: *do not change the name of the app*.  If you do, then OAuth will break, since it depends on exactly the name you already have.
  
Since team03 builds on team02, it's fine for us to use the same deployment.
  
<em>Note: At the time of this exercise, 05/12/2022,  the Heroku/GitHub interface in the web dashboard is disabled, due to a security breach at Heroku. If/when it's restored, the following instructions could be simplified.  For now, we have to do this at the command line. </em>
  
Next, you'll want to clone the repo on your local system. 

Change directory (`cd`) into the repo, and then issue this command, substituting in your Heroku app name:
  
```
heroku git:remote -a s22-4pm-2-team02-qa --remote heroku-qa
```
  
Then, do this command to push the main branch to the Heroku deployment:
  
```
git push heroku-qa main
```
  
This should deploy the starter code to the Heroku app.  
  
If it works, you have just one more step: Edit the `README.md` of your main repo to fix the link to the production deployment.

It will start out looking like this:

```
TODO: Add a link to the deployed Heroku qa app for your team here, e.g.

* <https://s22-7pm-3-team02-qa.herokuapp.com>  
```

Change it so it looks like this (removing the TODO, and replacing `s22-7pm-3` with your team name:

```
* QA deployment: <https://s22-7pm-3-team02-qa.herokuapp.com>  
```  

That's it for this task.  
  
Note however, that if/when you need to deploy other branches to the qa site, this is the syntax:
  
```  
git push heroku-qa my-feature-branch:main
```  
  
You should typically announce this on the team's slack channel before pushing; this helps to avoid conflicts where two team members push to -qa at the same time.
 
If that becomes a bottleneck, you can create as many additional -qa deployments as you need.  They will need to be added to the list of authorized redirect URIs on Google OAuth (or else you'll need to create a separate OAuth Client Id and Client Secret value for each one.)
  
</details>  


# Adding Issues

Now, each of you may choose to continue working on the same database table that you did in team02, or you can choose to mix it up; that's a decision I'll leave up to the team.

As a reminder, these are the six tables:

* Menu Item
* Organizaton
* Recommendation
* Review
* Help Request
* Article

Choose which of these you are going to work on.  Then, for your database table, you are going to add a few issues to the Kanban board.

The easiest way to do this is to start by creating *Cards* on the Kanban board, and then *Converting them to Issues*.

Here is what that process looks like:

![create-card-convert-to-issue](https://user-images.githubusercontent.com/1119017/167974490-12699832-a56b-4e41-9ac5-cca96f31c1a3.gif)

Here are the cards you need to create.  I'm using `Recommendation` as the example here; substitute in your database table name in place of that.

* Add Recommendation menu to nav bar
* Add Placeholder for Recommendation Index Page
* Add RecommendationTable component to Storybook (along with fixtures)
  - Note that you can include the DeleteColumn at this stage, or not; your choice.
* Replace RecommendationTable placeholder page with one that includes Recommendation Table
* Add Delete Column to RecommendationTable (if not already done)

The idea is that you should *make a separate pull request* for each of these issues; and it should be code reviewed and merged separately.

For each, you should get all of the tests to pass before moving on to the next issue. 
* You may find this annoying at first, and you may think that it will slow you down.
* That may be true when you are working as an individual
* But keep in mind: up until now, and still including this team project, the tasks are designed so that you stay out of each other's way.
* When it comes to the real project, you'll constantly be in each other's way, unless you work in *very small pieces*, adding the test
  coverage *as you go*.
* This exercise is designed to help you develop that skill.

Once you've made the cards and converted them to issues, the next step is to add detail to each issue, including acceptance criteria.

<details>
<summary>
Setup Task 2: Populating your team03 repo with the starter code
</summary>
  
</details>


<details>
<summary>
Setup Task 3: Setting up -qa and -docs qa repos (must be done after 2)
</summary>
  
</details>

<details>
<summary>
Setup Task 4: Connecting repo to prod Heroku deployment (must be done after 2)
</summary>
  
</details>


<details>
<summary>
Setup Task 5: Connecting repo to qa Heroku deployment (must be done after 2)
</summary>
  
</details>


# Set up that needs to be done by each team member




# Open up issues to work with them.

At a later stage, you'll be adding acceptance criteria. To do that you need to go to the full issue view.  Here's how that looks:

![open-issue](https://user-images.githubusercontent.com/1119017/167975328-26f20584-4fbe-4f21-9799-30cf77960e97.gif)

# Confusion about closing issues

Take note of the `Close Issue` button.  A common mistake is to confuse two things:
* The *window* for an issue can be open or closed
* The *issue itself* can be:
  - open (as in still being worked on) or 
  - closed (as in, we're done with this issue)

If you have the *window* for an issue open on the Kanban board, here is how you close it:

![close-issue-window](https://user-images.githubusercontent.com/1119017/167975653-10970b78-b9ca-4ce7-aa87-2f1ac5523dd2.gif)


By contrast, if you accidentally click the Purple "close issue" button when you really just intended to close the user interface (I do this several times a week), here is how you reopen it.  Note that you may have to move it on the Kanban board as well, since closing an issue might automatically move it around. Here's what that looks like:

![accidentally-close-issue](https://user-images.githubusercontent.com/1119017/167975893-3a63137a-af23-4552-a2a8-15c22a45946b.gif)

# About acceptance criteria

A well written issue should have:
* A clear and consise title
* A clear description
* Acceptance criteria

Learning to write good  acceptance critera is a *crucial skill*.  You want to think like an adversary: i.e. someone that is trying to trick you.   The acceptance criteria should be written in such as way that if you had a really lazy programmer on your team, there is no way that they could pass the acceptance criteria without actually doing everything that is needed for the feature to work.

As an example, suppose the issue is "Add Recommendations to the nav bar".

If your acceptance criteria consists only of:

- [ ] Add `Recommendations` to Nav Bar

Then the programmer could add the word "Recommendations" as static text (rather than as a pull down menu) and strictly sopeaking, they would have satisfied the acceptance criteria. But, they clearly would *not* have done what was intended!

So better is:

- [ ] There is a pull down menu on the Nav bar with the label `Recommendations`.
- [ ] When that label is clicked, we see a menu with a single open: "List Recommendations".
- [ ] When the "List Recommendations" option is selected, the browser window goes to the route `/recommmendations/list`

# Adding Acceptance criteria to your issues: the mechanics

The mechanics of adding acceptance criteria to your issues are these:
* Use the markdown syntax `- [ ]` at the start of each acceptance criterion:

  ```
  - [ ] There is a pull down menu on the Nav bar with the label `Recommendations`
  ```
* There is a button that will put this in automatically, as illustrated here.  Also, once you enter a single criterion, if you press enter, the next line will automatically be filled in with the prefix for the next criterion.
  
  ![add-acceptance-criteria](https://user-images.githubusercontent.com/1119017/167977053-ad548bff-cd19-40c0-a621-6d15a1526a71.gif)

* You can reorder criteria by clicking and dragging as shown here:

  ![reorder-criteria](https://user-images.githubusercontent.com/1119017/167977256-b10f323b-0d65-4a3d-9be2-18064f31da3e.gif)

# Content of your acceptance criteria

Now that you understand the idea of acceptance criteria, and how to enter them, we are going to leave it up to you to decide how to write them out.

We encourage you to seek feedback from each other during your code reviews on whether the acceptance criteria are well-written.   If they are reasonable, we'll give you full credit, but if they are missing or sloppy, your team may lose points.

Keep in mind that the team03 grade is a *team grade* and not an individual grade.  So please hold one another accoutable for writing good acceptance criteria.  If you are not sure, ask the staff for guidance.


# More details on team03

In this team project, our starter code has a frontend and backend, and we are focusing only on the frontend; you will likely not have to make any modifications to the backend.

We are focusing on learning these new React concepts:

* Adding new items to the navbar
* Adding components for new placeholder pages
* Adding routes in `App.js` to link urls to pages
* Creating a component that uses the `OurTable` component to create a table
* Changing the placeholder page so that it loads data using the `useBackend` hook to fetch data
* Using the `ButtonColumn` feature of `OurTable` to add a delete button 
* Using `npm test` to run unit tests
* Using `npm run coverage` to run test coverage
* Using `npx stryker run` to run mutation coverage
* Using `npm run storybook` to visualize frontend components in isolation
 

## Copying your team02 work into the starter code.

You'll start with the starter code `STARTER-team03`, and then add to it the files you created in team02 to implement
the database tables and backend CRUD operations

These will likely include, for each of the database tables you created in team02:
* A Java class for the `@Entity`
* A Java class for the `@Repository`
* A Java class for the Controller
* A Java class containing Controller tests

The first pull request you make should simply copy those files from your team02 repo into the appropriate directories.


## Your next task: add a menu with one option for each of the six database tables

You'll see on the menu bar that there are menus for Todos, Dining Commons and Dates.

You should add a menu item similar to that for Dining Commons, for the database table you are working on.

* Menu Item
* Organizaton
* Recommendation
* Review
* Help Request
* Article

You'll need to coordinate with your teammates to ensure that you don't end up with merge conflicts.

It may be easier to have one person on the team add all six menu items; that's up to you to coordinate.

## Next Steps

Now, take on each of the issues you added to the Kanban board.

Make a new branch each time, and do a separate pull request for each issue.

The videos for team03 contain the information you need to carry out the steps:


* [Intro to Front End](https://gauchocast.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=6a3feb86-018d-4ff9-9212-ae8e015108de) (1 hr 14 minutes)
* [Adding Delete Button](https://gauchocast.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=76f95008-fe11-4d69-9463-ae9201678437) to Table (18 minutes)
* [FrontEnd Testing part 1](https://gauchocast.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=ef93222e-3712-4adc-872d-ae9300054f55) (20 minutes) (npm run coverage)
* [FrontEnd Testing part 2](https://gauchocast.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=3601f9cc-6bc1-4225-b1ff-ae9300055dc3) (14 minutes) (npm run coverage continued)
* [FrontEnd Testing part 3](https://gauchocast.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=3aa343d8-5aea-4390-9ab6-ae9300121554) (19 minutes) (eslint and stryker)

As you finish each issue:
* Do a pull request, and ask for code reviews
* Check that the CI/CD tests are green. If they aren't fix that before starting the next issue.
* Once CI/CD is green, you do *not have to wait* for the code review and the PR to be merged before staring the next issue;
  you can just make a new branch off the previous branch and continue coding.
* However, we strongly encourage you to work with your team to try to get PRs merged as quickly as possible. Don't let them pile up.

Also, and I can't emphasize this enough: keep each PR small.   We are trying to get you into that habit, because it will pay off in the project phase, and in real world practice.


When all of your issues are either complete, or at least have open pull requests, turn your attention to helping the team to get finished.

# Check in with the team

* See if there are code reviews that you can help with
* See if anyone else on the team needs help with their tasks

# Your next steps

The team03 assignment will be followed shortly by team04, which will use the same repo, code base, and kanban board; you can think of it as "team03 part 2".

In team04, you'll add a data entry form for each of your six database records.   That data entry form will be used for both entering new records (i.e. the POST route)
as well as editing database records (the PUT) route.   You'll also add Create and Edit pages to the pages directory.

You'll then hook up the "edit column" in the table to the Edit page.   That's coming soon.

# Asking for help

  
If you need additional guidance, ask on the `#help-team03` channel, and we'll try to steer you in the right direction.

# When you are done

When all branches are merged to main, all tasks on Kanban board in the done column, please submit on [Gauchospace]({{page.gauchospace_url}})
