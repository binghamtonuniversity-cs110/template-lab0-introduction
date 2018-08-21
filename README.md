#### CS 110 - Fall 2018
# Lab 1 - Getting Familiar with Your Environment
## Due Date: 5:00 p.m., August 31st, 2018

*All programs will be tested on the machines in the LNG103 lab. If your code does not run on the system in this lab, it is considered non-functioning EVEN IF IT RUNS ON YOUR PERSONAL COMPUTER. Always check that your code runs on the lab machines before submitting.*

### Driver Code and Test Files

* lab1.py

### Grading Rubric

**_TOTAL: 10 points_**
* **Part B: 8 points**
    * Must have at least 2 commits (3 points)
    * Must have at least 1 issue posted (3 points)
    * Google form submitted (2 pts)
* **Part C: 2 points**
    * Follows requested project structure and submission format
    * Follows [formatting guidelines](https://docs.google.com/document/d/1RU9bHsJhc4wecOXelXF5uUjcNTce4f2I0-09kJKvRvk/edit?usp=sharing)

### Guidelines

This is an individual lab assignment. You must do the vast majority of the work on your own. It is permissible to consult with classmates to ask general questions about the assignment, to help discover and fix specific bugs, and to talk about high level approaches in general terms. It is not permissible to give or receive answers or solution details from fellow students.

You may research online for additional resources; however, you may not use code that was written specifically *to* solve the problem you have been given, and you may not have anyone else help you write the code or solve the problem. You may use code snippets found online, providing that they are appropriately and clearly cited, within your submitted code.

*By submitting this assignment, you agree that you have followed the above guidelines regarding collaboration and research.*

## Part A: Learning the Environment and Writing the code

Part A must be completed in lab. Each lab during the semester will have a Part A that you must attempt to complete in lab. As soon as you complete Part A, you may show the TA and leave. If you cannot complete Part A by the end of lab, speak with the TA at the end of lab.

If you miss your lab time without prior arrangements with me or the TA, you cannot make up or complete part A outside of lab. In this case, you will not receive credit for Part A, even if completed (_many labs will require you to complete Part A in order to complete the lab_).

There will usually be additional parts to the lab that may be completed outside of lab on your own time.

_In this lab, you will learn to_:

* Use the command line to issue commands to the operating system
* Write and execute a simple python program in a command-line environment
* Use `git` to manage your projects and submit your work for grading.

Look for these icons!

| | Meaning |
|:----:|---------|
| :bulb: | Tips and useful information |
| :warning: | Caution! This could cause you problems. |
| :no_entry_sign: | Danger! Don't do this! |

Log into a machine using your PODS user id and password. (If you're reading this online in the lab, you've probably succeeded in doing this already.) Locate and launch a "terminal". We will call this, inter-changeably, a **terminal**, **shell**, or **command line**. The shell will accept and execute Linux commands, of which there are hundreds. We'll learn a few today, and I'll try to introduce you to more and more throughout the semester. You will need to get used to using the terminal, so don’t be afraid of it. You can’t ‘hurt’ the computer from the terminal.

The Linux help system is accessible through the system man pages. This is standard on all Unix/Linux distributions. "man" is short for "manual" (but the command is "man"). To access the man pages for a particular command, at the command prompt type the command "man" (without quotes) followed by the command you are interested in, followed by the <ENTER> key.
* :bulb: The basic format of entering commands in the terminal is:
    * *command* -*options* *args*
        * *command* : starts a program, just like clicking on an icon in the windowed environment
        * *option* : optional configuration flags that change the way the program runs. Usually preceded by a dash, -.
        * *args* : arguments the program needs to run, such as a key or filename
* For example, to read about the "pwd" command, type `man pwd`
    * This will open up the man program and display the help information for the pwd command. In the man page environment, to go forward and look at additional information that does not fit on the first screen, press the **ENTER** key.
* To exit the man page program, type the letter `q`.
* We will be using the following commands often, so review them in the man pages:
    * man
    * echo
    * pwd
    * mkdir
    * rm
    * cd
    * ls
    * mv
    * cp
    * python3
* :warning: *These are Linux specific commands. Although some commands are similar on the windows console, most will not work the same or at all.*


### Using Linux Commands

Next, you will begin running and using some of the commands you learned about in the previous section above. In particular, complete the following steps:
* On the command line, type: cd ~
    * This takes you to your home directory if you are not already there.
    * :bulb: The ~ is just a shortcut symbol that means home directory
* Create a directory named cs110. On the command line, you can do this with the following command:
    * mkdir cs110
* Change your "current working directory" to be the cs110 directory. To do this, execute the following command:
    * cd cs110
        * You can navigate *up* a directory using the `..` command. For example, `cd ..` goes up the directory tree.
* Confirm that you are in fact in the cs110 directory by typing the command:
    * pwd
* Next you are going to create a file with a brief explanation of the 3 of the commands you looked up in the previous section. You will use 3 commands to create and verify your file: `echo`, `>>`, `cat`.
    * The `echo` command prints whatever you pass to it to the console. Essentially, it _echos_ what you say to it.
    * You can easily create or append a text file in the terminal with the `>>` command. The `>>` command redirects output to a file instead of printing it.
        * You can use these two commands to quickly create a small text file.
            * `echo "Hello World" >> test.txt`
    * You can now use the `cat` command, which just prints whatever is in a file, to verify the file contents.
        * `cat test.txt`
    * Choose 3 of the above 10 commands you looked up, and create a text file called `commands.txt` that briefly explains, in your own words, what the commands do.
        * `echo "cd changes to another directory" >> commands.txt`

## Part B: Writing the Code
The next thing we are going to do is learn how to work with git and github.
First, let's set up our git credentials. Enter the following two commands in the terminal:

`git config --global user.name "Firstname Lastname"`

`git config --global user.email "email@binghamton.edu"`

:warning: **Replace `Firstname Lastname` and `email@binghamton.edu` with your information**

You should be in your cs110 directory. If you are not, go back to part A and try to figure out how to get there. If you need help, ask someone.

In this directory, you are going to clone this repository to get a copy of the source code onto your account. To do this, you will first need to have signed up for a Github account if you didn't already have one.

### Github
You will need a Github account to submit your labs. You will also use your Github account any time you need help with your code. If you do not already have one, you can go to [Github](https://github.com) and sign up.

Once you have signed up for an account, fill out and submit the following google form:
[https://goo.gl/forms/qAbilZWoDCukNCpk2](https://goo.gl/forms/qAbilZWoDCukNCpk2)

:warning: You must log in with your bmail to use the form.

:bulb: If you have any trouble, ask for help.

When you click on the link to fork your own repo of Lab 1, github will set things up for you.

:warning: :warning: :warning: :warning: :warning: :warning:

**It is extremely important that you do not interrupt the setup process. It can sometimes take up to 5 minutes to set everything up depending on Github's current server load. If you interrupt the process, we will have to manually fix it for you.**

:warning: :warning: :warning: :warning: :warning: :warning:

Once the fork has completed setting up, look at the Github landing page for your fork of this project. You should see a green button that says "Clone or download". Press it and you should see a URL like https://github.com/binghamtonuniversity-cs110/lab-1-fall18-username.git. Copy that text somewhere you can access it, then go back to the terminal.

Next, be sure you are still in the cs110 directory and execute the following command in the terminal:

`git clone URL`

:bulb: *where URL is the copied text ending in ".git".*

We will explore git workflows in-depth later in this lab.

Now that we have our repository set up, we will edit the code. Change your directory to the cloned repository. If you aren't sure how to do this, first review part A, and try to figure it out. As a last resort, ask for help.

If you are not already familiar with a linux editor, please use gedit, which has several nice features for Python code development.

:warning: Beware that gedit is a linux editor, and will not work on other OS's (Windows, Mac, etc.).

You can use gedit to open a file by typing, for example, the following into a linux command shell:

`gedit lab1.py &`

If there is no file in the current folder named *lab1.py*, then gedit will create a new empty one for you (remember, you can check your current folder location with `pwd`). If the file does exist, it will edit the existing file. If you cloned the git repository correctly, you should have a `lab1.py` file with the following contents:

```python
def main():
    print("Hello World")
main()
```

:bulb: The ampersand at the end of the command says to run this application in the background. This will allows you to write some code, save it, then run it in the shell without quitting gedit.

After making changes to a file, you can save it by clicking "Save" at the top of the gedit window, or with the hot key command `<ctrl-s>`. Note that if you have made changes to an open file, and those changes have not been saved, the file name across the top of the window will be preceded by an asterisk (for example, "\*lab1.py"). To exit from gedit, make sure your modifications are saved, and then type `<ctrl-q>` in the gedit window, or simply close the gedit window by clicking the “x” in the upper right hand corner.

Open the accompanying *lab1.py*  program with gedit. You must keep the format, indentation, and capitalization EXACTLY as it is!

* First run the program by typing the following command into the terminal: `python3 lab1.py`
    * :bulb: If you are not in the correct folder, you will get an error. Please review the commands form part A to navigate to the correct folder.

### Submitting an issue
What if you have a problem with your code? That's what we are here for, and Github makes it easy to get help.
* Navigate back to your repo on Github. One of the tabs is labeled **issues**. Click on this tab.
* You should see a green button labeled **New Issue**. Click on this button to create a new issue.
* Submit your issue by providing the following:
    * Title - should be descriptive of the problem
    * In the body provide
        * Filename
        * Line number(s)
        * Description of the issue
* After you submit your issue, you can click on the ellipses (...) in the top right corner, and select **CopyURL**. You can then post this URL on Piazza.

:warning: This is always the process for getting help with your code. If you copy and paste code into Piazza or just link to your repo without creating an issue, we will ask you to create an issue first, which will delay how quickly we can help you.

## Part C: Submission
* Required code naming and organization:
    * lab1.py

:no_entry: Every lab will have a required submission guidelines. Please read submission requirements carefully. Any deviations from specifications on future labs or projects will result in point deductions or incomplete grades.

### Git

In this and future labs, we will use Github Classroom repositories. You have already [forked](https://help.github.com/articles/fork-a-repo/) this repository when you accepted the emailed link. That makes a copy of the repository, free for you to make changes. Then you cloned your forked repository to get a working copy onto this machine.

Now that we have made local changes to our working copy, let's [commit](https://git-scm.com/docs/git-commit) those changes to the repository:

:warning: *These commands all presume that your current working directory is within the directory tracked by `git`.*

```shell
git commit -a -m "first commit"
```

The `-a` says that git should add all tracked files with changes to your commit, and the `-m` says the next string contains the commit message, which is required by git any time you make a commit.

What about _untracked files_? Remember the commands.txt file you created earlier? You are going to have to move it into your working folder, and add it to the repository. I am assuming you created the file in the parent directory. If you created it somewhere else, you will need to adjust the following commands accordingly.

Run the following commands:

```shell
cd ..
mv commands.txt <repo folder>
cd <repo folder>
git status
```
:warning: You should replace <repo folder> with the name of your folder.

You'll notice that `git` tells us that `commands.txt` is an _untracked file_. That means it's not being tracked by the repository. Let's fix that by [adding](https://git-scm.com/docs/git-add) it.

```shell
git add commands.txt
git commit -a -m "Added commands.txt file"
```
:warning: *You* __must__ *add any new files you create to the repository with the `git add` command or they will not upload to the repo, and your code will not work.*

Once we've made the commits for a given coding session, we need to add those to the repository by performing a [push](https://git-scm.com/docs/git-push):

```shell
git push
```

Lastly, the next time we begin a coding session, we will need to [pull](https://git-scm.com/docs/git-pull) to ensure we have the most updated working copy.

```shell
git pull
```
:bulb: You should get a message that you are already up to date.

This will allow you to keep your code in the lab and on your own computer synchronized if you want to work outside of lab.

Lastly we are going to make our final commit. You will need to do this when your submission is ready for grading.

```shell
git commit -a -m "final commit message"
git push
```

:bulb: You may get a message that there have not been any changes. That's okay, that just means you have already *saved* all changes.

You can commit as often as you like, and revert your code to any previous commit using the **commit hash**. The commit hash is a long number that identifies a specific version of your code. I recommending making commits often with a comment describing the state of your code. To find your most recent commit hash, use the following command:

```shell
git rev-parse HEAD
```    
You should get a long, strange looking number:
```
35e27598324d8b4d7ddeb4d7aa8abe91c6263705
```

To complete your submission, you must copy and paste this number into mycourses. Go to MyCourses, select CS110, and **Assignment Hash Submission**. Select Lab 1, and where it says text submission, paste your commit hash. The TAs will only grade your submission that corresponds to the hash you submitted. You can update this as often as you like until the deadline.

I strongly recommend making a submission early on, even if your assignment is not 100% working, to avoid late penalties.

:warning: You __MUST__ submit the commit hash on mycourses before the deadline to be considered on time **even if your lab is completely working before the deadline**. :warning:

That's it! We've completed our work for this lab. We will use this submission process for all subsequent labs and assignments.

:bulb: Useful `git` references:
- https://guides.github.com/introduction/flow/
- https://help.github.com
- https://git-scm.com/doc
