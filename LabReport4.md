# Lab Report4 Vim(Week7)

For the lab report this week, reproduce the task from above on your own. For each numbered step starting right after the timer (so steps 4-9), take a screenshot, and write down exactly which keys you pressed to get to that step. For special characters like <enter> or <tab>, write them in angle brackets with code formatting. Then, summarize the commands you ran and what the effect of those keypresses were.

## Step4: Log into ieng6

screenshot：

![cd](LabReport4(1).png)

I used the following steps: 
1. First I type **ssh cs15lfa23ns@ieng6.ucsd.edu**
2. Press <Enter>
3. Enter my password. //*I successfully logged into ieng6.*

## Step5：Clone your fork of the repository from your Github account 

screenshot：

![cd](LabReport4(2).jpg)

I used the following steps: 
1. **git clone git@github.com:UCSDNobel1998/lab7.git**
2. Press <Enter> //*Clone by using SSH Url.*

## Step 6: Run the tests, demonstrating that they fail

screenshot:
![cd](LabReport4(3).jpg)

I used the following steps: 
1.type in **cd lab7**
2.<Enter>; //*Changed directory to lab7.*
3.javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java<enter> //*This command compiles all files ending with .java in the current directory, using JUnit.*
4.java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests //*The purpose of this command is to run the JUnit test class named ListExamplesTests to ensure that the required classes can be found during the running process.*

## Step 7: Edit the code file to fix the failing test

screenshot:
![cd](LabReport4(4).jpg)
![cd](LabReport4(5).jpg)
![cd](LabReport4(6).jpg)
