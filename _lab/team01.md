---
desc: "Team Project 01: Spring Boot Backend, part 1 (unauthenticated RESTFul APIs)"
assigned: 2022-10-13 17:00
due: 2022-10-20 23:59
github_org: ucsb-cs156-f22
layout: lab
num: team01
ready: true
starter: https://github.com/ucsb-cs156-f22/STARTER-team01
qxx: f22
participation_activity_num: p03
participation_activity_date: "Thursday 10/13/2022"
---

# First team programming assignment: Spring Backend, and working with APIs

This is a team programming assignment.  Each team has it's own repo to complete this assignment, and
you will work as a team.

# Grading

* There are two Gradescope autograders for this assignment: team01a and team01b
* They run different tests.  Both count towards your grade
* You should submit as a team from your main branch, with a group submission for the team
* Please coordinate on your submissions to Gradescope, using your team's Slack channel to coordinate

# Working with a Kanban Board

In this assignment, we'll start practicing with a *Kanban Board*, which is a basic tool used by many software development organizations.
- Every organization has some approach to what is called the *Software Design Life Cycle* or *SDLC*
- Some organizations adopt a formal framework such as *Agile* or *Scrum*
- Others use a more informal or hybrid approach, choosing bits and pieces from various frameworks, keeping what works, and setting aside what doesn't.
- I put myself in that category, embracing a core principle from Agile: *Inspect and Adapt*.
- More on that later.

## What you'll do: Process

From a process standpoint, you are working with a Kanban board.
- A Kanban board is a "visualization of work in progress"
- If you've ever worked with a Trello board, it's a similar idea.
- Originally, a Kanban board was a corkboard, and each item was an index card pinned to it with a thumbtack.
- These days, they are mostly online tools.

In this course, we typically work with four columns labelled:
* "todo", "in progress", "in review" and "done".  

There may be more columns or fewer, though typically at a minimum, there is:
* "todo", "in progress" and "done".

Here's how that will play out in detail:


1. Navigate to the web page for the GitHub organization, i.e. <https://github.com/{{page.github_org}}>.  You'll see a tab for `Projects`. Click on that tab.  You should then see a project for your team for the team01 assignment, e.g. `f22-6pm-1-team01`, `f22-6pm-2-team01`,etc.

2. Open the link for your team's Project.  You should find four columns: `Todo`, `In Progress`, `In Review`, `Done`
3. You will be populating the `Todo` column with a set of tasks, which are called *Issues* in the GitHub implementation of Kanban.  More on how to do this later.
4. Now navigate to your repo for team01, which will have a url such as: <https://github.com/{{page.github_org}}/team01-f22-7pm-2>.  You will see a tab for `Issues`. Click on that tab.
4. You should now see a list of issues. These are the work items your team needs to complete to do the the work for the team01 assignment.  (There may also be some additional housekeeping steps; but these issues are the bulk of the work you need to divide up as a team.) 
5. Each team member will take on an issue, one at a time, assign it to themselves, and move it from the "To Do" column of the Kanban board to the "In Progress" column as you start the issue.  When you are finished with the issue, you move it into the "In Review" column when you've made a "Pull Request" to indicate that the issue is ready for your team members to review. 
6. Ideally, each team member should have exactly one (and only one) issue assigned to them in the In Progress column at a time. 
5. Once a pull request is complete for a given task, you move it into the `In Review` column
   - At this stage, you seek a code review from a member of the team that 
     was not involved in the coding.
   - Also, at this stage, if the PR is not "green on CI", 
     meaning that all of the GitHub actions scripts show green checks, this is when you 
     should address that, before merging the pull request.
6. Only when the PR is merged does the issue get moved into the `Done` column.

Please note that each team has a mentor (those are listed [here](https://bit.ly/cs156-f22-teams) that will be keeping an eye on your Kanban boards.  As long as you are not done with your contribution to the project, you should always have at least one issue in the `In Progress` column (the thing you are working on to contribute to the team's work.)

# The Kanban board belongs to the team

The staff has pre-populated your Kanban board with a number of issues to help you get started.  However, please be aware of these important points:

* There may be things in this assignment description, or other things that your team needs to get done that are *not* included on the Kanban board.
* As/when you find such things, feel free to *add them to the Kanban board yourself*.

The purpose of the Kanban board is primarily to *serve the team* as a visual representation fo the work in progress.  

It is true that since this is a *course*, there is an aspect that you are maintaining the Kanban board for a "grade", as part of an "assignment"&mdash;but the hope is that ultimately, you'll see the intrinsic value of keeping a board like this up-to-date so that the team has way to see what's going on with the project at a glance.

# What are we actually building?

Now let's turn from a discussion of process, to a discussion of the product itself.

This video goes with this introduction:
* On YouTube (public): [team-intro (10:13)](https://youtu.be/jY2BLuEfAgk)

You are building a Spring Boot webapp that *only has a backend*.  The front end code will built in a later team project.

We will use a tool called *Swagger-ui* that:
* builds a temporary front-end that can be used by developers to test the backend.
* provides a way for programmers to automatically build documentation for their backend.

If you want to see an example of what the working web app should look like, you can visit this site:

* <https://staff-team01.herokuapp.com/>

This is an exercise in working with three kinds of APIs as explained in [this short article on APIs](https://ucsb-cs156.github.io/topics/apis.html)

The starter code you are given contains three "controllers", each of which implements a separate backend API:

* The Java class [`EarthquakesController`](https://github.com/ucsb-cs156-f22/STARTER-TEAM01/blob/main/src/main/java/edu/ucsb/cs156/spring/backenddemo/controllers/EarthquakesController.java) implements an API endpoint that provides information about earthquakes within a given distance from Storke Tower, that have a magnitude that is greater than or equal to some minimum specified.
* The Java class [`CountryCodeController`](https://github.com/ucsb-cs156-f22/STARTER-TEAM01/blob/main/src/main/java/edu/ucsb/cs156/spring/backenddemo/controllers/CountryCodeController.java) implements an API endpoint that, given the name of a country, provides information about that country, including a list of latitude and longitude points that mark the outline of that country.
* The Java class [`CollegeSubredditsController`](https://github.com/ucsb-cs156-f22/STARTER-TEAM01/blob/main/src/main/java/edu/ucsb/cs156/spring/backenddemo/controllers/CollegeSubredditsController.java) provides an endpoint that gives a list of subreddits on the social networking site Reddit.com that correspond to various colleges and universities.   This endpoint doesn't need any input.

These three controllers, in turn, rely on three Java classes that each provide a "service".  The service provided, in each case, is a method `getJSON(p1,p2,...)` that may or may not take parameters.  The parameters are the ones that were input to each of the controllers 
* the [`EarthquakeQueryService`](https://github.com/ucsb-cs156-f22/STARTER-TEAM01/blob/main/src/main/java/edu/ucsb/cs156/spring/backenddemo/services/EarthquakeQueryService.java) implements `getJSON(String distance, String minMag)` which is used by the `EarthquakesController`.
* the [`CountryCodeQueryService`](https://github.com/ucsb-cs156-f22/STARTER-TEAM01/blob/main/src/main/java/edu/ucsb/cs156/spring/backenddemo/services/CountryCodeQueryService.java) implements `getJSON(String country)` which is used by the `CountryCodeController`
* the [`CollegeSubredditQueryService`](https://github.com/ucsb-cs156-f22/STARTER-TEAM01/blob/main/src/main/java/edu/ucsb/cs156/spring/backenddemo/services/CollegeSubredditQueryService.java) implements `getJSON()` (with no parameters) which is used by the `CollegeSubredditsController`

For each of these controller / service pairs, there are also tests:

| Controller  | Controller Test | Service  | Service Test |
|-|-|-|-|
| `EarthquakesController` | `EarthquakesControllerTest` | `EarthquakeQueryService` | `EarthquakeQueryServiceTest` |
| `CountryCodeController` | `CountryCodeControllerTest` | `CountryCodeQueryService` | `CountryCodeQueryServiceTest` |
| `CollegeSubredditsController` | `CollegeSubredditsControllerTest` | `CollegeSubredditQueryService` | `CollegeSubredditQueryServiceTest` |
{:.table .table-sm .table-striped .table-bordered}


So you are given those twelve classes.   Your job, as a team, is to implement 24 more classes (4 each), i.e. one row of the following table:

| Controller  | Controller Test | Service  | Service Test |
|-|-|-|-|
| `LocationController` | `LocationControllerTest` | `LocationQueryService` | `LocationQueryServiceTest` |
| `PublicHolidaysController` | `PublicHolidaysControllerTest` | `PublicHolidayQueryService` | `PublicHolidayQueryServiceTest` |
| `RedditController` | `RedditControllerTest` | `RedditQueryService` | `RedditQueryServiceTest` |
| `TidesController` | `TidesControllerTest` | `TidesQueryService` | `TidesQueryServiceTest` |
| `UniversityController` | `UniversityControllerTest` | `UniversityQueryService` | `UniversityQueryServiceTest` |
| `ZipCodeController` | `ZipCodeControllerTest` | `ZipCodeQueryService` | `ZipCodeQueryServiceTest` |
{:.table .table-sm .table-striped .table-bordered}


You can see what those services will look like in Swagger by looking at this example of the finished app running:

* <https://staff-team01.herokuapp.com/swagger-ui/>

That will also give you an idea of what the documentaiton should look like when you've put in all the proper values for the various annotations (the things
that start with `@` in the code.)

# Note: This is an exercise

To be clear: this particular application (with backend services and controllers based on these six APIs) is just an "exercise"; similar to a scrimmage for a sports team, or playing "scales" on a musical instrument. The application we are building doesn't necessarily make sense as a piece of working software, but it will help us to practice some important skills.

The nice thing about this first team activity is that we've structured it so that, for the most part, each contributor's code is independent of the others&mdash; you'll get a first taste of working as a team, but for the most part, your contributions will succeed (or not) independent of your other team members.  

This will probably be the last time that is true, however, so you are encouraged to get to know one another, and help and encourage one another. 

# The Repos you will work in

Here are the links to the repos:

| 5pm | 6pm | 7pm|
|-----|-----|----|
|[team01-{{page.qxx}}-5pm-1](https://github.com/ucsb-cs156-{{page.qxx}}/team01-{{page.qxx}}-5pm-1)|[team01-{{page.qxx}}-6pm-1](https://github.com/ucsb-cs156-{{page.qxx}}/team01-{{page.qxx}}-6pm-1)|[team01-{{page.qxx}}-7pm-1](https://github.com/ucsb-cs156-{{page.qxx}}/team01-{{page.qxx}}-7pm-1)|
|[team01-{{page.qxx}}-5pm-2](https://github.com/ucsb-cs156-{{page.qxx}}/team01-{{page.qxx}}-5pm-2)|[team01-{{page.qxx}}-6pm-2](https://github.com/ucsb-cs156-{{page.qxx}}/team01-{{page.qxx}}-6pm-2)|[team01-{{page.qxx}}-7pm-2](https://github.com/ucsb-cs156-{{page.qxx}}/team01-{{page.qxx}}-7pm-2)|
|[team01-{{page.qxx}}-5pm-3](https://github.com/ucsb-cs156-{{page.qxx}}/team01-{{page.qxx}}-5pm-3)|[team01-{{page.qxx}}-6pm-3](https://github.com/ucsb-cs156-{{page.qxx}}/team01-{{page.qxx}}-6pm-3)|[team01-{{page.qxx}}-7pm-3](https://github.com/ucsb-cs156-{{page.qxx}}/team01-{{page.qxx}}-7pm-3)|
|[team01-{{page.qxx}}-5pm-4](https://github.com/ucsb-cs156-{{page.qxx}}/team01-{{page.qxx}}-5pm-4)|[team01-{{page.qxx}}-6pm-4](https://github.com/ucsb-cs156-{{page.qxx}}/team01-{{page.qxx}}-6pm-4)|[team01-{{page.qxx}}-7pm-4](https://github.com/ucsb-cs156-{{page.qxx}}/team01-{{page.qxx}}-7pm-4)|
{:.table .table-sm .table-striped .table-bordered}

You will get three grades for this assignment:
* You'll get two autograded grades via Gradescope
* You'll may also get a manual grade assigned in Canvas; this will be a check that you've followed the Kanban board and Git/GitHub processes described in the assignment.

# Part 1: Team divides up the work


# Step 1.1: Divide up the six controllers among your team

This step is a part of participation assignment ({{page.participation_activity_num}}), in class on {{page.participation_activity_date}}. 

In the "To do" column on the Kanban board, you'll find issues for implementing the six services.

Divide these up among the six members of your team.  When each team members claims one of the services, they should drag the issue for that service into the `In Progress` column, and then assign the issue to themselves.

The six services are:

* Location look up (enter a string, get back locations in the world along with their latitude/longitude)
* Look up public holidays (enter a year and a country code), get back public holidays
* Reddit query (enter a subreddit name, get back recent reddit posts; whomever does this one needs to have 
     a reddit account.)
* Tides query (enter a start and end date, and a station id, get back high and low tides during that period)
* University query (enter part of a university name, get back all matching universities)
* Zip Code query (enter a zip code, get back information about that zip code).

Each member of the team is responsible for implementing one of these services, the matching controller, and the tests that go along with them.

**NOTE: to get the participation grade for today's class, you MUST actually claim the issue and drag it into the `In Progress` column on the Kanban board during the class period for the participation activity.   If you are not present in class (either in person or online), you might get assigned one of these by your team.
But you only get the particpation grade if you actually did the Kanban board steps in class on the day this was assigned.

# Step 1.2: Deploy the repo, as is, to Heroku

A member of your team should find the issue on the Kanban board for deploying the repo to Heroku,  should drag that issue into `In Progress`, and assign that task to themselves

1. Visit the Heroku Dashboard, and create a Heroku app with the name <tt>cs156-{{page.qxx}}-5pm-1-team01</tt>, substituting in your team number in place of `5pm-1`.
2. On the deploy screen, link your Heroku app to your team's repo, and deploy the main branch.
3. When the app is deployed, you should be able to navigate to the link below for your team, and launch the application.

Heroku Dashboard:

| 5pm | 6pm | 7pm|
|-----|-----|----|
|[{{page.qxx}}-5pm-1-team01](https://dashboard.heroku.com/apps/{{page.qxx}}-5pm-1-team01)|[{{page.qxx}}-6pm-1-team01](https://dashboard.heroku.com/apps/{{page.qxx}}-6pm-1-team01)|[{{page.qxx}}-7pm-1-team01](https://dashboard.heroku.com/apps/{{page.qxx}}-7pm-1-team01)|
|[{{page.qxx}}-5pm-2-team01](https://dashboard.heroku.com/apps/{{page.qxx}}-5pm-2-team01)|[{{page.qxx}}-6pm-2-team01](https://dashboard.heroku.com/apps/{{page.qxx}}-6pm-2-team01)|[{{page.qxx}}-7pm-2-team01](https://dashboard.heroku.com/apps/{{page.qxx}}-7pm-2-team01)|
|[{{page.qxx}}-5pm-3-team01](https://dashboard.heroku.com/apps/{{page.qxx}}-5pm-3-team01)|[{{page.qxx}}-6pm-3-team01](https://dashboard.heroku.com/apps/{{page.qxx}}-6pm-3-team01)|[{{page.qxx}}-7pm-3-team01](https://dashboard.heroku.com/apps/{{page.qxx}}-7pm-3-team01)|
|[{{page.qxx}}-5pm-4-team01](https://dashboard.heroku.com/apps/{{page.qxx}}-5pm-4-team01)|[{{page.qxx}}-6pm-4-team01](https://dashboard.heroku.com/apps/{{page.qxx}}-6pm-4-team01)|[{{page.qxx}}-7pm-4-team01](https://dashboard.heroku.com/apps/{{page.qxx}}-7pm-4-team01)|
{:.table .table-sm .table-striped .table-bordered}

Running App:

| 5pm | 6pm | 7pm|
|-----|-----|----|
|[{{page.qxx}}-5pm-1-team01](https://{{page.qxx}}-5pm-1-team01.herokuapp.com)|[{{page.qxx}}-6pm-1-team01](https://{{page.qxx}}-6pm-1-team01.herokuapp.com)|[{{page.qxx}}-7pm-1-team01](https://{{page.qxx}}-7pm-1-team01.herokuapp.com)|
|[{{page.qxx}}-5pm-2-team01](https://{{page.qxx}}-5pm-2-team01.herokuapp.com)|[{{page.qxx}}-6pm-2-team01](https://{{page.qxx}}-6pm-2-team01.herokuapp.com)|[{{page.qxx}}-7pm-2-team01](https://{{page.qxx}}-7pm-2-team01.herokuapp.com)|
|[{{page.qxx}}-5pm-3-team01](https://{{page.qxx}}-5pm-3-team01.herokuapp.com)|[{{page.qxx}}-6pm-3-team01](https://{{page.qxx}}-6pm-3-team01.herokuapp.com)|[{{page.qxx}}-7pm-3-team01](https://{{page.qxx}}-7pm-3-team01.herokuapp.com)|
|[{{page.qxx}}-5pm-4-team01](https://{{page.qxx}}-5pm-4-team01.herokuapp.com)|[{{page.qxx}}-6pm-4-team01](https://{{page.qxx}}-6pm-4-team01.herokuapp.com)|[{{page.qxx}}-7pm-4-team01](https://{{page.qxx}}-7pm-4-team01.herokuapp.com)|
{:.table .table-sm .table-striped .table-bordered}

The result of visiting the home page of the app in the browser should be something like this:
   
```json
{"api-documentation":"http://localhost:8080/swagger-ui/","greeting":"Greetings from Spring Boot","repo":"https://github.com/ucsb-cs156-f22/STARTER-team01","team":["Andrew L.","Bryan T.","Calvin J.","Jacqui M.","Mara D.","Max L.","Phill C.","Wade V."]}
```
   
It might also be nicely formatted, depending on whether you have any browser extensions installed for processing JSON:
```json
{
  api-documentation: "https://starter-team01.herokuapp.com/swagger-ui/",
  greeting: "Greetings from Spring Boot",
  repo: "https://github.com/ucsb-cs156-f22/STARTER-team01",
  team: [
    "Andrew L.",
    "Bryan T.",
    "Bryan Z.",
    "Kevin H.",
    "Phill C.",
    "Pranav M.",
    "Seth V."
  ]
}
```

At a later step (Step 3.2) you'll customize this with links for your team and with the names of your team members.  But we're getting ahead of ourselves.

# Step 1.3: Give team and staff access to your Heroku Deployment

Please visit the `Access` tab of the Heroku Dashboard for your deployed app.

Add each of the members of your team.

Then also add the assigned LA and TA for your team.   
* You can find their names here: <https://bit.ly/cs156-f22-teams>
* To get the email that you should use for Heroku, consult the Staff pinned post on the annoucements channel.
* Then add `phtcon@ucsb.edu`, the instructor for the course.

   
# Part 2: Work as an individual on your service

In this part of the lab, you work as an individual, on your part.  You may get help from other team members&mdash;in fact you are strongly encouraged to do so!  Pairing on this is a great idea!  But, you should be doing the commits and pull requests from your github account so that you and your team gets credit.

This Video (about 40 minutes) walks you through steps 2.0 through 2.4
* [On Youtube](https://youtu.be/mdh9LJ3RSOQ)

* It's a little longer than I had hoped, because part way through I run into a mistake, and have to debug my way out of it.
* This was already my second attempt at making this one, so rather than start over *again*, I just rolled with it.
* It's a great opportuntiy to see if you can spot my mistake before I do, and to see what steps I took to try to figure out what was going on.

A video for steps 2.5, 2.6, and 2.8 (about 15 minutes) appears here: [Team01 Steps 2.5, 2.6 and 2.8](https://youtu.be/QtlirGJjkz4)

## Step 2.0: Optional, but recommended: install VSCode extension for Lombok

This step is optional, but highly recommended.  If you like, you may come back and do this later
as the need arises.

In this lab, we'll be using a package called Lombok. Lombok makes many things easier, 
by writing boring "cookie-cutter" (also known as "boilerplate") code for you!   However this can cause VSCode to
get confused; VSCode says: "dude, you don't have getters and setters!" or "your variable `log` is undefined!"

To help VSCode not be confused, look under VSCode Extensions, and install this one:

* <https://marketplace.visualstudio.com/items?itemName=GabrielBB.vscode-lombok>


## Step 2.1: Clone the repo to your own machine (or CSIL account)

Clone the team's repo to your own machine or CSIL account, with `git clone repo-url`, then cd into the repo and open it up in your editor (we suggest VSCode).

* OR try opening it in a GitHub Codespace

Then try running `mvn spring-boot:run` and opening up the server on <http://localhost:8080>.

Try navigating to <http://localhost:8080/swagger-ui/> and trying out the various APIs.

Then when you are ready to start coding, we'll move on to Step 2.2.

## Step 2.2: Create a new branch

First come up with a branch name, using this convention: `Firstname-Servicename`, for example:
* If your name is Chris, and you are working on the `PublicHolidayService`, call your branch `Chris-PublicHoliday`
* If your name is Taylor, and you are working on the `ZipCodeService`, call your branch `Taylor-ZipCode`

To create your branch, cd into your cloned repo, and use this command:

```
git checkout main
git pull origin main
git checkout -b Chris-PublicHoliday`
```

This creates a new branch `Chris-PublicHoliday` that is branched off a fresh copy of the main branch.

You'll do all of your work in this branch, and when you are done, you'll do a *Pull Request* to get your code into the `main` branch.  

* *Note that using this workflow is a required part of the assignment*.   
* We are practicing a workflow (the GitHub feature-branch/pull-request workflow) that will become super important later in the course, and even more important when you work on real world projects.

## Step 2.3: Implement the Service you were assigned

Now, in the directory `src/main/java/edu/ucsb/cs156/spring/backenddemo/services`, you should find the "stub" for the service that you are asked to create.  

Each of these services provides a method `getJSON` (which may or may not have parameters, depending on the specifics of the service.)  This `getJSON` method encapsulates a web request to another web application that is our source of information.
Our backend is going to aggregate information from many sources and then, eventually, make it all available to a front-end user interface.

Each of these service works roughly the same as the example `EarthquakeQueryService` or the `CountryCodeQueryService`, so use those services as templates for how to write yours.   
* The `EarthquakeQueryService` and `CountryCodeQueryService` are both provided for you as examples.  Please read over them; we'll also go over them in lecture.  
* The `CollegeSubredditQueryService` is also provided for you, but it works a bit differently; it uses a CSV file as it's data source rather than a JSON web service.  So don't use that as a model for your services. We'll discuss that one in lecture and how it differs from the others.

Now, open up the stub file for your service, and start adding code based on what you see in the two example services.

The first piece of information you need is a value for the endpoint, which is in the table below.

| Service                     | Endpoint | 
|-----------------------------|----------|
| `LocationController`       | `https://nominatim.openstreetmap.org/search/{location}?format=json` |
| `PublicHolidayQueryService` | `https://date.nager.at/api/v2/publicholidays/{year}/{countryCode}` |
| `RedditQueryService`        | `https://www.reddit.com/r/{subreddit}.json` |
| `TidesQueryService`         | `https://api.tidesandcurrents.noaa.gov/api/prod/datagetter?application=ucsb-cs156&begin_date={beginDate}&end_date={endDate}&station={station}&product=predictions&datum=mllw&units=english&time_zone=lst_ldt&interval=hilo&format=json` |
| `UniversityQueryService`    | `http://universities.hipolabs.com/search?name={name}` |
| `ZipCodeQueryService`       | `http://api.zippopotam.us/us/{zipcode}` |
{:.table .table-sm .table-striped .table-bordered}

You will also need some additional documentation about the parameters.  You can find this on the swagger-ui
pages of staff solution, here:
* <https://staff-team01-solution.herokuapp.com/swagger-ui/>

NOTE: The `EarthquakeQueryService` (along with the test for it) has two hard coded parameters in addition to the ones that 
are exposed through the api (i.e. `minMag` for minimum magnitude, and `distance` (for distance in km from Storke Tower).   We 
could have chosen to make those parameters that the user of the API could supply.  And indeed, it would feasible (though 
it isn't part of this assignment) to implement a separate service that allows the user to supply those, or to make 
the lat/long of Storke Tower the default if and only if the user doesn't supply values for those.

But, the bottom line is that *none of the other services you are implementing needs latitude and longitude, especially not that of Storke Tower,
in the implementation.*   So those should not appear in your code for anything other than the `EarthquakeQueryService` and the 
`EarthquakeQueryServiceTests`.   Some might say that the `EarthquakeQueryService` is therefore a bad example for you to work from&mdash;I choose to
think of it differently; it's an example that forces you to really think about what's going on, and what parameters you should retain, vs. which ones
you should not retain.

Additionally, there are some special instructions for the `RedditQueryService` near the bottom of this web page.

As you work on your service, make commits frequently, with meaningful commit messages. 
* Use your initials at the start of your commit message (e.g. `cg` for "Chris Gaucho")
* Separate your initials from your message with a hyphen
* Your message should describe what you did

Examples:

* `git commit -m "cg - added service to get information on zip codes"`
* `git commit -m "cg - correct typo in endpoint url for zip code service"`

Having meaningful commit messages is a component of your grade for this assignment, so please do put some thought into what you write.

As you make commits, push them to your branch, for example:

```
git push origin Chris-Zipcode
```

A few handy commands:
* `git status` shows what branch you are on, among other things
* `git branch -a` shows all current branches
* `git fetch` updates information about branches by pulling new branch names from GitHub

When you're done implementing the first draft, the next step is to write the test for your service

## Step 2.4: Implement the test for the service you were assigned

In the directory `src/test/java/edu/ucsb/cs156/spring/backenddemo/services` you will find tests for the three sample services.  Use these as a model to write a test for your service.

We'll go over the code for these tests in lecture.

Run the tests by running `mvn test` and then check the test coverage with `mvn test jacoco:report`

When that test passes, we'll build the controller and the controller test so that you can try out your service.

## Step 2.5: Implement the controller for the service

A video for steps 2.5, 2.6, and 2.8 appears here: [f22 Team01 Steps 2.5, 2.6 and 2.8](https://youtu.be/QtlirGJjkz4)

In a Spring Boot application, a controller class is one that implements backend endpoints (i.e. provides a web service
on a URL).   You will now implement a controller so that users of your app (in practice, typically, the front end code)
can access the information provided by your service. 

The documentation at the staff solution to the lab <https://staff-team01-solution.herokuapp.com/swagger-ui/> shows the urls of the endpoints you'll be implementing; they 
are also shown in this table:


|  Controller                | Endpoint     |
|----------------------------|--------------|
|  `LocationController`      | `/api/locations/get` |  
|  `PublicHolidayController` | `/api/publicholidays/get` |  
|  `RedditController`        | `/api/reddit/get` |  
|  `TidesController`         | `/api/tides/get` |  
|  `UniversityController`    | `/api/university/get` |
|  `ZipCodeController`       | `/api/zipcode/get` |
{:.table .table-sm .table-striped .table-bordered}


You'll see additional information in the Swagger-ui that is provided by annotations such as these found in the `EarthquakesController`

* `@Api(description="Earthquake info from USGS")`
* `@ApiOperation(value = "Get earthquakes a certain distance from UCSB's Storke Tower", notes = "JSON return format documented here: https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php")`
* `@ApiParam("distance in km, e.g. 100")`

Please:
* Take note of how those are used in the `EarthquakesController`
* Note the similar information that appears in the Swagger-ui interface of the staff solution here: <https://staff-team01-solution.herokuapp.com/swagger-ui/> 
* Add these annotations in the appropriate places in your own Controller so that the documentation matches that of the staff solution.  This is another component of your grade for this assignment.

To check if your controller endpoint is operational, you can run:

```
mvn spring-boot:run
```

And then visit the `/swagger-ui/index.html` endpoint.  You should then be able to test your service interactively.

When it appears to be working, make a commit, and then we'll move on to the coding part for the individual phase: writing a test for your controller.

## Step 2.6: Write the controller test

In the directory: `src/test/java/edu/ucsb/cs156/spring/backenddemo/controllers` you'll find example controller tests.

Using those as a model, implement a controller test for your controller.

Run the tests by running `mvn test` and then check the test coverage with `mvn test jacoco:report`

## Step 2.7: Removed

(This step was a repeat of step 2.4, we we've removed it, but
we didn't renumber since the videos are referring to steps by number.)


## Step 2.8: Make a Pull Request

* Navigate to your repo on the GitHub website
* Go to the Pull Requests tab
* Click to create a new pull request
  - the `base` branch should be `main` (this is where your code will be "pulled into")
  - the `compare` branch should be your feature branch, e.g. `Chris-Zipcode`
  - for the title, put in something like "Add ZipCode Service and Controller"
* For the PR description, enter something like this 

  ```
  In this PR, we add an endpoint `/api/zipcode/get` that can be used to get information
  about the location of a particular zipcode.  
  ```
* Then, once the PR is created, add your team members as code reviewers
* Do not merge your own PR.  You should wait until another member of your team has code reviewed it, 
  and then they can do the merge.
* Once you've made your PR, drag the card for your issue into the `In Review` column on GitHub
* Link your PR to the issue. One way to do this by putting `Closes #13` in the text of the PR description (where `13` is the issue number.)  There are also ways to link issues with PRs in the GitHub web interface. 


## Step 2.9: Try submitting your branch on Gradescope

Now, go to the [team01 assignment on Gradescope]({{page.gradescope}}) and submit from the team's repo, and from your branch (`Name-Topic`) rather than the `main` branch (there's a drop down where you can select the branch) to see
if the tests pertaining to your service/controller are passing.  Don't worry (for now) about the other tests for the moment; just try to get the tests for your own service/controller to pass.

# Part 3: Back to the team 

## Step 3.1: Review and merge the PRs

Now, as a team, look at one another's PRs.  You should be able to do a code review (we'll demonstrate how that works in lecture), and approve the PR with the comment `LGTM` (`Looks Good To Me`, or `Let's Get This Merged`).
* Note that "commenting LGTM" is not the same as doing an "Approving Code Review" with the comment `LGTM`.  You need the latter.
* It's also a good idea to try it out. Here are three ways:
  - You can check out the branch, then run `mvn spring-boot:run` to test the code.
  - You can also deploy the branch in the PR to Heroku and try it there.
  - Finally, you can try submitting that branch to Gradescope and see if it passes it's tests
* When the *team* is satisfied with the code for one of the branches, you can merge that branch into main by clicking the "Merge" button on the PR.
* When a PR is merged, drag it's card into the Done column on the Kanban board.



## Step 3.2: Customize the `HomeController`

Now, someone on the team should assign themeslves the issue for customizing the Home Controller and should drag that issue into the "In Progress" column.


Make a branch, `YourName-HomeController` (e.g. `Alex-HomeController`), and
update the code in `HomeController` so that:

* instead of a list of the staff names, there is a list of the names of the people on your team that contributed to this repo
* instead of a link to <tt>https://github.com/ucsb-cs156-{{page.qxx}}/STARTER-team01</tt>, there is a link to your team's private repo (e.g. <tt>https://github.com/ucsb-cs156-{{page.qxx}}/team01-{{page.qxx}}-5pm-1</tt>

Make these changes, test them, and then make a PR for this, and merge it. (Following the usual steps of dragging to the `In Review` column, and then the `Done` column.)

## Step 3.3: Finish the changes to the README.md

Now, someone else on the team should assign themselves the issue for making
changes to the README.

Make a  branch, `YourName-READMEFixes` (e.g. `Alex-READMEFixes`), and
update README.md, so that all of the places that say "TODO" are replaced with the appropriate content.

Make these changes, test them, and then make a PR for this, and merge it. (Following the usual steps of dragging to the `In Review` column, and then the `Done` column.)

When items 3.1, 3.2, and 3.3 are done, and all of the PRs are merged, you are ready to submit for your team on Gauchospace.


# Part 4: Submission

## Step 4.1  Deploy your main branch on Heroku

Deploy your repos main branch on your team's shared Heroku deployment.  Here's the dashboard link:

| 5pm | 6pm | 7pm|
|-----|-----|----|
|[{{page.qxx}}-5pm-1-team01](https://dashboard.heroku.com/apps/{{page.qxx}}-5pm-1-team01)|[{{page.qxx}}-6pm-1-team01](https://dashboard.heroku.com/apps/{{page.qxx}}-6pm-1-team01)|[{{page.qxx}}-7pm-1-team01](https://dashboard.heroku.com/apps/{{page.qxx}}-7pm-1-team01)|
|[{{page.qxx}}-5pm-2-team01](https://dashboard.heroku.com/apps/{{page.qxx}}-5pm-2-team01)|[{{page.qxx}}-6pm-2-team01](https://dashboard.heroku.com/apps/{{page.qxx}}-6pm-2-team01)|[{{page.qxx}}-7pm-2-team01](https://dashboard.heroku.com/apps/{{page.qxx}}-7pm-2-team01)|
|[{{page.qxx}}-5pm-3-team01](https://dashboard.heroku.com/apps/{{page.qxx}}-5pm-3-team01)|[{{page.qxx}}-6pm-3-team01](https://dashboard.heroku.com/apps/{{page.qxx}}-6pm-3-team01)|[{{page.qxx}}-7pm-3-team01](https://dashboard.heroku.com/apps/{{page.qxx}}-7pm-3-team01)|
|[{{page.qxx}}-5pm-4-team01](https://dashboard.heroku.com/apps/{{page.qxx}}-5pm-4-team01)|[{{page.qxx}}-6pm-4-team01](https://dashboard.heroku.com/apps/{{page.qxx}}-6pm-4-team01)|[{{page.qxx}}-7pm-4-team01](https://dashboard.heroku.com/apps/{{page.qxx}}-7pm-4-team01)|
{:.table .table-sm .table-striped .table-bordered}

Double check that:
* the running app shows your team members names (i.e. that Step 3.2 above was done correctly)
* that each of the other controllers works properly and returns good results (check this by interactively testing through the swagger-ui interface)

## Step 4.2  Each team member must submit team01a individually from the main branch on Gradescope

Once all of the PRs for the team are merged, *each* team member should find [assignment team01 on Gradscope]({{page.gradescope}}), submit from the team's repo, and the `main` branch on Gradescope.  The main branch should now contain all team member's work.

*Do not simply assume that your team will submit on your behalf*.

To help promote both team and individual accountability, I am asking each team member to submit the team's work to Gradescope separately, after all of the PR's are merged.

I would like to see which team members are actually in touch with their teams and engaged with the process&mdash;hopefully that's everyone.   This mutual team accountability will be an important skill during the project phase of the course, so we are practicing it with a programming assignment now (which is a "lower stakes" part of your course grade.)

## Step 4.3  One team member can submit team01b on Gradescope on behalf of the team

You will get one grade for this assignment out of 100 points based on the Gradescope autograder.

Please be sure that all team members names are included in this group submission.

   
# Special Instructions for the RedditQueryService
 
The Reddit Query service will work just like the other services, except that you may get frequent errors 
of the form `429 Too Many Requests` as described in [this Stack Overflow post](https://stackoverflow.com/questions/30992791/http-429-too-many-requests-when-accessing-a-reddit-json-page-only-once-using-ja).   The fix is to add this line of code,
which you should customize with your reddit id (put it in place of `cgaucho`).

```java
   headers.set("User-Agent","spring-boot:cs156-team01:f22 (by /u/cgaucho)")
```

This goes immediately after these lines of code, which you'll find in the example services:

```java
   HttpHeaders headers = new HttpHeaders();
   headers.setAccept(List.of(MediaType.APPLICATION_JSON));
   headers.setContentType(MediaType.APPLICATION_JSON);
```



