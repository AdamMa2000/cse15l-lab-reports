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

![cd](LabReport4(2).png)

I used the following steps: 
1. git clone git@github.com/AdamMa2000/lab7.git；
2. Press <Enter> //*Clone by using SSH Url.*

## Step 6: Run the tests, demonstrating that they fail

screenshot:
![cd](LabReport4(3).jpg)

I used the following steps: 
1. type in **cd lab7**
2. <Enter>; //*Changed directory to lab7.*
3. Type in "javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java<enter>" ; //*This command compiles all files ending with .java in the current directory, using JUnit.*
4.Type in "java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests" //*The purpose of this command is to run the JUnit test class named ListExamplesTests to ensure that the required classes can be found during the running process.*

## Step 7: Edit the code file to fix the failing test

screenshot:
![cd](LabReport4(4).jpg)

I used the following steps: 
1. Type in **ls**；<Enter> //*List all files in Lab7*
2. vim ListExamples.java；<Enter> //*Open the ListExamples.java file in Vim*
3. /index1；<enter> //*Search “index1”*
4. nnnnnnnnn; c + e //*I pressed the n key 9 times and found the "index1" that needed to be modified. Pressing the C and E keys simultaneously deleted "index1"*
5. Type in **index2** //*Enter "index2"*
6. <Esc> ：wq //*Save and exit*

screenshot:
![cd](LabReport4(5).jpg)
![cd](LabReport4(6).jpg)

I used the following steps: 
1. cat ListExamples.java //*After saving, I use the above command to check whether the file content has been modified successfully.*

## Step 8： Run the tests, demonstrating that they now succeed

screenshot:
![cd](LabReport4(7).jpg)

I used the following steps: 
1. <up><up><up><up><up> <Enter> "javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java"; <enter>; //*I found the command in history by pressing the up key five times*
2. java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTest; <enter>； //*The above command is JUnit running ListExamplesTest*

## Step 9: Commit and push the resulting change to my GitHub account

screenshot:

![cd](LabReport4(8).png)

I used the following steps: 
1. **git add ListExamples.java<enter>**；**<enter>** //*This command temporarily saves the changes to ListExamples.java*
2. **git commit -m "Update the ListExamples.java"**；**<enter>** //*This command will have a short prompt message after completing the changes.*
3. **git push**；**<enter>** //*This command can push the submitted content to GitHub.*
