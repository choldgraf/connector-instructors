# Getting Started as a Connector Instructor

## Points of contact

**Sam Lau** (samlau95@gmail.com), **Chris Holdgraf** (choldgraf@berkeley.edu),
and **Elaine Angelino** (elaine@berkeley.edu) are your current points of contact
about issues and questions you may have as a connector instructor. Email us with
questions or [ping us on slack][slack].

[slack]: https://data8-connectors.slack.com/messages/general/

## Who is this for?

These guides are intended for connector instructors interested in creating
material that utilizes the same infrastructure as the main course.

Specifically, if you would like to use [**IPython notebooks**][ipython] and
optionally the [**`datascience`**][datascience] package in your course, this
guide is for you.

[ipython]: http://ipython.org/notebook.html
[datascience]: https://github.com/data-8/datascience

If you do not want to use this infrastructure that's fine by us. We'd be happy
to help you in whatever capacity we can.

## Setup

If you run into issues or questions with any of these steps, contact Sam or
Chris with your issue(s). It's our responsibility to make sure you have access
to the needed websites.

You'll need an account on https://data8.berkeley.edu/ . You should be able to
log in to that site with your @berkeley.edu email address. If you run into a:

![screenshot 2016-01-17 10 41 37](https://cloud.githubusercontent.com/assets/2468904/12379069/6dd0cf96-bd07-11e5-9261-18f99528f050.png)

This means that you don't have access yet. Ping either Sam or Chris.

You'll also need an account on [Github][github] and the ability to push to the
Github repo associated with your connector course.

[Github][github] is a website that hosts code and files. A repository on Github
holds the files for a specific project. Each connector class has a repository.
If you don't know what your repository is, contact Sam.

[github]: https://github.com/

## Workflow

Here's a rough overview of the workflow we use in the main class. We'll base the
rest of this tutorial on these steps. Feel free to add/remove steps as fit for
your course.

Click a link to jump to that section of this guide.

1. [Create a notebook.](#creating-notebooks)
2. [Push the notebook to Github.](#pushing-your-notebooks-to-github)
3. [Distribute the notebook to students.](#distributing-notebooks)
4. [Students work on notebooks.](#student-work)
5. [Students submit their completed notebooks to you.](#student-submission)

[data-8]: https://github.com/data-8
[interact]: http://data8.org/text/1_data.html#example-plotting-the-classics

Here's a diagram of the steps.

![connector-instructor](https://cloud.githubusercontent.com/assets/2468904/12474089/f8ac3700-bfcc-11e5-988a-5f686788c4fc.png)

Let's talk in more detail about each of these steps.

### Creating notebooks

![step1](https://cloud.githubusercontent.com/assets/2468904/12474029/6d17c1be-bfcc-11e5-80f8-fbc7ff25aa57.png)

This guide is intended for those with **no prior experience** with Jupyter,
`git`, or Github. Feel free to develop your own workflow if you know what you're
doing.

#### Setting up your repo

First, visit https://data8.berkeley.edu/ and log in. You should see a screen that
looks something like the one below. Click the "Terminal" button as marked:

![screenshot 2016-01-05 17 54 11](https://cloud.githubusercontent.com/assets/2468904/12132922/70ea3a22-b3d5-11e5-983a-6cd2aae3b10f.png)

You should see a screen that looks like this:

![screenshot 2016-01-05 17 56 14](https://cloud.githubusercontent.com/assets/2468904/12132944/a2dfd758-b3d5-11e5-920b-14b622d4efec.png)

This is a terminal that allows you to run commands. Type the following into the
terminal:

    git clone https://github.com/data-8/<repo_name>

Where the `<repo_name>` is the name of the repository for your connector. The
repository names are listed at https://github.com/data-8. For example, if you
are the instructor for the Health connector, you'd write:

    git clone https://github.com/data-8/health-connector

#### Adding your content

After this step, you should be able to see your connector's folder at
https://data8.berkeley.edu/ . **Once your folder is there, you do not have to
repeat the steps in the Setting up your repo section.**

Click on your folder to go inside that directory.

![screenshot 2016-01-05 18 02 28](https://cloud.githubusercontent.com/assets/2468904/12133071/a1a3be9e-b3d6-11e5-9efa-74cffcaba1e0.png)

You should see a screen like the one below. Click the button marked by the arrow
in the below image to create a new notebook. You may create a notebook in any
folder as long as the folder is in your connector folder. That is, in the
above example you may create a notebook in `~/health-connector/foo/bar/`, but
not `~/some_other_folder`.

![screenshot 2016-01-05 18 04 33](https://cloud.githubusercontent.com/assets/2468904/12133094/d7786e98-b3d6-11e5-8118-3a82bec33492.png)

Fill in the notebook with your content.

**Example notebooks:** For examples of notebooks, you can see
the [table demos][demos] or find all raw notebooks for the textbook [here](https://github.com/data-8/textbook/tree/gh-pages/notebooks).The main class uses notebooks for lectures, labs, and
projects. In addition,

**Adding datasets:** If you have datasets/other needed files to distribute or
use in a notebook, you can upload them using the button as labeled below:

![screenshot 2016-01-19 22 15 32](https://cloud.githubusercontent.com/assets/2468904/12441280/429ce95a-befa-11e5-8e61-869452920490.png)

[demos]: https://github.com/deculler/TableDemos
[textbook]: http://data8.org/text/

### Pushing your notebooks to Github

![step2](https://cloud.githubusercontent.com/assets/2468904/12474031/6d1a12e8-bfcc-11e5-83e4-e2dc5b420e6b.png)

Once your notebook is ready for distribution, you must to upload it to Github so
that it can publicly accessed online.

For those who are familiar with `git` and Github, push your file(s) to the
`gh-pages` of your repo. The file(s) should then be available at
`http://data8.org/<repo_name>/<file_name>`.

If you are not familiar with `git`/Github, follow the instructions below.

1. On data8.berkeley.edu, open a new terminal. (New -> Terminal)
2. Type in

        cd <repo_name>

    Where the `<repo_name>` is the name of your repository (eg.
    `health-connector`).

3. Type

        git status

    You should see something that lists the files you've changed. If your
    changed files don't show up, ensure that they are in your repo's folder.

4. Type the following commands:

        git add -A
        git commit -m 'Update'
        git push origin gh-pages

    If you run into something that looks like:

        ERROR: Permission to data-8/some-connector.git denied

    Contact Sam. This means that you don't have the right access to Github.

5. Verify that you can access your file by visiting
`http://data8.org/<repo_name>/<file_name>`. For example, for the `Demo2.ipynb`
file in the `health-connector` repo you'd use the link:
http://data8.org/health-connector/Demo2.ipynb .

If the last step doesn't work, double the check the steps above and contact us
on a persisting issue.

### Distributing notebooks

![step3](https://cloud.githubusercontent.com/assets/2468904/12474090/f9d45bb2-bfcc-11e5-8884-1ec12945f828.png)

Once your notebook is uploaded to Github, you can give your students links that
work like the Interact buttons in the textbook.

Create a link like the following:

    https://data8.berkeley.edu/hub/interact?repo=<repo_name>&path=<path_name>

Where the `<repo_name>` is replaced with your repo name and `<path_name>` is
replaced with the path to a file or folder in the repo.

For example, if you have a working link of
http://data8.org/health-connector/Demo2.ipynb, the link you'd give students is:

    https://data8.berkeley.edu/hub/interact?repo=health-connector&path=Demo2.ipynb

Any student that visits this link will end up with their own copy of the
`Demo2.ipynb` file in a folder called `health-connector` their
data8.berkeley.edu account. You can repeat this for any file, not just
notebooks.

**I want to push a folder of content to students.** You can! If you have a
folder called `datasets` in the `health-connector` repo, you'd give students:

    https://data8.berkeley.edu/hub/interact?repo=health-connector&path=datasets

**I made a typo and want students to get an updated version.** Sure! If you
update a file, students can grab the update by visiting the original link again.

Note that in some cases an update would conflict with students' work (eg.
updating a notebook that students have filled out). In such a case, the system
will give up trying to update the file in favor of preserving the students'
work.

**A student messed up his work. Can he/she start over?** Certainly. Have the
student delete or rename the bad file/folder, then visit the link again. The
original file/folder will appear good as new!

### Student work

![step4](https://cloud.githubusercontent.com/assets/2468904/12474033/6d1d97ce-bfcc-11e5-8fb5-373c31c034b2.png)

You can use notebooks as a supplement to a lecture. For example, [here's a cool
notebook about probability][prob-nb]. Here's [a notebook we use to explore
literature][books-nb] in the [first chapter of the textbook][ch1].

[prob-nb]: http://nbviewer.jupyter.org/url/norvig.com/ipython/Probability.ipynb
[books-nb]: https://github.com/data-8/textbook/blob/gh-pages/notebooks/Books.ipynb
[ch1]: https://ds8.gitbooks.io/textbook/content/chapter1/example-plotting-the-classics.html

You can also use notebooks as assignments (the Data 8 class does both). You can
check out [the notebook we use for Lab 1 for Data 8][lab1] as an example of
this.

[lab1]: https://github.com/data-8/data8assets/blob/master/labs/lab01/lab01.ipynb

As you can see from the lab, we have cells that the students fill in. You can
make notebooks like this as well and distribute them to students in the same way
as detailed above.

In that example above, we give Data 8 students this link to get the lab (and its
related files):

    https://data8.berkeley.edu/hub/interact?repo=data8assets&path=labs/lab01

### Student submission

![step5](https://cloud.githubusercontent.com/assets/2468904/12474032/6d1a431c-bfcc-11e5-9944-e150c2277eef.png)

Unforunately as of right now we don't have an easy way for students to submit
their work programmatically. You can accept submissions through email, bCourses,
or otherwise.

Students are currently able to download their notebooks off their
data8.berkeley.edu accounts in multiple formats, including `.pdf`, `.py`, and
`.ipynb`. They can download a notebook by opening it, turning Edit mode **on**,
then navigating to File -> Download as -> Format of choice.

An easy way to collect work is for students to export a notebook as a PDF file
and then submit to bCourses. We have autograding for Data 8 but it requires set
up. Let us know if you'd like to learn how to set that up.

## FAQ
**Q: Where can I find old materials for this course?**
    
>A: See http://data8.org/fa15/ for the set of materials from Fall 2015. It contains links to topics covered, sample notebooks, homeworks, etc.

**Q: How can I get a new package added to my students' servers?**
    
>A: Create a new issue in this github repo, and attach a notebook that shows this package to it. We'll try to integrate any additional libraries that your notebook specifies. The more lead time we have the better. Ping Ryan on the issue.*

> When we do update the single user server with new software, it requires that students stop and start their server.

**Q: Where can I find some example notebooks?**
    
>A: **Example notebooks:** For examples of notebooks, you can see
the [table demos][demos] or find all raw notebooks for the textbook [here](https://github.com/data-8/textbook/tree/gh-pages/notebooks). The main class uses notebooks for lectures, labs, and projects.

**Q: How can I more closely follow the class material?**
    
>A: Most of the material will mimic the previous semesters of Data8. However, some material will change (at least in timing if not in content). Those decisions will be made by John close to real time. The best bet is to look at the outline from the syllabus and then find the corresponding sections in [the textbook](http://www.inferentialthinking.com) to see how the material is covered. The textbook is basically the lecture notes from last semester.

**Q: What should I do if students want to join my connector without taking data8**
    
>A: There aren't going to be any "official" course resources for teaching people python/notebook/etc skills if they aren't enrolled in the main data 8 course. If the student has previously taken data8, then it shouldn't be a problem. If they have not taken data8, then:

>   A. Remind them that the main course is a pre/co-requisite for any connector. (aka it is generally discouraged)

>   B. If they really want to join, then the instructor can make a personal choice whether to include them. We'd recommend that you give some kind of personal assessment, written exam, etc to make sure that it won't create a lot of extra work for the instructor.

**Q: Where can I ask a question that wasn't answered here?**
    
>A: You can either open an issue in this repository, ask on the Slack chatroom, or email the connector assistants
