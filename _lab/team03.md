---
desc: "Team Project: FrontEnd CRUD, part 1: Index Page, and Delete Column"
assigned: 2022-05-12 14:00
due: 2022-05-18 23:59
github_org: ucsb-cs156-s22
layout: lab
num: team03
ready: false
gauchospace_url: update_this_url
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
</details>  
  
<details>
<summary>
Setup Task 3: Set up -docs repo (must be done after 2)
</summary>
</details>  
  
<details>
<summary>
Setup Task 4: Set up -docs-qa repo (must be done after 2)
</summary>
</details>  
  
<details>
<summary>
Setup Task 5: Push main branch to team02 heroku prod (must be done after 2)
</summary> 
</details>  

<details>
<summary>
Setup Task 6: Push main branch to team02 heroku qa (must be done after 2)
</summary> 
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
