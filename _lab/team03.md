---
desc: "Team Project: FrontEnd CRUD, part 1: Index Page, and Delete Column"
assigned: 2022-11-02 17:00
due: 2022-11-10 23:59
github_org: ucsb-cs156-f22
layout: lab
num: team03
ready: true
starter: "git@github.com:ucsb-cs156-f22/STARTER-team03.git"
---


{% include drop_down_style.html %}


# Set up tasks for lab on Wednesday 11/02

You should have six team members, and there a six setup tasks to do. So ideally, you'd divide these up
one per person.

But, if you have fewer than six team members present today, I suggest you still try to 
get all six of these done with the team members you do have.

Note that there is an order here, so keep that in mind when organizing tasks:

* Setup Task 1: Creating your team's Kanban board (can be done at any time)
* Setup Task 2: Populating team03 repo with starter code (can be done at any time)
* Setup Task 3: Set up -docs and -docs-qa repos (must be done after 2)
* Setup Task 4: Set up Google OAuth (may be done at any time, but must be coordinated with 5 and 6)



## Big Picture: what is team03 all about?

From a high-level standpoint, you'll be doing these things:

Coding Tasks:
* Adding some front end components for each of your six database tables
* Adding tests for these

# Set up Tasks

There are several set up tasks.  I suggest that you divide these up among your team, and indicate on the team slack channel who is doing what.

Here's the full list, followed by more detail about each one (in the dropdown boxes indicated by the triangles;  **_click the triangle_** (▶) to reveal the steps for each one.

Ideally, if you have six team members available to help out, each team member will do one of these.  If you have fewer than six team members available, I suggest combining either (3,4) or (5,6) since they  are quite similar, and can easily be done quickly by the same person.


<details>
<summary>
Setup Task 1: Creating your team's Kanban board
</summary>

1. **Make sure you are the only person creating a Kanban board for your team**
  
   - Tell the rest of the team (via your Slack channel) that you are setting up the Kanban board (so that you don't have two folks doing it at the same time.)
   
   - Before you do, make sure that someone else didn't already post that they were creating the Kanban board for the team.  And wait a few seconds
     to be sure that there isn't someone else typing in that they are doing it at the exact same time.
  
   - If your entire team is in meeting person, you can also just check in with them in person.

2. Go to this URL: https://github.com/orgs/ucsb-cs156-f22/projects

3. Click "Add Project".  In the modal that pops up, select "New Board".  (If you accidentally create a table, you can convert it to a Board later.)
  
4. Name your project team03-f22-6pm-3 (substitue your team name)
  
5. Then, share your project with your team.  You don't need to share it one person at a time.
  
  
</details>
  
<details>
<summary>
Setup Task 2: Populating team03 repo with starter code
</summary>
  
One team member should clone the team03 repo, which should be found here:
  
| Section | 1 | 2| 3| 4| 
|-|-|-|-|-|
| 5pm | [team03-f22-5pm-1](https://github.com/ucsb-cs156-f22/team03-f22-5pm-1) | [team03-f22-5pm-2](https://github.com/ucsb-cs156-f22/team03-f22-5pm-2)    | [team03-f22-5pm-3](https://github.com/ucsb-cs156-f22/team03-f22-5pm-3) | [team03-f22-5pm-4](https://github.com/ucsb-cs156-f22/team03-f22-5pm-4) | 
| 6pm | [team03-f22-6pm-1](https://github.com/ucsb-cs156-f22/team03-f22-6pm-1) | [team03-f22-6pm-2](https://github.com/ucsb-cs156-f22/team03-f22-6pm-2)    | [team03-f22-6pm-3](https://github.com/ucsb-cs156-f22/team03-f22-6pm-3) | [team03-f22-6pm-4](https://github.com/ucsb-cs156-f22/team03-f22-6pm-4) | 
| 7pm | [team03-f22-7pm-1](https://github.com/ucsb-cs156-f22/team03-f22-7pm-1) | [team03-f22-7pm-2](https://github.com/ucsb-cs156-f22/team03-f22-7pm-2)    | [team03-f22-7pm-3](https://github.com/ucsb-cs156-f22/team03-f22-7pm-3) | [team03-f22-7pm-4](https://github.com/ucsb-cs156-f22/team03-f22-7pm-4) | 
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
 
This task has three parts:
  
* Part 1: Enable Actions, Set up `DOCS_TOKEN`, Run job to create `-docs` and `docs-qa` repos
* Part 2: Give whole team admin access to `-docs` and `-docs-qa` repos, and enable GitHub pages
* Part 3: Run jobs to set up Storybook, and adjust links in README.md

## Part 1: Enable Actions, Set up `DOCS_TOKEN`, Run job to create `-docs` and `docs-qa` repos
  
  
In this task, you'll set up a GitHub Pages site for documentation of your code base; for now, that just consists of the published Storybook, which is
an interactive catalog of all of your React components.

To do this, follow these steps:
  
1.  Go to the Actions tab of your repo, and if Actions is not already enabled, enable it.
  
2.  Go to the settings page for your personal GitHub account, like this:
  
    <img width="237" alt="image" src="https://user-images.githubusercontent.com/1119017/168149677-706a468e-85e8-4186-8265-7e4a90fbb511.png">

3.  Find the Developer Settings in the left navigation, near the bottom.
  
    <img width="228" alt="image" src="https://user-images.githubusercontent.com/1119017/168149892-44de1722-3416-4378-b78a-c3928b0ccb6d.png">

4.  On the developer settings, choose `Personal Access Token`
    <img width="274" alt="image" src="https://user-images.githubusercontent.com/1119017/168149966-7d4fdc82-2bb8-4d18-8f20-57fddbc04e08.png">

5.  Click `Generate New Token`.  You'll need to confirm your password.
    <img width="693" alt="image" src="https://user-images.githubusercontent.com/1119017/168150055-f221a3ac-a8f3-4cd6-aacb-f7fbd8f33fc2.png">

6.  Fill in the description with your team03 repo name (like shown below). Note that the description is just for humans, so the formatting doesn't have to be exact.  This is just so you can remember what the token is for.

    Select 90 days for the expiration, and then select `repo` as the only scope (it includes all the detailed scopes underneath).
  
    <img width="668" alt="image" src="https://user-images.githubusercontent.com/1119017/168150417-f7d096ee-b3a7-4403-8d55-ca0337a561f1.png">

    Finally, scroll down and click `Generate Token`.

    <img width="299" alt="image" src="https://user-images.githubusercontent.com/1119017/168150606-427be326-828c-47ef-af04-f399254d06c5.png">

     You'll be shown a token value (this one is fake and has been deactivated).  Copy it, because once you close the window it's gone, but
     DO NOT PASTE IT ANYWHERE except in the secrets portion of your team03 repo (next step).  This value can be used in place of your 
     GitHub password, so you need to protect it.
  
     <img width="667" alt="image" src="https://user-images.githubusercontent.com/1119017/168150856-e3623eae-e041-4a02-814c-417566ff1d3a.png">

  
7.   Return to your main team03 repo, and go to Settings page for `Secrets: Actions`  (This is done on the regular `team03-f22-4pm-1` repo, NOT on the `-docs` and `-docs-qa` repos.)

     <img width="270" alt="image" src="https://user-images.githubusercontent.com/1119017/168151099-7508f238-c9f2-4e2a-8721-8cbeb610cc30.png">

     On the Secrets page click `New Repository Secret` then add a secret called `DOCS_TOKEN`.  Be careful here, because the name must be 
     *exactly* `DOCS_TOKEN`, not `DOC_TOKEN` or anything else; this value is referenced in the GitHub workflow scripts.

     <img width="716" alt="image" src="https://user-images.githubusercontent.com/1119017/168151417-37955809-9710-4c28-837d-ba5a7ba0fc12.png">

     After you are done, it should look like this:

     <img width="661" alt="image" src="https://user-images.githubusercontent.com/1119017/168151474-1b17b540-0968-470c-bb8f-ec5c891daa5c.png">

     If you need to replace the secret (e.g. for debugging reason), you can overwrite it, but once you store it, you can't look at it.
     So if you get it wrong, you just have to create a new one; you can't edit the old value.
  
     
      
8. Now, once `DOCS_TOKEN` is updated, and till in your main team03 repo, and go to the page for GitHub Actions (the `Actions` tab).   You should see these workflows in the list on the left:

    <img width="244" alt="image" src="https://user-images.githubusercontent.com/1119017/168151802-c6e22e2f-dd63-49e0-ab06-3d641c75a8e6.png">

   `00-publish-docs-to-github-pages-setup: set up -docs and -docs-qa repos (run once, manually)`

    This should automatically create the repos with `-docs` and `-docs-qa` that will host your React Storybook.  
  
9.  Wait for that jobs to finish, and verify that your `-docs` and `-docs-qa` repos have been created.
  
## Part 2: Give whole team admin access to `-docs` and `-docs-qa` repos, and enable GitHub pages

Go through all of the steps below for *both* the `-docs` and the `-docs-qa` repos.    

1. Visit the Settings page for the repo

2. Visit the `Collaborators and Teams` link (second on left navivation)
   <img width="1133" alt="image" src="https://user-images.githubusercontent.com/1119017/168176108-6f18cc07-5bbc-456e-a080-b84691c0eea1.png">

3. You should see your own GitHub (the one of the person that created the repo) in the list of folks with access. You should click the `Add Team` button (upper right) to add your entire team:
  
   <img width="895" alt="image" src="https://user-images.githubusercontent.com/1119017/168176229-ae70dccf-954f-4db2-b754-c75fbaa989dd.png">

   You'll see this pop-up modal:
  
   <img width="343" alt="image" src="https://user-images.githubusercontent.com/1119017/168176264-ef1b9c26-e457-449d-bd9f-53591e0cce11.png">
  
4. Type in your team name (e.g. `f22-5pm-2`) and the team name shoudl pop up so that you can add it.
   
   <img width="339" alt="image" src="https://user-images.githubusercontent.com/1119017/168176345-1505716e-678d-4e22-8d22-25081d227ddc.png">

5. Click the button, and the modal should change to look like this:
  
   <img width="384" alt="image" src="https://user-images.githubusercontent.com/1119017/168176391-fcf3a6c0-6287-43b9-953b-5e1b50469332.png">

6. Change the permission level to Admin, and the click to add your team.
  
   <img width="384" alt="image" src="https://user-images.githubusercontent.com/1119017/168176410-ad3f3145-be8c-4bf3-974a-4ce7c18055ee.png">

7. It should add your team to the list of folks with access:
  
   <img width="675" alt="image" src="https://user-images.githubusercontent.com/1119017/168176491-1727710e-5c56-440f-9d65-1d4f23b9a1f3.png">

8. Now, still under the `Settings` page for the repo, then look for `Pages` in the left navigation. 
    You want to enable GitHub pages, so that the settings look like this:

    <img width="640" alt="image" src="https://user-images.githubusercontent.com/1119017/168149276-6ebbf519-48ed-4f2e-8137-f7d68dedbb78.png">

Remember: repeat these steps for both `-docs` and `-docs-qa`  
  

## Part 3: Run jobs to set up Storybook, and adjust links in README.md
    
1.  Now return to your main `team03` repo (not the `-docs` or `-docs-qa` but the one with the Java and JavaScript code).
2.  Go under Actions, and click on the job that starts with `02-publish-docs-to-GitHub` and you should see this:

    <img width="1090" alt="image" src="https://user-images.githubusercontent.com/1119017/168151888-dcc54aeb-bbf9-4f3d-97e8-5448a065c9ba.png">

    On the right hand side of the screen, find where it says `Run Workflow`, and click it.  That should expose this box:
  
    <img width="335" alt="image" src="https://user-images.githubusercontent.com/1119017/168152002-c51f67c2-57f7-4291-a856-4daa9ac3cb63.png">

    Click `Run Worfklow`
  
3. Repeat this step for the job that starts with `04-publish-docs-to-GitHub`.
  
4. When each of these two jobs is finished, you should be able to navigate to your GitHub Pages sites at URLs like this (subsitute your own team name):

    * <https://ucsb-cs156-f22.github.io/team03-f22-5pm-3-docs>
    * <https://ucsb-cs156-f22.github.io/team03-f22-5pm-3-docs-qa>
  
    And these links should show a Storybook page like the ones shown below (except your team name will show instead of `STARTER-team03`.  The branches
    listed may be different two, but this is the general idea of what the pages should look like.

    <img width="629" alt="image" src="https://user-images.githubusercontent.com/1119017/168152477-28391f6f-489a-4ff7-82e8-27699d6c2b4c.png">

    <img width="694" alt="image" src="https://user-images.githubusercontent.com/1119017/168152556-1247a9e2-a15b-4dfb-8169-1daf056ec755.png">

  
5. Go into the `README.md` file of your main team03 repo, and edit the links to the documentation.  They will look like this when you start:
  
    ```
    TODO: Add correct links to the -docs and -docs qa GitHub pages sites

    * Storybook (production): <https://ucsb-cs156-f22.github.io/STARTER-team03-docs>
    * Storybook (development/qa): <https://ucsb-cs156-f22.github.io/STARTER-team03-docs-qa>
    ```
  
    After you edit, it should look like this (with links appropriate for your team). Note that you should *remove* the part that says `TODO`.
  
    ```
    * Storybook (production): <https://ucsb-cs156-f22.github.io/team03-f22-6pm-4-docs>
    * Storybook (development/qa): <https://ucsb-cs156-f22.github.io/team03-f22-6pm-4-docs-qa>
    ```
 
That's it for this task.  
  
</details>  
  

<details>
<summary>
Setup Task 4: Google OAuth (may be done at any time, but must be coordinated with 5 and 6)
</summary>
  
Coordinate with the folks doing task 5 and 6 so you know *exactly* what the URL will be for your
prod and qa apps.

Then set up Google OAuth for these.  You can do that by creating a new Google OAuth app, or if you have an existing one,
you can just add more "callback urls" to the list of existing ones, e.g. 

<img width="559" alt="image" src="https://user-images.githubusercontent.com/1119017/199622864-76221ee8-6649-4f51-b9c3-4622cf01044b.png">

Either way, your job is to end up with a value for `GOOGLE_CLIENT_ID` and `GOOGLE_CLIENT_SECRET` that you can put in the
Config vars for your teams prod and qa Heroku deployments.
  
The folks doing Setup Tasks 5 and 6 may set up those values with placeholders, or they may not set them up at all, but it will be your job
to make sure those have the correct values, and that Google OAuth then works.  You will need to collaborate with the folks doing Setup tasks 5 and 6.

You are done when you can login with OAuth on both your prod and qa apps for team03.  
  
</details>
  
<details>
<summary>
Setup Task 5: Push main branch to team03 heroku prod (must be done after 2 and in coordination with 4)
</summary>
  
Create a heroku instance for your team03 app, with a name such as the following (substituting your team):
  
* New app name: `f22-6pm-3-team03`
* Link to Heroku app: <https://f22-6pm-3-team03.herokuapp.com>

  
Then:
  
1. Set up the Heroku app to automatically deploy from main branch of your repo, the This should deploy the starter code to the Heroku app.  
2. Add a config var called `PRODUCTION` with the value `true` 
3. Add the config vars for `GOOGLE_CLIENT_ID` and `GOOGLE_CLIENT_SECRET`; just fill in values `todo` for now; the person doing set up task 4 will
   fill in the real values.
4. Add a config var called `ADMIN_EMAILS` and add all of your team, plus your instructor (`phtcon@ucsb.edu`) and your mentor (the TA or LA listed in <https://bit.ly/cs156-f22-teams>).  Their email can be found pinned to the `announcements` channel on the Slack.
5. Make sure the Heroku app is up and running, and that you can login with your Google account, and see the Admin menu.
6. Add the same folks you add to `ADMIN_EMAILS` as collaborators on the Heroku app (i.e. using the `Add Collaborator`
  button under the `Access` tab:
  
   <img width="854" alt="image" src="https://user-images.githubusercontent.com/1119017/199622077-baf38448-ca51-415c-b118-5f41a75715d2.png">

  
If it works, you have just one more step: Edit the `README.md` of your main repo to fix the link to the production deployment.

It will start out looking like this:

```
TODO: Add a link to the deployed Heroku app for your team here, e.g.

* <https://f22-7pm-3-team02.herokuapp.com>  
```

Change it so it looks like this (removing the TODO, and replacing `f22-7pm-3` with your team name:

```
* Production deployment: <https://f22-7pm-3-team02.herokuapp.com>  
```  

The team member doing step 4 will be getting the correct values for `GOOGLE_CLIENT_ID` and `GOOGLE_CLIENT_SECRET` but they can't do that
unless/until you give them access, which is one of the things you should have done above.
  
You will need to collaborate with the person doing Setup tasks 4.

You are all three done with Setup Task 4, 5, 6  done when the team can login with OAuth on  your prod and qa apps for team03.  
  
  
</details>  

<details>
<summary>
Setup Task 6: Push main branch to team02 heroku qa (must be done after 2 and in coordination with 4)
</summary> 
  
This is the same as Setup Task 5, except for the qa deployment instead of prod.

To save space, I won't repeat the instructions; just refer to those instructions, with these differences:
 
1. Add `-qa` to end of app name, e.g.  
  
   * New app name: `f22-6pm-3-team03-qa`
   * Link to Heroku app: <https://f22-6pm-3-team03-qa.herokuapp.com>
  
2. Do not set up the app to automatically deploy the `main` branch.  Instead, deploy the `main` branch once (or as many times as you need to get the app up and running with OAuth)
   and then leave it for manual deploys of feature branches that need to be tested.
  
The team member doing step 4 will be getting the correct values for `GOOGLE_CLIENT_ID` and `GOOGLE_CLIENT_SECRET` but they can't do that
unless/until you give them access, which is one of the things you should have done above.
  
So, you will need to collaborate with the person doing Setup tasks 4.

You are all three done with Setup Task 4, 5, 6  done when the team can login with OAuth on  your prod and qa apps for team03.  
    
  
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

# Will there be a team04
  
There may or may not be a team04; it depends on how much time is left.
  
If there is, in team04, you'll add a data entry form for each of your six database records.   That data entry form will be used for both entering new records (i.e. the POST route)
as well as editing database records (the PUT) route.   You'll also add Create and Edit pages to the pages directory.

You'll then hook up the "edit column" in the table to the Edit page.   

# Asking for help

If you need additional guidance, ask on the `#help-team03` channel, and we'll try to steer you in the right direction.

# When you are done

When all branches are merged to main, all tasks on Kanban board in the done column, please submit on Canvas as you did for team02.  Link coming soon.
