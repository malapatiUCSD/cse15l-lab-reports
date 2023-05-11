<h1>LAB REPORT 2</h1>
<h2>Part 1: String Server</h2>

<h2>Part 2: Lab 3 Bug</h2>
![Image](lab2image.png)

Failing Input

This code was attempting to flip the arraylist but the bug was it flipped it twice, returning the elements to the same index as before.
This problem arose because the program iterates through the entire arraylist instead of just half of the indexes and flipping the first half.
An example of a failing input would be `int[] input = {};` It would return `{}`. As expected
An example of a failing input would be `int[] input1 = {1, 2, 3};` It would return `1, 2, 3`. 
<h2>Part 3: What I Learned</h2>
