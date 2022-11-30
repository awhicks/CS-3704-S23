---
num: "Lecture 27"
lecture_date: 2022-11-30
desc: "Wed Discussion: Get PRs merged, plan video"
ready: true
---

{% include drop_down_style.html %}


# ESCIs: please don't forget to fill them out!

They are super important.

# Final CATME survey, and the end of quarter post-survey

* You'll get a link to final CATME survey over the weekend.
* Link to post survey (for extra credit) will be showing up on Slack and Canvas soon.

If you did not fill out the pre-survey, but would still like to do so for extra credit, 
and/or to offer your informed consent to allow us to use your data for research,
let me know via Slack DM and I'll send you the link.

# Final Exam Slot: for presentations

The instructions for the final video are listed below.
* The final video presentations will take place during our finals week slot
* You are not required to attend in person, but you are required to participate;
  - There's a participation grade for providing feedback on one another's presentations
  - There's a live demo component as well, and your team needs to be represented there.

# Today

* Get PRs merged
* Plan for video



<details>
<summary>
Getting PRs merged
</summary>

# Getting PRs merged

  
Let me encourage you to take the PR that's at the head of the queue (i.e. the oldest one for your team), and if it's in a mergeable state (i.e. passing CI/CD, has peer code review, no outstanding changes requested) then deploy it to your QA branch, with a post like this one:

```
Deploying: sheila-pr-37-add-cow-death-controller
PR https://github.com/ucsb-cs156-f22/f22-6pm-happycows/pull/62
on QAs site; https://dashboard.heroku.com/apps/f22-6pm-4-happycows-qa
Build Progress: https://dashboard.heroku.com/apps/f22-6pm-4-happycows-qa/activity/builds/c122de5b-20a5-4841-94c9-0621b7d51d1a
```

Like this: 

<img width="576" alt="image" src="https://user-images.githubusercontent.com/1119017/171724637-deb8cb25-d881-45f5-9199-fbea38e9d800.png">

That will help speed things along, because the PR that's "next up" to merged will be identified for us, and already deployed to the QA site.

# Merge Conflicts

Also, periodically, go through your PR queue (there's a link on each team's slack channel for convenience), and look at each PR for your team.  If you see this, then there are merge conflicts.

<img width="988" alt="image" src="https://user-images.githubusercontent.com/1119017/171724762-5b3c801b-7315-49d3-8239-57d998e5a04d.png">


If you can, fix them yourself.  If you can't then mark the PR with the "merge conflicts" label, and ping the person on your team that can fix them.

# Out of date branches

If you see this:

<img width="994" alt="image" src="https://user-images.githubusercontent.com/1119017/171724954-b2e17c17-003a-4468-982d-6446dd0c266c.png">

Then click to update the branch:

<img width="253" alt="image" src="https://user-images.githubusercontent.com/1119017/171724999-e2d9d075-ace0-41e3-974b-4bc2d600cb83.png">


All of this will help all of us get done with this final project (and the grading thereof) much more quickly!

</details>
  


<details>
<summary>
Notes about the final exam
</summary>
  
  
# Notes about the final exam
  
The final exam will be an online take home exam, and will be mainly high level questions about the process of software development that you learned in team01, team02, team03 and team04.

There may be questions about any of the following.  If you've been paying attention all along, you shouldn't really need to "cram".  The answers should be pretty much in your knowledge base already.

* Agile processes, e.g. standups, retrospectives, the role of a product owner/manager
* GitHub tools and their interaction with Agile processes: using feature branches, issues, Kanban board, Pull requests, code review
* General Web Development concepts, e.g.: Backend vs. Frontend
* Some Spring Boot specifics: controllers, services, use of Swagger
* Some React specifics: components, use of Storybook
* Testing in general: unit testing, test coverage, mutation testing
* Spring Boot Testing: Role of JUnit, Jacoco, Pitest, Mocking and Stubbing
* React Testing: role of jest, and Stryker
* Using third party APIs and representing data with JSON (as we did in team01, and later phases as well.)

I'll be asking questions about these topics that I think are the type you might be asked as a job interview.  So if you study, study the way you would for a job interview.

# Please do not collaborate on your exam answers.

* Identical text is unlikely to occur if each of you is working indepenently and writing in your own words.
* If you are copying/pasting text from an online source (e.g. to explain what a retrospective is) be sure that you use "quotation marks" around direct quotations, and **cite your source.**
  
  Otherwise, you are liable to end up triggering the suspicion of academic dishonesty because of the similarity of your text to someone else that happens to be
  using the same source.
  
  Also: relying too much on direct quotes rather than putting things in your own words may result in lower grades; if you have to quote others too much, 
  it suggests that you have not really internalized the content, but have to rely on others understanding.  So use direct quotes sparingly, if at all; try instead
  to answer in your own words.
  
 
Academic integrity investigations are unpleasant for everyone, and they don't help anyone learn. 

I really dont want to spend my time on those, so please don't create conditions where I have to do that.

Work independently, and let your learning speak for itself.

# Clarity and consiseness counts

* Small grammar / spelling errors may or may not be penalized; if an interviewer would be confused by the answer, or have some doubt as to your understanding,
  then they count.   If there is no doubt about your understanding, I'm liable to be more lenient.
* Make sure your answers are clear and understandable.
* Do not just do an information dump of everything you know about the topic, or everything you can possibly find online about the topic.  An employer wants someone to answer
* their question, and they also want someone that makes good use of their time.  Don't waste the interviewer's time.

</details>

<details>
<summary>
Notes about the final presentation
</summary>

# Notes about the final presentation

The final presentation should be a team effort, and should highlight all of the PRs that got merged into the main branch.

Limit your presentation to five minutes.

For full credit: 
* Make a video of between 5-8 minutes (see guidelines below) and submit the link on Gauchospace.
* If you don't have a video ready by the deadline, you may present live, but the presentation will have a 5% penalty applied (note that live demos also
  tend to be a bit more risky).

Highlight the work *from an end user perspective first*.

That is:
* The best thing is to show how an end user would use the feature
* The next best thing is to show either a front or backend component in isolation, for example:
  - If there is a front end component that is not active in the app yet, you can show it in Storybook
  - If there is a backend API, but the functionality isn't available in the user interface yet, you can demo it in Swagger.
* Show internals of code only after explaining the user facing functions, and even then, only if you have left over time.

  
# Instructions for your video:

Here's a tutorial [video on making demo videos from CS48 S20](https://youtu.be/k0Je8ASh4jo) (Video inception)

Based on the experience of CS48 students, **pre-recording is strongly recommended**.  You will *know for sure* in advance whether the
demo is successful, and whether or not you've hit the target length of 5-8 minutes.

Your video should be 5 to 8 minutes long, and cover these points:

* First, mention the names of the members of the team, and introduce the person narrating the video.  
  - It is ok if all the team members appear in the video.  It is also ok if only one person narrates the video on behalf of the team.
* Second, go through each of the features that your team worked on that were merged into `main`
  - Only demo the features that were merged into `main`
  - Focus in this part of the video on demoing the features from a *user perspective*, not on the technical details of how they were implemented.
* Next, if there is time remaining to reach the 5-10 minute mark, you may briefly cover any technical and/or non-technical challenges your team faced
  - You don't have to cover everything.  
  - You don't really even have to include this part if your demo already hits the 5-10 minute range.
  - If you do include this part, focus on the items that you think would be interesting to the audience (fellow students in CS156 F20, and the staff of CS156 F20). 
  - Possible items to include
    - Particularly interesting technical details of what you had to write in the code
    - Challenges in testing
    - Challenges in team communication and organization, and what you did to overcome those
* Optional: at the end, if you like, you may thank anyone that was particularly helpful to the team from the staff (TAs and LAs, or students from other teams). 
  - Please don't include thanks to me (Prof. Conrad) in the video; I don't want this to be an exercise in brown-nosing.
  - If you do want to express gratitude, feel free to share your thoughts with me on the Slack, by email, etc.  

Please then also poll your team members and let me know your thoughts about the privacy of your final demo video:
* public, available to anyone that is interested in the app and the course
* unlisted, but ok to make it available to future CMPSC 156 students (as an example, and to orient them to the app and the course)
* unlisted, and only shown once for this team's final demo, and to course staff 

</details>
