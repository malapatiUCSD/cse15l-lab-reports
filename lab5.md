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

Upon examining your code and reviewing the displayed output, it appears that the test failed due to differing array lengths. This suggests the presence of a factor in your code that is influencing the size of the array. Specifically, on *line 26*, I noticed that the lengths of your `index1` and `index2` arrays are inconsistent. When utilizing conditional loops to index these arrays, it is generally recommended to begin the indexing from **0**. Therefore, it would be advisable to modify the starting value of `index1` from **100** to **0**.

<h3>Student Response</h3>


Thank you for pointing that out. You were right about the `index1` length, because I started with **100**, it affected the rest of the code as the conditional statements only ran due to `index1` being smaller than `list1`. I fixed this bug by first typing `nano ListExamples.java` on my terminal so I can access the code itself and replace the **100** on `index1` with **0**. Then I saved and exit, compile and ran tests by using `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` and `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` exactly as I did before.
<img width="1512" alt="Screenshot 2023-06-08 at 11 41 53 PM" src="https://github.com/malapatiUCSD/cse15l-lab-reports/assets/130113314/5887f969-ca7a-431c-8273-30e0f0bde7e2">
<img width="1000" alt="Screenshot 2023-06-08 at 11 46 03 PM" src="https://github.com/malapatiUCSD/cse15l-lab-reports/assets/130113314/225223b4-3a79-417c-b46d-a66ad369c7e2">

<h3>Information Needed About The Setup</h3>
The file and directory used was `ListExamples.java` in *lab7*. `ListExamples.java` code before debugging with TA:
<img width="1512" alt="Screenshot 2023-06-08 at 11 30 18 PM" src="https://github.com/malapatiUCSD/cse15l-lab-reports/assets/130113314/5883fd42-ee00-48dd-aba9-728465d715fa">

The commands that I entered was `cd lab7` to enter the directory, `nano ListExamples.java` to access the code file through the terminal and to then change the size of `index1` to a very large number so that it will fail the while loops. In this case it was *100** To fix the bug, you can simply go back to the `ListExamples` file either through the terminal or just clicking the file on the left primary side bar on VScode, and change `index1` size back to **0**. Lastly, you would want to compile and run the tests by using the following commands:

`javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java`

`java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests`

<h2>Part 2 – Reflection</h2>
Something cool I learned during the second half of the quarter would be the `grep` commands. I learned this during Lab from week 5 and 6 and from Lab Report 3. It showed me the cool searching techniques of many text files and ways to access specific information using `grep`.
I learned 4 unique commands: `grep -n`, `grep -l`, `grep -c`, and `grep -i`. They all have super cool funtionalities.
The `grep -n` command takes in a string argument and a text file and prints entire line including the line numbers in that text file that contain the given string input.
The `grep -l` command is a great command option that prints the name of the text files in the current directory that have the given string argument.
The `grep -c` command is command option that takes in the string input and .txt file and returns the number of lines containing the given string in the .txt file. 
The `grep -i` command takes in a string argument and a text file and prints every line in the text file that contains the string input, but unlinke `grep -n` it is not case sensitive nor does it return the line number that the string argument occurs on. This command is useful to understand where in the text the string input is regardless of being upper-case or lower-case. These four commands are genuinely cool things I learned in the second half of CSE 15L. Thank you for all your help!
