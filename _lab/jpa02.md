---
desc: Spring Boot and Heroku Hello World
assigned: 2022-10-04 19:00
due: 2022-10-12 23:59
github_org: ucsb-cs156-f22
layout: lab
num: jpa02
ready: true
starter: https://github.com/ucsb-cs156-f22/STARTER-jpa02
---

{% include drop_down_style.html %}

# Individual lab, but you may help one another

This is an **individual** lab on the topic of Java web apps on Heroku.

You may cooperate with one or more pair partners from your team to help in debugging and understanding the lab, but each person should complete the lab separately for themselves.

# Ask for help on `#help-jpa02` 

There should be a slack channel called  `#help-jpa02`  where you can ask questions about this assignment.  Check that channel first to see if your question has already been answered. 

# Step 1: Understanding what we are trying to do

### What are we trying to accomplish again in this lab?

-   In this lab, we will <em>create a basic "Hello, World" type web app in Java"</em>
-   A web app is a piece of Java code that takes HTTP request messages as input, and responds with HTTP response objects as output.
-   Heroku is a platform where we can host a Java web app.

### Why use Heroku?

-   Web applications run on the "server" side of the web architecture, not the client side.
-   So to test a web application, we need to set up a web server that can run Java code.
-   Configuring a web server for Java is challenging. But, fortunately, we don't have to.
-   Heroku.com offers "platform as a service" cloud computing for Java web applications.
-   We'll use the "free plan" that they offer for folks just getting started with learning Heroku.
-   This puts your application "on the web", for real, so that anyone in the world can access it 24/7


### The Free Plan is Going Away

Note: CMPSC 56/156 has relied on the free plan of Heroku for at least six years now.  However, the free plan is going away on **November 28, 2022**, which is before the end of this course.  We found this out very late in Summer 2022--otherwise would have spent part of the summer redesigning the course for a different platform. 

As it is, we'll have to figure that out on the fly, but for now, we think the free plan is still in place, so we'll move ahead with using it, even while we are looking for alternatives.

There is some talk of a Heroku "student plan", but it's not yet clear what that will look like, whether that will meet the course's needs, and when or if that will be rolling out.  So for now, we just have to plan on not relying on Heroku anymore at all.

### Limitations of the free plan of Heroku

TL;DR: You should NOT need to enter a credit card into Heroku.  If you are asked for one, something has gone wrong.

-   If no-one has accessed your web app for a while, it "goes to sleep", so to speak.
    -   The first time someone tries to access it after it has gone to sleep, there is a <em>noticable</em> delay in the response, perhaps several seconds or even up to a minute.
-   If too many people try to access your service per hour, eventually, you'll run out of "free resources".
    -   That is <em>very unlikely to happen</em> unless you make a web app that somehow attracts the attention of a very large audience.
    -   I suggest you try to avoid doing that with the web apps you develop for this class.
    -   I suggest you avoid doing that in general, unless/until you have some plan for how to make money off your web app to pay for the server resources. (With a credit card, you can set up Heroku to have higher usage limits, and to keep your app running so that response time is fast. But you should NOT need that for this course.)


### Web Apps vs. Static Web Pages

You may already have some experience with creating static web pages, and/or with creating web applications (e.g. using PHP, Python (Django or Flask) or Ruby on Rails.) If so, then the "Learn More" section will be basic review.

If you are new to writing software for the web, you are <em>strongly encouaged</em> to read the background information at the "learn more" link below.
-   [Web Pages vs. Web Apps](https://ucsb-cs156.github.io/topics/webapps_webapps_vs_websites/)

### What are we trying to accomplish again in this lab?

If you just did a deep dive into the article [Web Pages vs. Web Apps](https://ucsb-cs156.github.io/topics/webapps_webapps_vs_websites/) it may be helpful to again review what we are trying to accomplish in this lab:

-   In this lab, we will <em>create a basic "Hello, World" type web app in Java"</em>
-   To test that, we need to run that on a server somewhere.
-   Configuring a web server for Java is challenging. But, fortunately, we don't have to.
-   Heroku.com offers "platform as a service" cloud computing for Java web applications.
    -   We'll use the "free plan" that they offer for folks just getting started with learning Heroku.
    -   This puts your application "on the web", for real, so that anyone in the world can access it 24/7

### Disk Quota

IMPORTANT: if you are working on CSIL, and at some point things just "stop working":

-   You get odd error messages, especially "cannot write file", or "disk quota exceeded"
-   You cannot log in---it takes your user name and password on the machines in Phelps 3525 or CSIL, but then just logs you out immediately.

Then you probably have a disk quota problem.

-   The best way to troubleshoot this, if you cannot log in, is to ask someone else that CAN log in to allow you to use a terminal window on their screen.
    -   Use `ssh yourusername@csil.cs.ucsb.edu` to get into your account from their terminal session.
-   For troubleshooting tips, visit: [CSIL Disk Quota Troubleshooting](https://ucsb-cs156.github.io/topics/csil_disk_quota/)

# Step 2: Create a Heroku Account

If you do not already have a Heroku account, navigate to <https://www.heroku.com/> and click the "Sign up for Free" link.

You'll be asked for:

-   First Name
-   Last Name
-   Email (you may use any email address you like)
-   Company (you may leave this blank).
-   Preferred Development Language: We suggest you select "Java" if you are currently enrolled in CMPSC 156
    -   (Don't worry; this doesn't prevent you from using the account with other languages later.)

## Step 2a: Set up Multi-Factor Authentication for Heroku

On February 1, 2022, Heroku will start requiring every user to enable Multi-Factor Authentication. This adds an additional layer of security to your account by requiring access to something physical (like a phone or a physical security key) to complete a login along with your password.

You should already be familiar with multi-factor authentication as [we use Duo here at UCSB](https://www.it.ucsb.edu/mfa). 

**You can set up multi-factor authentication [here](https://id.heroku.com/vaas/manage).** You can also get to this page by logging into [Heroku Dashboard](https://dashboard.heroku.com/), clicking on your profile picture, then "Account Settings", and then "Manage Multi-Factor Authentication".

The easiest method to set up is the "One-Time Password Generator". Clicking on the "Add" button within this option will present you with a QR code that you can scan using an authenticator app. 

* If you are using the Duo app, click "Add" on the main screen, followed by "Use QR code", to scan the code. Be sure to name the code with "Heroku" so you know which service this code belongs to.

Finish setup by entering the code from your authenticator app into Heroku's website.

In addition to using one-time passwords (OTPs), you can use on-device biometric sensors (such as Windows Hello, Touch ID, and Face ID) via the "Built-in Authenticators" option, or a physical U2F security key.

**Note that this new requirement breaks the ability to login to Heroku by typing your credentials directly into Heroku CLI.** Heroku CLI logins (i.e. `heroku login`) must now be completed via the browser login flow. If you are logging in from a device without a browser (such as an SSH session into CSIL), you will have to manually paste the link generated in the CLI into a web browser to complete the login.

More info on this change can be found [here](https://devcenter.heroku.com/articles/multi-factor-authentication).

# Step 3: Create your repo

You should already have a repo under the course organization 
<tt>{{page.github_org}}</tt> called 
<tt>{{page.num}}-<i>githubid</i></tt>
created for you by the staff, where <tt><i>github</i></tt> 
is your github id.

If not, create one for yourself following that naming convention;
it should initially be private, and empty (no `README`, license or
`.gitignore`.)

Clone that repo somewhere and cd into it.

Then add this remote:

<tt>git remote add starter {{page.starter}}</tt>

Then do:

```
git checkout -b main
git pull starter main
git push origin main
```

# Step 4: Start your webapp on `localhost`

The application should be ready to go out of the box; it
starts up a web server that brings up a page with the message
`Greetings from Spring Boot!`

We are going to run a command
to start up this web server
and then try to connect with
a browser.

* First, use `mvn compile` to make sure that the code compiles.

  * If you get the error on CSIL about `JAVA_HOME` not being defined
    correctly, you may need this command:
    ```
    export JAVA_HOME=/usr/lib/jvm/java-17-openjdk
    ```
* Next, try `mvn test` to be sure that the test cases pass.
* Then, try `mvn spring-boot:run`.  This should start up a web
  server on port 8080 running on `localhost`

  The `mvn spring-boot:run` command is a shortcut that is provided for us to be able to run the jar file.  It does pretty much the same thing as 
  if we ran the `.jar` file and specified the class containing our `main` on the command line.

## Connecting with a browser

Now, if you are running on your own machine, connecting with a browser is quite simple;
the web server is running on the local machine (`localhost`) on port
8080, so putting the address <http://localhost:8080> in your browser
will just work.  If you are successful, you should see the message `Greetings from Spring Boot` appear in your browser.

It's the case where you are running on CSIL where things can get more
complicated.  

First, there's the possibility that port 8080 may already be taken;
in that case you'll see the error:

```
Web server failed to start. Port 8080 was already in use.
```

<details>
<summary>
To see how to fix the `Port 8080 was already in use` error, click the triangle:
</summary>

In this case, the fix is to choose another port number.  Any number between `8080` and `65535` is fair game; to try another port number, use the command shown below (change `12345` to whatever port number you like):

```
PORT=12345 mvn spring-boot:run
```

You'll need to substitute this number (e.g. `12345`) in place of `8080`
when trying to load the website.

</details>


<details>
<summary>
To see strategies for bringing up a web page for a web server running on CSIL, click the triangle.
</summary>

## Strategy 1: Point browser directly at CSIL machine

If you are running on CSIL, you can try to point your web browser *at the machine* where the server is running instead of `localhost`.

For example, if you are running on CSIL and type in `hostname`, and 
see this:

```
[pconrad@csilvm-01 ~]$ hostname
csilvm-01.cs.ucsb.edu
[pconrad@csilvm-01 ~]$ 
``` 
  
Then substitute that name in place of `localhost`, e.g. point your browser as <http://csilvm-01.cs.ucsb.edu:8080> instead of <http://localhost:8080>

This may not always work, because firewalls may prevent access.  Using
the [UCSB VPN](https://www.it.ucsb.edu/pulse-secure-campus-vpn/get-connected-vpn) may help.

## Strategy 2: Port Forwarding

If you are using `ssh` to connect to CSIL, the solution shown here
allows you to forward traffic on `localhost:8080` on your own machine
to `localhost:8080` on the machine you are connecting to:

* <https://ucsb-cs156.github.io/topics/csil_ssh_port_forwarding/>

## Strategy 3: Remote Desktop 

Using the Remote Desktop (RDP) Solution described in the articles below, you can load a complete "desktop" of a CSIL Linux environment and show it in a window on your Mac or Windows machine.  

* Windows Instructions: <https://doc.engr.ucsb.edu/pages/viewpage.action?pageId=31785118>
* Mac Instructions: <https://doc.engr.ucsb.edu/display/EPK/CS+Lab+RDP+Access+-+MacOS+Client>

In the RDP window, you can open both a terminal window and a browser that are both
running on CSIL.  Since that browser is running on the same system as
the web server, you can just use <http://localhost:8080> to connect
to the server.

</details>

## About `localhost` and "Port Numbers"

The code in this repo is configured to start up a webserver on port 8080, running on `localhost`, which is a name for the machine on which the code is running.  

* If you are running the code on a CSIL machine, then `localhost` refers
  to that machine.  
* If you are running on your own machine, then `locahost` refers to that
  machine.
* The port number is a more specific "communications channel" on that machine.   You can find more information on port numbers
  at this short article, which you are encouraged to read if you are not already familiar with port numbers
  (or, for that matter, even if you are): <https://ucsb-cs156.github.io/topics/port_numbers/>
  
So the web address to acccess your server is: `http://localhost:8080`.

* Note: You should use `http` not `https` when running on `localhost`. Using `http` is the unsecure, unencrypted version.   
* It is possible to set up Spring Boot to run `https` (the secure, encrypted version), but it's complicated and typically
  unnecessary; Heroku sets up `https` for us automatically, so we really don't need to deal with those steps most of the time.

# Step 5: Understanding `localhost` vs. Heroku

When running on `localhost`:
* The web app is only runnning as long as your program is executing. 
* As soon as you CTRL/C the program to interrupt it, the web app is no longer available.
* The web app is only available on the machine where you are running the program; not on the public internet.

Running on `localhost` is fine for testing and development.  But eventually we want to know how to deploy a web application so that anyone on the internet can access it.

To get the web app running on the public internet, we'll need to use a cloud-computing platform such as Heroku.
Heroku allows us to deploy web applications in Java rather easily. 

*A side note*: though we won't explore it in this course, Heroku also makes it easy to deploy webapps in *a variety of langauges*, including Python, Node (JavaScript), and Ruby just to name a few.   Many of the skills you'll learn in this course about Heroku will transfer to those other languages if you want to work with them in other courses such as CMPSC 48, CMPSC 189A/B, or personal projects.)

*A note about security*: Let's say up front that this is a risky thing to do.   You need to be very careful about security when deploying web applications to the public internet.  Fortunately, this particular application is rather simple and low-risk.   We'll discuss web security throughout the course.

# Step 6: Create a new Heroku App using the Heroku CLI

In this step, we'll deploy our Spring Boot application to the public internet using Heroku.

Use this command to login to Heroku at the command line:

```
heroku login
```

Then, use this command to create a new web app running on heroku.  Substitute in your UCSBNetId (i.e. your ucsb email *without* the `@ucsb.edu` part. 

That is, if your email is <tt>cgaucho@ucsb.edu</tt>, please make your heroku application name
<tt>{{page.num}}-cgaucho</tt>.  This name is important, because the Gradescope autograder willbe looking for a Heroku application that matches this naming convention.  If there is a reason that you cannot use this naming convention (e.g. your ucsbNetId is not accepted as part of a 
heroku application name because of special characters, upper case characters, etc.), please note this on the `#help-jpa02` channel on Slack.

Note that you should convert your ucsbnetid to all lowercase; heroku web-app names do not permit uppercase letters, and use `-` in place of underscores or periods.

<tt>heroku create {{page.num}}-<i>ucsbnetid</i></tt>

Notes:
* A reminder that this is an individual lab, 
  so you should complete it for yourself, i.e. there is only one github id in the name, not a pair of github ids.   
* Please do not literally put the letters <tt><i>githubid</i></tt> 
  in your app name; you are meant to substitute your own github id there.
* If Heroku indicates that the name is too long, you may truncate any
  part of it.   

# Step 7: Login to the Heroku Dashboard

Login to <https://dashboard.heroku.com/apps> and look for the <tt>jpa02-cgaucho</tt> app (or whatever your name is) that you created.

You should find a place where you can connect your App to Github.  

Click on this, and select your repo to connect the Github Repo to Heroku.

Then, click on "deploy branch".


# What if it doesn't work?

If it doesn't work, try these things before asking a mentor, TA, or instructor for help.

1. Make sure you are logged into Heroku at CLI with `heroku login`.  If you are working on CSIL, exited your CSIL shell (logged out), and logged back in again, you have to login to Heroku again.  Then repeat the commands.
3. Try `heroku logs --app appname` (substitute the name of your app where you see `appname`).  You'll see the log output of that app on Heroku.   
   * You may find it helpful to open a second Terminal, login to CSIL and the Heroku CLI, and use `heroku logs --app appname --tail`, which keeps the log output running continously.
   * You can also see your logs in a web browser at: <https://dashboard.heroku.com/apps/app-name/logs> (note that you need to put your `app-name` in the URL instead of `app-name`.  
   * You can navigate to this from <https://dashboard.heroku.com/> by selecting your app, clicking on it,  selecting the `More` menu at upper right, and the selecting `Logs`.

# Step 8: Changing what is shown on the page

Go into the Java source code under `src` and locate the file `/src/main/java/edu/ucsb/cs156/spring/hello/HelloController.java` 

In this file, locate the line of code that says:

```java
    @RequestMapping("/")
    public String index() {
        return "Greetings from Spring Boot!";
    }
```

This method returns the contents of the home page (`"/"`) for the webapp.

Change that code by changing "Spring Boot" to your email address (without the `@ucsb.edu` part).

For example, if your email is `cgaucho@ucsb.edu`, instead of:

```java
        return "Greetings from Spring Boot!";
```

You'll have:

```java
        return "Greetings from cgaucho!";
```

<details>
<summary>
If your email contains upper-case letters, underscore (`_`) or periods (`.`) click the triangle for special instructions:
</summary>
    

Update: The autograder has been modified to handle the cases of:
* mixed case (upper and lowercase letters) in email addresses
* underscores `_` in email addresses
* periods `.` in email addresses

In order to convert each of these to legal Heroku app names, the autograder converts your email by:
* stripping off the @ and everything after the @
* converting to all lowercase
* converting `_` and `.` to `-`
Examples:
* `Foo.Bar@ucsb.edu` becomes `foo-bar`
* `My-Lit.tle_pony@umail.ucsb.edu`  becomes `my-lit-tle-pony`    
    
So, if your email address is `My-Lit.tle_pony@umail.ucsb.edu`, you should modify your code to replace:
```java
        return "Greetings from Spring Boot!";
```

with
```java
        return "Greetings from my-lit-tle-pony!";
```

If your email presents any other corner cases that are handled above, make a post on `#help-jpa02` on slack to ask for help.

</details>

Then:
* use `mvn compile` to make sure your code still compiles
* (optional, but suggested in case you need to debug)
   * use `mvn spring-boot:run` to test locally, perhaps with `curl http://localhost:8080`
* Use git add, git commit, and git push to push your changes to github.
* Visit the Heroku Dashboard, go to the `Deploy` tab, and scroll down to `Manual Deploys`.
  Select the `main` branch and click `Deploy Branch` to deploy your branch to the web.
  
  As before, wait until the script says that your branch is successfully deployed
  (or, if there are errors, read the error message in the log and address the errors.)
  
If it works, then the words "this github repo" should become clickable links.  
* The words "this github repo" should link to your github repo

Ok, so far, we haven't really done anything we couldn't have done with a static web page.  But we have gotten a working Java web app running on Heroku, so it's start we can build on.  


# Step 9: The test cases

You'll see that when you run "mvn test" that there are test cases, some of which are now failing.

The test cases are in these files:
* `src/test/java/hello/HelloControllerTest.java` (Unit Test)

Run the tests and see them fail.

Then modify them so that they pass.   Note that we are doing TDD "wrong" this time; to do it "the right way",  we should have modified the tests first, and then modified the code so that the tests pass.   We'll pivot to this style of working once we have a better grasp on all the moving parts here.

# Step 10: Adding links to repo in the README.md

Edit your README.md.  You'll find some TODO items inside indicating what edits you need to make.

All quarter long, we want you to develop the habit of adjusting the 
README.md in your repo to include a link to your repo.

The link to your repo may seem redundant, but it helps your mentors, TAs and instructors; when you submit your work for grading to either Gradescope or Gauchospace, having those links handy really helps us navigate through your assignments quickly to evaluate them and assign grades.

# Step 11: Submitting your work for grading

When you have a running web app, make a submission under jpa02 on Gradescope.


