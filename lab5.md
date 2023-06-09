<h1>LAB REPORT 5</h1>
<h2>Part 1 – Debugging Scenario</h2>
<h3>Student Question</h3>
<img width="1512" alt="Screenshot 2023-06-08 at 11 03 45 PM" src="https://github.com/malapatiUCSD/cse15l-lab-reports/assets/130113314/433a0da6-f30c-4a83-abf5-388193829f15">

`ListExamples.java` code:

<img width="1512" alt="Screenshot 2023-06-08 at 11 30 18 PM" src="https://github.com/malapatiUCSD/cse15l-lab-reports/assets/130113314/5cbc7d06-1f93-40bc-8a24-d004aaa8d303">


The bug/symptom I keep seeing is:
<img width="1148" alt="Screenshot 2023-06-08 at 11 31 37 PM" src="https://github.com/malapatiUCSD/cse15l-lab-reports/assets/130113314/8d2674bc-706b-4a12-813f-e343f878206f">

After entering the two commands:
`javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java`

Followed with:

`java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests`



<h3>TA Response</h3>
Upon examining your code and reviewing the displayed output, it appears that the test failed due to differing array lengths. This suggests the presence of a factor in your code that is influencing the size of the array. Specifically, on line 26, I noticed that the lengths of your index1 and index2 arrays are inconsistent. When utilizing conditional loops to index these arrays, it is generally recommended to begin the indexing from 0. Therefore, it would be advisable to modify the starting value of index1 from 1000 to 0.

There has to be a space before 1 in the condition, because bash thinks `[` is a command. This should fix the bug that is present. The .sh file is bug.sh and it need a space before the 1. That is all that needs to be fixed and you should be good to go!
<h3>Student Response</h3>
<h3>Information Needed About The Setup</h3>
<h2>Part 2 – Reflection</h2>
Something cool I learned during the second half of the quarter would be the `grep` commands. I learned this during Lab from week 5 and 6 and from Lab Report 3. It showed me the cool searching techniques of many text files and ways to access specific information using `grep`.
I learned 4 unique commands: `grep -n`, `grep -l`, `grep -c`, and `grep -i`. They all have super cool funtionalities.
The `grep -n` command takes in a string argument and a text file and prints entire line including the line numbers in that text file that contain the given string input.
The `grep -l` command is a great command option that prints the name of the text files in the current directory that have the given string argument.
The `grep -c` command is command option that takes in the string input and .txt file and returns the number of lines containing the given string in the .txt file. 
The `grep -i` command takes in a string argument and a text file and prints every line in the text file that contains the string input, but unlinke `grep -n` it is not case sensitive nor does it return the line number that the string argument occurs on. This command is useful to understand where in the text the string input is regardless of being upper-case or lower-case. These four commands are genuinely cool things I learned in the second half of CSE 15L. Thank you for all your help!
