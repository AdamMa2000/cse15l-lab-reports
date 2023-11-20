# CSE15L Lab Report 3 - Bugs and Commands (Week 5)

## Part1:Bugs
Part 1 - Bugs
Choose one of the bugs from week 4’s lab.

I chose the error of "averageWithoutLowest" in ArrayExamples.

---

Provide:
### 1.A failure-inducing input for the buggy program, as a JUnit test and any associated code (write it as a code block in Markdown)
Code inside ArrayTests.java：
```
@Test
  public void averageWithoutLowest() {
    double [] input1 = {1.0, 1.0, 10.0, 18.0};
    double expected = 14.0;
    assertEquals(expected, ArrayExamples.averageWithoutLowest(input1), 0.01);
  }
```

### 2.An input that doesn’t induce a failure, as a JUnit test and any associated code (write it as a code block in Markdown)
Code inside ArrayTests.java：
```
  @Test
  public void averageWithoutLowest2() {
    double [] input1 = {4.0, 6.0, 8.0};
    double expected = 7.0;
    assertEquals(expected, ArrayExamples.averageWithoutLowest(input1), 0.01);
  }
```

### 3.The symptom, as the output of running the tests (provide it as a screenshot of running JUnit with at least the two inputs above)
![cd1]()

### 4. The bug, as the before-and-after code change required to fix it (as two code blocks in Markdown)
**The code before fix:**
  ```
static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    double lowest = arr[0];
    for(double num: arr) {
      if(num < lowest) { lowest = num; }
    }
    double sum = 0;
    for(double num: arr) {
      if(num != lowest) { sum += num; }
    }
    return sum / (arr.length - 1);
  }
```

**The code after fix:**
```
static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    double lowest = arr[0];
    int countLowest = 0;

    for(double num: arr) {
      if(num < lowest) {lowest = num;}
    }

    for(double num: arr) {
      if(num == lowest) {countLowest++;}
    }
 
    double sum = 0;

    for(double num: arr) {
      if(num != lowest) { sum += num; }
    }
    
    return sum / (arr.length - countLowest);
  }
```

### 5.Briefly describe why the fix addresses the issue.
In the unmodified code, it is assumed that there is only one smallest number in the array. After finding this number, start using the for loop statement to start calculating the number of times this number appears. This does not require the smallest number in the array.

---

# Part 2 - Researching Commands#

Consider the commands less, find, and grep. Choose one of them. Online, find 4 interesting command-line options or alternate ways to use the command you chose. To find information about the commands, a simple Web search like “find command-line options” will probably give decent results. There is also a built-in command on many systems called man (short for “manual”) that displays information about command

I chose the ‘find’ command as an example.

### Give 2 examples of using it on files and directories from ./technical. Show each example as a code block that shows the command and its output, and write a sentence or two about what it’s doing and why it’s useful.

### Example1: Finding Files with a Specific Name

bash:
```
find ./technical -type f -name "example.txt"

```
output:
```
./technical/example.txt
./technical/subdirectory/example.txt
```

**Write a sentence or two about what it’s doing and why it’s useful.**
In this example, the find command searches for a file named example.txt in the technical directory. -type f refers to the file I need to find. -name refers to the name I want to match, which can be quickly and accurately positioned.

### Example2：Finding Directories with a Specific Name
bash: 
```
$ find . -iname "*gen*"
```
output:
```
./GeneratedData
./Genesis
./filegen123
./GENERIC
./subdirectory/GeneratedReports
```
*This example comes from ChatGPT*

**Write a sentence or two about what it’s doing and why it’s useful.**
The find command identifies files and directories with "gen" in their names, including files and directories with different letter cases, demonstrating how -iname can simplify searching for names with case variations. This is useful for quickly locating a specific file or directory when the case sensitivity of a name is uncertain.

---

### 1.Search Files Based On Owners and Groups

**Example1:**
```
$ find . -mmin -5
./test.txt
```

**Write a sentence or two about what it’s doing and why it’s useful.**
The meaning of this command is to find all the files and directories that I have modified in the past 5 minutes. This is very useful for me to find the files I just modified, and I don’t need to worry about forgetting what I modified.

**Example2**
```
$ find . -mmin -10
.
./test.txt
./test1.txt
./test2.txt
```

**Write a sentence or two about what it’s doing and why it’s useful.**
‘-mmin -10’ This command is used to search the current directory and its subdirectories for files or directories that have been modified in the past 10 minutes. The output shown includes the files test.txt and test2.txt because I just created two new files named test1.txt and test2.txt.

---

### 2.Find Files and Directories Based on Size
**Example1:**
```
# find / -size 50M
.
./test.txt
./test1.txt
```

**Write a sentence or two about what it’s doing and why it’s useful.**
The ‘-size 50M’ command means to find files that occupy less than 50 megabytes of memory.

**Example2**
```
# find / -size +80K -100M
.
./test.txt
```

**Write a sentence or two about what it’s doing and why it’s useful.**
'-size +80K -100M' means to find files with a file size greater than 80K and less than 100M.

---

### 3.Find Files Based on their Permissions

**Example1:**
```
# find . -type f -name "test1.txt" -exec rm -f {} \;
```

**Write a sentence or two about what it’s doing and why it’s useful.**
The meaning of this command is to find a file named ‘test1.txt’ and delete this file.

**Example2**
```
# find . -type f -name "*.txt" -exec rm -f {} \;
```

**Write a sentence or two about what it’s doing and why it’s useful.**
The meaning of -name "*.txt" is to find all files whose names end with '.txt' and delete all these files. This can be done in batches to delete some files with the same name.

---
Source: https://www.tecmint.com/35-practical-examples-of-linux-find-command/


