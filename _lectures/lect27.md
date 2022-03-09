---
num: "Lecture 27"
lecture_date: 2022-03-09
desc: "Wed Lecture: Continue work on team04"
ready: true
---

# Notes about the final

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
