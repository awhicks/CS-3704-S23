---
num: "Lecture 15"
lecture_date: 2022-10-25
desc: "(Thu Lecture): Review CATME results, Heroku Concurrent Build Limit, Continue work on team02"
ready: true
---

{% include drop_down_style.html %}

Video: <https://gauchocast.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=2a0584c4-9fae-4ee7-a815-af40018826ad>

# Today in class

* Bryan Zamora Flores has an announcement about **speed advising** (it's in the drop down below)

<details>
  
<summary>
Speed Advising: Wed Nov 2, 2pm-6pm, HFH 1132, Refreshments Served.
</summary>

![Speed Advising Flyer](https://user-images.githubusercontent.com/1119017/198417166-47e30cec-0c79-4cae-9574-0cb73d590997.jpg)

<img src="https://user-images.githubusercontent.com/1119017/198417166-47e30cec-0c79-4cae-9574-0cb73d590997.jpg" alt="speed advising flyer" width="500" />
  
</details>

* We'll briefly discuss 
  - the CATME survey results
  - Heroku concurrent build limit
* Then: standup on team02
* Then: work on team02

# Topics Coming up soon:

* team03 will add frontend development in JavaScript for CRUD operations on top of the backend we've already built
* We'll discuss how to do an "Agile Retrospective", and then do one
* We'll start looking at the legacy code projects

# Heroku Concurrent build limit

If you get this error when deploying on Heroku:

```
The build failed with the message Your account has reached its concurrent builds limit.
```

The tl;dr solution:
* Wait 5 minutes and try again"
* Might also need to coordinate deploys with members of your team (via your team's slack channel)

Details in drop down below:

<details>
<summary>
  More about the `concurrent builds limit` on Heroku
</summary>
  
The "concurrent build limit" is usually only applicable when you are trying to do more than one deploy at a time... e.g. if someone on the team tries to deploy a branch, and then the same person (or someone else) tries to deploy a branch before the first build has finished.

One team thought it meant they needed to delete their older apps (ones that have already received final grades and are no longer needed), e.g.   
jpa02, jpa03, team01.
  
That's not necessarily a bad idea: it may help make sure you don't run out of "free tier minutes" this month (before those go away forever, end of November).
  
But it probably won't address the "concurrent build limit" issue; you can still run into that even with a single app on your Heroku account.
  
I suggest: 
* Configure your prod instance to simply deploy each time there is a push to `main`
  - This can still result in the concurrent build limit being triggered if two PRs are merged in quick succession, but it typically isn't a problem.
* Coordinate deploys to your QA branch via your team slack channel
  - Check that there isn't already a build in progress, and check when the last build was done; you can see this on the `Activity` menu on the Heroku dashboard.  Example:
    
    <img width="642" alt="image" src="https://user-images.githubusercontent.com/1119017/198363761-ebe3b256-7a04-4e3e-b325-6714e3cc2336.png">

  - Send a message like "Deploying branch `xy-post-menuitemreview` to QA site" right before you do it
  
  
</details>




The "concurrent build limit" is usually only applicable when you are trying to do more than one deploy at a time... e.g. if someone on the team tries to deploy a branch, and then the same person (or someone else) tries to deploy a branch before the first build has finished.


phtcon
  < 1 minute ago
You can still run into that even with just a single app on Heroku.   It's a good idea to delete the earlier apps that you no longer need (e.g. jpa02, jpa03, team01) but it won't necessarily make that error go away forever.
Typically, the solution to the "The build failed with the message Your account has reached its concurrent builds limit." error is to just wait 5 minutes and try again :slightly_smiling_face:

# CATME

The results of the first CATME survey have been released.  Log in at <https://catme.org> with your `username@ucsb.edu` email to see them.

Please review them now.

There is some detail about CATME results in the "drop down" (if you click the arrow).

<details>
<summary>
Details about your CATME results
</summary>

After they are released, you should be able to see something like this.  (These are all examples from CMPSC 156 but *not* from this quarter).

<img width="744" alt="image" src="https://user-images.githubusercontent.com/1119017/198357454-2cf7002e-9a95-4aca-9ef2-f548f98a0f84.png">

The three arrows show the student's self-rating, the team average for this student, and the overall average of all team ratings (on this team) for all students on this team.

So in this case, we see that:
* the team rated the student higher than the student rated themself
* lower than the team average
* but not much lower than the team average, and still in the "pretty good to excellent" range.

There will be two boxes like this:
* One for "Contributing to the Team's Work"
* Another for "Interacting with Teammates"

Following that, there are anonymized comments; they include your self-assessment, and the anonymous comment of your teammates.  Again, the example shown below is a real one from CMPSC 156, but not from this quarter's class:

<img width="918" alt="Screen Shot 2022-10-27 at 10 18 35 AM" src="https://user-images.githubusercontent.com/1119017/198356690-950572ba-0fb9-431d-959b-50319ffd3bd5.png">
  
</details>

