<h1>LAB REPORT 4</h1>
<h2>Step 4: Log into ieng6</h2>
<img width="1512" alt="Screenshot 2023-06-07 at 10 45 10 PM" src="https://github.com/malapatiUCSD/cse15l-lab-reports/assets/130113314/613b67ed-2eeb-4241-8d0f-19e10b3a023e">

To log into my ieng6 account, I simply just typed:

`ssh cs15lsp23xx@ieng6.ucsd.edu <enter>`

in the terminal since `<enter>` allows the terminal to run the command.
Since I have already set up a **SSH key**, I am able to log into my
remote account without the need to type my password in.
<h2>Step 5: Clone your fork of the repository from your Github account</h2>

<img width="1512" alt="Screenshot 2023-06-07 at 10 50 14 PM" src="https://github.com/malapatiUCSD/cse15l-lab-reports/assets/130113314/cb2468e2-9d57-4160-a7d3-f67cd63873bb">

To clone the repository, I simply copied the link from GitHub and typed:

`git clone https://github.com/ucsd-cse15l-s23/lab7 <enter>` 

It says `'lab7' already exists and is not an empty directory` due to the fact that I already cloned the lab7 during the actual lab.

<h2>Step 6: Run the tests, demonstrating that they fail</h2>
<img width="1512" alt="Screenshot 2023-06-07 at 10 54 27 PM" src="https://github.com/malapatiUCSD/cse15l-lab-reports/assets/130113314/aafddefe-6c80-4dc7-aa22-e35f64dd6815">

During this step, we expect the tests to fail, but first we would need to compile the files in the directory. In order for me to get into the right directory, I typed:

`cd lab7/ <enter>` 

which would basically bring me to *lab7* directory. I used `<enter>` because tab basically autofil the directory as long as there aren't
any files with similar names in the root directory. Next, I typed `<Ctrl-C> javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` 
to copy the command and `<Ctrl-V> javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java <enter>` to paste the command into my terminal
in order to compile the files. Afterwards, I did the same thing `<Ctrl-C> java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` to copy and `<Ctrl-V> java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests <enter>` to paste the
command to run tests on the terminal. As we could see on the screenshot above, the output showed that there were 2 tests run and 1 failure. 


<h2>Step 7 - Edit the code file to fix the failing test</h2>
Now that we know there is one failure on the tests, we can do open a text editor in the terminal by simply typing `nano ListExamples.java`. This will allow us to edit the code inside the terminal. It should look something like this:

<img width="1512" alt="Screenshot 2023-06-07 at 10 59 10 PM" src="https://github.com/malapatiUCSD/cse15l-lab-reports/assets/130113314/c32cbbbe-89d3-40ab-8b27-31b5e0317dd4">


To check on what was wrong with the code, I typed


`
<down>
`

until I saw what was causing the error
and then I found out that the final (bottom) *index1* is supposed to be *index2*, so in order to fix this I typed `<right>` until I reached *1* and then I typed `<delete><2>` to change it to *2*. Finally,
after making all these changes, I typed `<Ctrl-O> <enter>` to write and save the changes and `<Ctrl-X>` to exit the nano 
text editor. 
<h2>Step 8: Run the tests, demonstrating that they now succeed</h2>

After completing these steps, it is now obvious that we would want to re-run the tests to see if it would pass or not. Since
I have previously typed all those commands in the terminal, this time I simply just need to type `<up>` until I find the compile command and then hit `<enter>` to run the tests. 


<img width="1512" alt="Screenshot 2023-06-07 at 11 08 32 PM" src="https://github.com/malapatiUCSD/cse15l-lab-reports/assets/130113314/375d3c70-c233-4ca9-b2ec-8172d0a5f55b">

As you can see, all the tests have now passed!

<h2>Step 9: Commit and push the resulting change to your Github account </h2>
Because all of the tests passed, we can commit and push the file into the *GitHub* repository by typing `git add *` to select all the files
in the curretn directory and `git commit -m "new file"` to take a snapshot of all the changes made to the file and the message 
that you want to put after changing the file. It should look like this:


<img width="751" alt="Screenshot 2023-06-07 at 11 49 32 PM" src="https://github.com/malapatiUCSD/cse15l-lab-reports/assets/130113314/7401066c-49cb-455c-9594-9c16c5852a55">

Finally, I typed `git push` to forward the changes into my repository on GitHub and it should like this:

<img width="1307" alt="Screenshot 2023-06-07 at 11 43 51 PM" src="https://github.com/malapatiUCSD/cse15l-lab-reports/assets/130113314/a0afc661-db83-4c34-b700-8460f9772aff">



