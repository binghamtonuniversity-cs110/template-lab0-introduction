**Lab 1 - Getting Familiar with Your Environment**

CS 110 - Fall 2017

Due Date: 5:00 p.m., Aug 31st, 2017

*All programs will be tested on the machines in the LNG103 lab. If your code does not run on the system in this lab, it is considered non-functioning EVEN IF IT RUNS ON YOUR PERSONAL COMPUTER. Always check that your code runs on the lab machines before submitting.*

### Driver Code and Test Input Files

* N/A

### Grading Rubric

**_TOTAL: 10 points_**

* **Part B: 8 points**

    * Code runs as expected

* **Part C: 2 points**

    * Follows requested project structure and submission format

    * Follows [formatting guidelines](https://docs.google.com/document/d/1RU9bHsJhc4wecOXelXF5uUjcNTce4f2I0-09kJKvRvk/edit?usp=sharing)

### Guidelines

This is an individual lab assignment. You must do the vast majority of the work on your own. It is permissible to consult with classmates to ask general questions about the assignment, to help discover and fix specific bugs, and to talk about high level approaches in general terms. It is not permissible to give or receive answers or solution details from fellow students. 

You may research online for additional resources; however, you may not use code that was written specifically *to* solve the problem you have been given, and you may not have anyone else help you write the code or solve the problem. You may use code snippets found online, providing that they are appropriately and clearly cited, within your submitted code. 

*By submitting this assignment, you agree that you have followed the above guidelines regarding collaboration and research.*

Part A: Learning the Environment and Writing the code

Log into a machine using your PODS user id and password. (If you're reading this online in the lab, you've probably succeeded in doing this already.) Locate and launch a "terminal". We will call this, inter-changeably, a **terminal**, **shell**, or **command line**. The shell will accept and execute Linux commands, of which there are hundreds. We'll learn a few today, and I'll try to introduce you to more and more throughout the semester. You will need to get used to using the terminal, so don’t be afraid of it. You can’t ‘hurt’ the computer from the terminal.

The Linux help system is accessible through the system man pages. This is standard on all Unix/Linux distributions. "man" is short for "manual" (but the command is "man"). To access the man pages for a particular command, at the command prompt type the command "man" (without quotes) followed by the command you are interested in, followed by the <ENTER> key.

* The basic format of entering commands in the terminal is: 

    * <command> -<options> <args>

        * <command> : starts a program, just like clicking on an icon in the windowed environment

        * <option> : optional configuration flags that change the way the program runs. Usually preceded by a dash, -.

        * <args> : arguments the program needs to run, such as a key or filename

* For example, to read about the "pwd" command, type ‘man pwd’

    * This will open up the man program and display the help information for the pwd command. In the man page environment, to go forward and look at additional information that does not fit on the first screen, press the <ENTER> key. 

* To exit the man page program, type the letter q. 

* We will be using the following commands often, so review them in the man pages:

    * man

    * pwd

    * mkdir 

    * rm

    * cd

    * ls

    * mv

    * cp

    * python3

# Using Linux Commands

Next, you will begin running and using some of the commands you learned about in the previous section above. In particular, complete the following steps:

* On the command line, type: cd ~

    * This takes you to your home directory if you are not already there.

    * The ~ is just a shortcut symbol that means home directory

* Create a directory named cs110. On the command line, you can do this with the following command:

    * mkdir cs110

* Change your "current working directory" to be the cs110 directory. To do this, execute the following command: 

    * cd cs110

* Confirm that you are in fact in the cs110 directory by typing the command:

    * pwd

* Create a directory within cs110.... name it lab1. "cd" into this new directory.

* Type the command ‘python3’ to enter the Python Interactive Shell

    * Note the prompt (**<<<**) followed by your cursor (**|**)

    * This lets you know that you are in the Python shell, and that the interpreter is awaiting your input.

        * **The python shell is different from the linux terminal.**** **Think of it as a special python shell inside the linux shell.

    * Exit the shell with the exit() command

* The shell environment is the place where you should try out various Python expressions and statements, 

    * HOWEVER, it is NOT the proper environment in which to write an entire program

* In your interactive book, you can use the in-browser environment to write "snippets" of code, or Python scripts

    * These are NOT complete programs

* In our class:

    * Complete programs will always be written in Python scripts

    * Complete programs will have a **main()** function

    * Complete programs will include an invocation of the **main()** function

    * Each complete program will be saved in a separate file given a **camelCaseName** followed by a **.py** extension

    * (e.g., **computeAverageProfit.py**)

    * Note that file names should NEVER contain spaces

# Part B: Writing the Code

If you are not already familiar with a linux editor, please use gedit, which has several nice features for Python code development. You can use gedit to open a file with the appropriate name for your definitions, by typing, for example, the following into a linux command shell:

gedit lab1.py &

If there is no file in the current folder named lab1.py, then gedit will create a new empty one for you. The ampersand at the end of the command says to run this application in the background. This will allows you to write some code, save it, then run it in the shell without quitting gedit. After making changes to a file, you can save it by clicking "Save" at the top of the gedit window, or with the hot key command <ctrl-s>. Note that if you have made changes to an open file, and those changes have not been saved, the file name across the top of the window will be preceded by an asterisk (for example, "*lab1.py"). To exit from gedit, make sure your modifications are saved, and then type <ctrl-q> in the gedit window, or simply close the gedit window by clicking the “x” in the upper right hand corner.

Enter the following simple program into this new window:  you must follow the format, indentation and capitalization EXACTLY! You may use spaces or tabs, but you have to be consistent. NOTE: Be aware that if you will be working on a windows machine at home, spaces are more cross platform compatible.

**def main():**

**weeks_str = input("Please enter the number of weeks this semester:  ")**

**classes_str = input("Enter the number of classes you are taking:  ")**

**tuition_str = input("Please enter your tuition:  ")**

**weeks = int(weeks_str)**

**classes = int(classes_str)**

**tuition = int(tuition_str)**

**cost_per_week = ((tuition / classes) / weeks)**

**print("Cost per week:", cost_per_week)**

**main()**

* Run your program by saving your file as lab1.py, and typing the following command

    * python3 lab1.py

        * If you made an error when typing the program, you will see an error message

        * Fix the error and try again, if necessary - ask for help if you need it!

* Make the following changes to your program and run it:

    * Insert print statements after each line of the **main()**** **that prints the value and type of the variable assigned to in the previous line

    * Using the code I have given you as an example, make the following additions to your **main()** function:

        * Ask the user to input how many times per week a class meets and save that in a variable called *classes_per_week*. 

            * For example, our class meets 3 days a week

        * Calculate the cost per class by dividing the cost_per_week by the classes_per_week and save the result in a variable called cost_per_class

        * Print the cost per class to the console with a nice message

            * -- try to figure out the syntax of this based on the syntax and behavior of the rest of your program

            * Don’t forget to convert the input from the user to an int

* Save your program, then run it and debug if necessary

    * If you have any difficulty completing this first assignment, ask your TA or post a note on Piazza to get help!

# Part C: Submission

* Required code naming and organization:

    * lab1.py

* Upload the lab1.py file to Blackboard under Lab 1 before the deadline.

