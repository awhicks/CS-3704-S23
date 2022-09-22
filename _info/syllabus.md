---
title: "Syllabus, CMPSC 156, Fall 2022"
layout: handout
ready: true
---


Basic Facts
-----------

* **Instructor**:  [Phill Conrad](http://www.cs.ucsb.edu/~pconrad) (contact via Slack)
   * Use the "instructor messsage" feature to contact Prof. Conrad, as well as all TAs, Readers and Mentors
* **Lecture**:
   * Tue/Thu 5pm-6:15pm 
   * You are expected to participate synchronously.  The mode of instruction is "in-person".
   * While there will be *some* lecture material (recorded and made available asynchronously over Zoom), in most class meetings there will be some 
     activities that are done in teams during the class meeting time.  There is no meaningful way these activities can be
     "recorded", done asynchronously, or "made up" after the fact, since the skills we are teaching and learning are *team* skills.   
* **TAs**: {{site.ta_list_full}} (contact via Slack)
* **Lab** (50 minute discussion section)
  * Wednesday {{site.discussion_section_times}}
  * Attendance/Participation is expected/required.
  * You must participate the section for which you are registered, since teams are assigned by section.
* Office Hours: See: [http://www.cs.ucsb.edu/~pconrad/ofchrs](https://ucsb-cs156.github.io/f22/info/office_hours/)

Course website: <https://ucsb-cs156.github.io/f22/>

About the Course
----------------

-   Our goal is to learn how Advanced Application Development works.
-   We will learn some aspects of Java and JavaScript--but not just to learn Java and JavaScript for the sake of learning another language.
-   Our bigger goals are:
    -   to practice using APIs and frameworks to get stuff done--a very relevant real world job skill!
    -   to learn how to learn a new language or technology--something you'll do a lot in your career
    -   to learn some professional-level, real-world programming practices.

The way I'm planning to teach the course is a bit different from what
you may have experienced before--I'm trying to create a learning
environment that *mirrors how real world software is developed* more
than is the case is traditionally structured courses.

So, the emphasis will be on:

-   open source, and sharing code, not keeping code secret
-   collaboration
-   writing code, that, where possible is actually useful and usable.

Note that "sharing code" doesn't mean "stealing code". We still don't
take credit for other people's work---academic honesty still
applies. It just 'looks different' in this course.


Final Course Grades
===================

Your grade will be made up of activities from the following categories:

* Participation Grades (10%) - Each participation grade will be out of 100 points.  
  
  Particpation grades may vary: some are individual, some are team, and some may be a combination of the two that adds up to 100.
  
  The lowest three participation grades will be dropped; accordingly, if you need to miss a lecture every now and then because of illness,
  internet problems, etc., it shouldn't affect your grade unless it becomes a persistent problem (in which case you should speak to the instructor as soon as possible about your situation.)
  
* Homeworks / Quizzes (20 %) - These will be administered through Gradescope.  
  Some questions will be graded by hand (e.g. short answer/essay type questions), while others might be autograded
  (e.g. multiple choice, fill in the blank, true/false questions.)  These will typically be based on assigned readings.
  We will drop only the lowest two grades from this category.
  
* PAs (Auto-Graded Programming assignments) (20 %) - jpa00 is an example of these programming assignments.  None of these will be dropped; you are
  responsible for all of them.   This may include individual assignments (such as jpa00), pair assignments, and/or team assignments.

* Exams (25 %) - If conditions permit, we will have two in-person written exams; a midterm and an final. There are two contingencies in case conditions change:
  - The instructor may substitute a "take-home" exam for either of the in-person exams.
  - If only one exam is offered, it will be worth 25% of your grade.
  - If is not possible to hold any exams, these points will be distributed instead among the other course components. 

* Project Grade:  (25%) - Your project grade will be based on your contributions during the Project phase of the course.   

  The project grade is divided into two parts:
  * One component of the project grade is based on your team's productivity, i.e. the extent to which your team
    makes substantial contributions to the open source project to which you are assigned.   Your team earns points towards a total of 
    100 points for this grade item each time a "pull request" is merged by course staff into the `main` branch of the GitHub repository of
    code for that project.    The number of points earned will vary depending on the challenge represented by the code change.
    
  * Other components of your project grade may be based on an assessment of your performance on various quality metrics related to your team's
    *professional skills* related to software development.  

    Your grade here may be a team based grade, an individual grade, or a combination
    of these.  Examples of these include, but are not limited to:
    - The quality of commit messages (inspected by spot checking)
    - The quality of descriptions on pull requests and issues
    - The extent to which you and your team keep your Kanban board up-to-date 
    - Your team's presentations to the course.

  In addition, we'll be using peer evaluations through a tool called CATME to assess your individual contributions to the project's success.
  The peer evaluation may apply a multiplier to your project grade, increasing it or decreasing it, per your team's assessment 
  of your contributions.   It is important to be sure that you are meeting your committments to your team for a variety of reasons; your
  grade is among those.

We will compute an overall average for your score in the course, based on the weights above, plus extra credit.

* Then, a standard 10 point scale will be applied to your overall grade, plus *each* of the four components of your grade 
  (Participation, Homeworks/Quizzes, PAs, and Project), with the upper and lower ends of each range as +/- grades, 
  except for A+ grades, see below.  There is no "rounding up"; a grade of 86.9999 is a B and a grade of 87.0000 is a B+.

  This gives us six grade components: the original five, plus your overall average.
  
Finally:

* To earn a grade of A, you must an A average overall, and in *each* of the five components.
* To earn a grade of A-, you must have at least an A- average overall, and at least a B- average in each of the components.
* To earn a grade of B+, you must have at least an B+ average overall, and at least a C+ average in each of the components.
* To earn a grade of B, you must have at least an B+ average overall, and at least a C average in each of the components.
* To earn a grade of B-, you must have at least an B- average overall,  and at least a C- average in each of the components.
* * To earn a grade of C+, you must have at least an B- average overall,  and at least a D+ average in each of the components.
* * To earn a grade of C, you must have at least an C average overall,  and at least a D average in each of the components.
* * To earn a grade of C-, you must have at least an C average overall,  and at least a D- average in each of the components.
* To earn a grade of D+, D or D- you need only to have that letter grade average overall (no additional criteria apply).

A+ grades: These may be awarded to the very best performing students in the class—but the cutoff for A+ grades will be determined at the end of the course at the discretion of the instructor (there is no pre-determined cutoff).   Students earning an A+ grade must be in the top 10% of each of the five components of the grade in the class.  The instructor may decide, at their discretion, to not award any A+ grades.

Missing homework/in-class activities: Drop the lowest n grades 
-------------------------------------------------------

If you miss a participation assignment, you miss the opportunity for the points on that participation assignment, or homework that was due. 

Rather than providing a makeup opportunity, I will drop:
* the lowest 3 participation assignments
* the lowest 2 homework/quiz grades 

This should be sufficient to allow for occaisional personal situations that may prevent your participation; if there is some special circumstance beyond your control where greater consideration may be needed, please contact the instructor; they will consider these on a case-by-case basis.

Each homework and in-class-activity will be of equal value (100 pts).


Project Points
==============

Project points will be earned by contributing to one of several open source legacy code projects.  You'll be
assigned to a project team, and the project team will be assigned to a set of bug fixes and feature requests.
This mirrors real world software development practice.

To earn a "perfect score" (100%) for this component of your grade, you need to earn 100 project points. If you only earn 80, then an 80% will be recorded for that portion of your grade.

Some assignments in the project category are worth more points, and some worth fewer.

If you accumulate more than 100 project points, up to 10 project points may be used to raise your final average in the class. (The points will be recorded as extra credit). 

You may not earn more than 110 total project points--any points in excess of 110 will not count towards your grade (though you'll probably learn a lot from having under taken the work to earn them.)


Late Programming Assignments
----------------------------

The policy is simple, and is based on the idea that the primary
purpose of the deadlines is to allow the TA manage his/her
workload. The number of labs in this course requires that he/she not
have to do "context switching" between grading different labs. All
labs must be graded in one sitting, or he/she just won't be able to
keep up with the workload.

So:

-   If you want your work to be graded without penalty, turn it in on time.
-   If you turn in your lab late, you RISK GETTING A ZERO.
-   We will grade late labs ONLY if it creates no extra inconvenience for the graders, and we WILL impose a penalty between 10-20% (see the individual grading rubrics for the labs.)
-   There is NO GUARANTEE that late labs will be graded at all. The TA will simply start work at some point after the deadline, and grade until he/she is finished. At that time, he/she will "close the books" on that particular lab, and any work not submitted at that time will NOT be considered.


Questions about grades
----------------------

**Summary: regrade requests must be made only on GradeScope, and always within one week.**

From time to time, the people who grade your papers may make clerical
errors in grading (e.g. adding up points wrong or applying a rubric
incorrectly.) For this reason, you are encouraged to review your
grades as they are posted to Gradescope and Gauchospace. You will
typically get an email as soon as each grade is posted. From the time
the grade is posted, you will have one calendar week to post regrade
requests. These must be made ONLY through Gradescope, ON the correct
problem. (Don't request a regrade for question 4 on the page for
question 7.)

Please note that <b>regrade requests based on clerical errors or
applying a rubric incorrectly are always welcome</b>. Over the course
of the quarter, we'll grade over 10,000 individual problems, so it is
unlikely that we won't make at least some mistakes.

<b>More problematic are challenges to the rubric itself</b>, e.g. "I
don't think you should have taken off so many points for that error"
or "I think I deserve more partial credit for that incorrect
answer". The instructor and TA will always listen, but please know
that we've put a great deal of thought, time and experience into
determining the rubric, and we've done our best to apply it to all
students equitably. You may have a different point of view, we will
not always agree with your assessment—in fact, we seldom will. <b>As
such, regrade requests on this basis are not encouraged.</b> It is
important to approach such conversations in a respectful manner,
accepting that the instructor, TA and grader have been given
responsibility for determining course standards, and applying those in
a fair way to all students.


Accommodations for disabilities
-------------------------------

Students with disabilities may request academic accommodations for exams online through the UCSB Disabled Students Program at http://dsp.sa.ucsb.edu/. Please make your requests for exam accommodations through the online system as early in the quarter as possible to ensure proper arrangement.

Managing stress
---------------

Personal concerns such as stress, anxiety, relationships, depression, cultural differences, can interfere with the ability of students to succeed and thrive. For helpful resources, please contact UCSB Counseling & Psychological Services (CAPS) at 805-893-4411 or visit http://counseling.sa.ucsb.edu/ .

Responsible scholarship
-----------------------

Honesty and integrity in all academic work is essential for a valuable educational experience.  The Office of Judicial Affairs has policies, tips, and resources for proper citation use, recognizing actions considered to be cheating or other forms of academic theft, and students’ responsibilities, available on their website at: http://judicialaffairs.sa.ucsb.edu.  Students are responsible for educating themselves on the policies and to abide by them.

Furthermore, for general academic support, students are encouraged to visit Campus Learning Assistance Services (CLAS) early and often. CLAS offers instructional groups, drop-in tutoring, writing and ESL services, skills workshops and one-on-one consultations. CLAS is located on the third floor of the Student Resource Building, or visit http://clas.sa.ucsb.edu

Standard Disclaimer
-------------------

This syllabus is as accurate as possible, but is subject to change at
the instructor's discretion, within the bounds of UC policy.

(end of syllabus)


