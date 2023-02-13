This assignment is `jpa00`, i.e "Java Programming Assignment 00".

If you find typos or problems with the lab instructions, please report these via email.


# Goals

This lab checks that you can succesfully edit, compile, run and submit a simple
`Hello.java` to Gradescope for grading.



# This lab requires Java 17.

# How to install Java 17 and Maven on your own machine

Note: these instructions were current as of S22.   Things change every quarter&mdash;sometimes even from day to day&mdash;and the only way we find out is when students try things and tell us.  (We don't have the bandwidth to try all of the instructions on every possible OS version combination.)

* For MacOS, this is fairly straightfoward; see instructions [here](https://github.com/awhicks/CS-3704-S23/blob/main/_info/software.md).
* For Windows, we recommend installing the Windows Subsystem for Linux (WSL), and then following the instructions for installation of Java 17 from [this page](https://github.com/awhicks/CS-3704-S23/blob/main/_info/software.md). 
* For Linux, there are instructions on  [this page](https://github.com/awhicks/CS-3704-S23/blob/main/_info/software.md) that apply to Debian/Ubuntu like systems.  If those don't work for you, ask the staff for help.
 

# Do I really need Java 17?  

You may be wondering whether it's ok if you have Java 19 or Java 18, or Java 11, or some other version of Java instead of Java 17.    This short answer is: for this simple `Hello` lab, it probably won't make a difference, but eventually it probably *will*.  So if you are going to the trouble of installing Java on your system, try to make sure it's Java 17, *specifically*, which (unlike Java 12, 13, 14, 15, 18 or 19) is considered a *Long-Term Support* release of Java.

Read more here if you are interested: [https://ucsb-cs156.github.io/topics/java_versions/](https://ucsb-cs156.github.io/topics/java/java_versions.html)  

# Something for everyone to learn

Note that even if you have done Java programming before, **there
may be a few things about this `Hello.java` program that may be
unfamiliar to you**.  These have to do with setting us up for real world
programming practices used in large software projects.

* Rather than compiling with command line tools such as `javac` and running
  the program with the `java` command, we'll be using a package and build
  manager called *Maven*.  For a small `Hello World` type program,
  this will seem like overkill; but it will set us up for being able to
  manage much larger projects.
* We are setting our code up in a GitHub repo right from the start.
* We are going to be following the directory conventions required
  by Maven.  So it's important to have the correct directory structure
  within the GitHub repo.

There a few details, but they are all straightforward.  It shouldn't take
very long, and if it goes well, you'll be able to start on the next lab
right away.

That one may actually take quite a bit more work.


Step 0: Getting oriented
========================

1. Ideally, you will already 
   know the following things from previous courses (CS 2114 3114).  It is possible that if you are joining VT for the first time in this course, some of this may be unfamiliar to you.   The rest of these instructions will assume you know how to do the items in the list below. If not, then let a member of the course staff know, and we'll point you to resources where you can come up to speed.

   -  knowing how to use a **basic
      text editor such as emacs or vim** to edit files.  (Here, for example, is some [basic instruction on vim](https://ucsb-cs156.github.io/topics/vim)
   -  knowing basic Unix/Linux
      commands to create directories, change directory, manipulate files, i.e. commands such as: `mkdir`, `cd`, `pwd`, `mv`, `rm`, `ls`.
   If those topics are new to you, please reach out to the instructor to let them know, and ask for pointers to resources where you can
   study up on these skills.
   
2. We strongly encourage the use of VSCode as an editor this course.   For this assignment, it will not matter what editor you use, 
   but in future assignments, the use of an IDE will become more important.  We'll discuss this more in lecture.

# The rest of the lab: Step-by-Step

## Step 1: Configure your machine for Java 17

* You should check that you have Java 17 and Maven by following the steps here: <https://ucsb-cs156.github.io/f22/info/software/>

## Step 2: Get setup with github and add yourself to our organization

We will be using github.com in this course. We have created an
organization called [CS-3704-spring-2023](https://classroom.github.com/classrooms/122842685-cs-3704-spring-2023) on github.com where you can
create repositories (repos) for your assignments in this course.

The advantage of creating private repos under this organization is
that the course staff (your instructors and TAs) will be able to see
your code and provide you with help, without you having to do anything
special.

To join this organization, you need to do three things.

1. If you don't already have a github.com account, create one on the
"free" plan. Visit [https://github.com/](https://github.com/)

2. If you don't already have your `@vt.edu` email address
associated with your github.com account. go to "settings", add that
email, and confirm that email address. 

3. Fill out the form [here](https://forms.gle/RmxBxcot56AipiD5A) that will automatically send you an invitation to join the course organization on github.

4. You can also go straight to [CS-3704-spring-2023](https://classroom.github.com/classrooms/122842685-cs-3704-spring-2023) and see the invitation there (if you're logged in). Accept the invitation that appears in your browser (from step 3) or log into your account on [https://github.com/](https://github.com/) to accept the invitation.

## Step 3: Get setup with gradescope

We will use gradescope to grade all your homeworks, exams and lab/programming assignments. I have manually added everyone (using your @vt.edu accounts) currently enrolled in the course to the Gradescope system. You should have received an email notification with instructions about logging into gradescope. Once you follow the instructions to set your password, you should have access to our course on Gradescope. 

## Step 4: Configure your machine for git/GitHub

You need to configure the environment you are working in for access to git/GitHub.

We want to be able to use `git` and GitHub with ssh links, so we need to set up public-key/private-key pairs.

We also want to set up `git` so that it records our commits properly.

1. `git` configuration: [Detailed Instructions](https://ucsb-cs156.github.io/topics/CSIL/csil_git_configuration.html)

    
2.  Configure ssh keys for git
    - Detailed instructions: [Configuring your ssh key for Github.com](https://ucsb-cs156.github.io/topics/GitHub/github_ssh_keys.html)


3.  If you are brand new to git and github, review a few basic facts about git and github.com 
    - <https://ucsb-cs156.github.io/topics/git/git_overview.html>


## Step 6: Finding your jpa00 repo on GitHub

Open a web browser and login to GitHub, then navigate to the [assignment invite link](https://classroom.github.com/a/YvXchMhy).

You should see that there is a private repo in this organization called `jpa00-yourGithubId`, where `yourGithubId` is replaced with your GitHub id.  This is the repo that you'll be using for this assignment.

This is currently an skeleton repo.  In the next step, we'll clone this repo into a directory on your local system.

## Step 7: Cloning the repo


1. Create a directory somewhere on your machine for cs3704, and cd into that.
   
   ```
   mkdir ~/cs3704
   cd ~/cs3704
   ```

   You can actually use any directory you like, but for consistency, we'll refer
   to `~/cs3704` throughout the rest of
   the instructions.

2. Now, go to the `github.com` web page, and find your `jpa00-userid` repo. The page should look something like this:

   ![jpa00-cgaucho-50.png](jpa00-cgaucho-50.png)

   You should see a button for `SSH`;
   select that button.  Then there is a button to copy the URL shown;
   click that to copy the URL.

3. Now type this command, replacing
   `url` with the url that you copied.

   That `url` should be something like
   <tt>git@github.com:cs-3704-spring-2023Environmment-setup-awh4kc.git</tt> but with your GitHub id in place of <tt>awh4kc</tt>.

   ```
   git clone url
   ```
   
   <tt>Cloning into Environment-Setup-awh4kc...</tt>
   
  
4. If you use the `ls` command, you should now have a subdirectory called <tt>{{page.num}}-cgaucho</tt> (except <tt>cgaucho</tt> will be your GitHub username.)  Use
   a `cd` command to change directory 
   into that directory, e.g.

   
   <tt>cd Environment-Setup-awh4kc</tt>
   

## Step 8: Check out the starter code.

Now lets take a look at what is in our repo:

You should see that the `README.md` for this repo has an explanation of the contents of the starter code.  Read though this explanation to learn more about:
* Maven
* the `pom.xml`
* the required directory structure

## Step 9: Compile and run the Starter code

To compile the starter code, return to a shell prompt in the directory where your cloned your repo.  You should see, when you type `ls`, that 
the file `pom.xml` is in the current directory.  For best results, you should always run Maven from this directory.

To compile type `mvn compile`.   

* If you see the message `The JAVA_HOME environment variable is not defined correctly...` plus a few more lines of output, see [this link](https://ucsb-cs156.github.io/topics/maven/maven_faq.html) for a fix. 
* Otherwise, you should see no error messages
* There may be warning about missing `resources` and `UTF-8 encoding`, but you can safely ignore those for now.  If you are curious, see the the section "Warnings you May be able to Ignore" on [this page](https://ucsb-cs156.github.io/topics/maven/maven_hello_world.html).

Then, type `mvn package`.  You should see a lot of output, but somewhere in that output, something like this:

```
 [INFO] Building jar: target/hello-1.0.0.jar
```

That indicates that you have built a `.jar` (or Java Archive) file.  This file is a compressed archive of all of the compiled Java code from your program.  You can run it with this command:

```
java -cp target/hello-1.0.0.jar edu.vt.gradescope.Hello
```

You should see output like this:

```
% java -cp target/hello-1.0.0.jar edu.vt.gradescope.Hello
This is the wrong output!
% 
```

The line `This is the wrong output!` is being produced by the line of code:

```
        System.out.println("This is the wrong output!");
```

You should eventually change this line to produce the correct output.
But, don't do that just yet.  Let's first see what happens when you submit a program with errors in it to Gradescope.



## Step 10: Submit incorrect Java code to Gradescope

In this step, we'll see what happens when you submit two incorrect program to Gradescope.  We aren't grading this step, so you *could* skip it, but we strongly encourage you to do it anyway, because it's important to be able to understand how the autograders work on a simple case before dealing with a more complex case.


First, we'll submit the starter code "as is" to Gradescope.  Gradescope will be expecting a program that produces, as it's output `Hello, World!` (followed by a newline).

Instead, your code currently produces: `This is the wrong output!` followed by a newline. 

We want to see what the Gradescope output looks like in that case.

To submit to Gradescope, navigate to:
<https://gradescope.com>.   

You should have an account invitation in your email.  If you don't, ask an instructor, TA or mentor for assistance.

To submit your work, you should be able to click on the GitHub link in Gradescope, and locate your repo.  The first time you do this, it may take a while; be patient before giving up.   If it still doesn't work after a while, you can ask the staff for assistance.


After you submit, it will take some time for Gradescope to process your submission.  Once it's processsed, you should see output similar to this:


![Gradescope output from starter code](jpa00-gs-starter-code-50.png)

The most important part is this:

```
FAILED:
expected:<[Hello, World]!
> but was:<[This is the wrong output]!
>
```

Note that it tells you exactly what was different between the expected and actual output (the part in `[]`).  The `!` is the same in both parts, so it is outside the `[]`.


Once you've understood this output,
let's move on and see what happens when you submit code with a syntax error.

Go into the file `src/main/java/Hello.java`, and remove the semicolon at the end of the statement:

```
 System.out.println("This is the wrong output!");
 ```
 
 So that it reads:

 ```
  System.out.println("This is the wrong output!")
 ```

This, of course, has a syntax error.

Try using `mvn compile` and see what happens when you submit this.

Then, commit this change to Github.

(Normally, we would NOT push code that has a syntax error, but for purposes of this experiment, we will.)

Add/Commit/Push with these commands:

```
git add src/main/java/Hello.java
git commit -m "commit code with syntax error to test autograder"
git push origin main
```

Now, submit to Gradescope again.  You should see output like this:

* At the right hand side, you'll see the following:

  ![mvn-compile-failed-50.png](mvn-compile-failed-50.png)

  This is how you'll know that the Maven compile failed on Gradescope.

  But where can you see what went wrong?  Read on:
  
  
* Look in the main window, for
  output with `mvn compile failed` at the top.  It will probably be very
  long (the whole output is not shown):

  ![mvn-compile-failed-top-50.png](mvn-compile-failed-top-50.png)

  This output is really long because it shows every single file that was
  downloaded by Maven in order to do it's work (which is quite a few).  However,
  the really useful output is at the bottom, so you have to scroll down a while:

* Look at the bottom of this section, and eventually you should see:

  ![mvn-compile-failed-bottom-50.png](mvn-compile-failed-bottom-50.png)

  Here, finally, you can see what's wrong with the compile (the missing semicolon).

Now that you understand what a failed compile looks like, let's finally fix the code
and finish the lab.

## Step 11: Submit correct Java code to Gradescope

Now, fix the code so that it produces the correct output.  Change the file `src/main/java/Hello.java` so that the `System.out.println` method call reads:

```
        System.out.println("Hello, World!");
```

Test this locally by compiling and running the code:

```
mvn compile
mvn package
java -cp target/hello-1.0.0.jar edu.vt.gradescope.Hello
```

You should see the correct output, `Hello, World!`.

Now, commit this change:

```
git add src/main/java/Hello.java
git commit -m "correct the output"
git push origin main
```

Then submit to Gradescope again.

Once you see that you have a score of 100 for Environment Setup on Gradescope, you are *done* with Environment Setup.

