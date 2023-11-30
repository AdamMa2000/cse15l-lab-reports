# Lab Report4 Vim(Week7)

## Part 1 – Debugging Scenario
Design a debugging scenario, and write your report as a conversation on EdStem. It should have:

1. The original post from a student with a screenshot showing a symptom and a description of a guess at the bug/some sense of what the failure-inducing input is. (Don’t actually make the post! Just write the content that would go in such a post)
### Original Student Post
***Title:*** Problem with the Java Program WordCounter: Inaccurate Word Count
***Content:*** Hi guys, I'm developing a Java program that can automatically count words, this program should count the number of characters in a file. However, I got a higher word count than expected. The following screenshot is what I got. I think this program may not handle spaces well. A calculation error occurs once I enter multiple spaces.

![cd](LabReport5(2).jpg)
![cd](LabReport5.jpg)


2. A response from a TA asking a leading question or suggesting a command to try (To be clear, you are mimicking a TA here.)

### TA's Response
***Title:*** Reply: Word count error in the Java Program WordCounter.
***Content:***  Hi there! It seems that the way your program divides lines into words may actually be connected to the issue. Do you take into consideration various kinds of whitespace characters in your reasoning? To handle multiple spaces and tabs, try modifying the line splitting code and observe the output that results. Try it out now!

3. Another screenshot/terminal output showing what information the student got from trying that, and a clear description of what the bug is.

### Follow-up Student Post
***Title:*** Modified the splitting logic in the code
***Content:*** I followed your suggestion and modified the splitting logic to help solve this problem. Below is a screenshot after I modified it. The word count within the document is now correct! thanks for your advice!

![cd](LabReport5(3).jpg)

4. At the end, all the information needed about the setup including:
* The file & directory structure needed

  
* The contents of each file before fixing the bug

  
* The full command line (or lines) you ran to trigger the bug

  
* A description of what to edit to fix the bug

You should actually set up and run the scenario from your screenshots. It should involve at least a Java file and a bash script. Describing the bug should involve reading some output at the terminal resulting from running one or more commands. Design an error that produces more interesting output than a single message about a syntax or unbound identifier error – showcase some interesting wrong behavior! Feel free to set this up by cloning and breaking some existing code like the grading script or code from class, or by designing something of your own from scratch, etc.
