# CSE15L Lab Report 3 - Bugs and Commands (Week 5)

## Part1:Bugs
Part 1 - Bugs
Choose one of the bugs from week 4’s lab.

I chose the error of "averageWithoutLowest" in ArrayExamples.

Provide:
## 1.A failure-inducing input for the buggy program, as a JUnit test and any associated code (write it as a code block in Markdown)
Code inside ArrayTests.java：
''' 
@Test
  public void averageWithoutLowest() {
    double [] input1 = {-1.0, -2.0, -3.0, -3.0};
    double expected = -1.5;
    assertEquals(expected, ArrayExamples.averageWithoutLowest(input1), 0.01);
  }
'''

## 2.An input that doesn’t induce a failure, as a JUnit test and any associated code (write it as a code block in Markdown)
Code inside ArrayTests.java：
@Test
  public void averageWithoutLowest2() {
    double [] input1 = {1.0, 2.0, 4.0};
    double expected = 3.0;
    assertEquals(expected, ArrayExamples.averageWithoutLowest(input1), 0.01);
  }

## 3.The symptom, as the output of running the tests (provide it as a screenshot of running JUnit with at least the two inputs above)
![cd1](https://github.com/AdamMa2000/cse15l-lab-reports/blob/main/lab3.jpg?raw=true)

## 4. The bug, as the before-and-after code change required to fix it (as two code blocks in Markdown)
### The code before fix:
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

### The code after fix:
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

## 5.Briefly describe why the fix addresses the issue.
In the unmodified code, it is assumed that there is only one smallest number in the array. After finding this number, start using the for loop statement to start calculating the number of times this number appears. This does not require the smallest number in the array.

# Part 2 - Researching Commands

