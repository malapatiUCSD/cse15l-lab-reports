<h1>LAB REPORT 4</h1>
<h2>Step 4: Log into ieng6</h2>
<img width="1512" alt="Screenshot 2023-06-07 at 10 45 10 PM" src="https://github.com/malapatiUCSD/cse15l-lab-reports/assets/130113314/613b67ed-2eeb-4241-8d0f-19e10b3a023e">

To log into my ieng6 account, I simply just typed:

`ssh cs15lsp23xx@ieng6.ucsd.edu <enter>`

in the terminal since `<enter>` allows the terminal to run the command.
Since I have already set up a **SSH key**, I am able to log into my
remote account without the need to type my password in.
<h2>Step 5: Clone your fork of the repository from your Github account</h2>
<img width="422" alt="image" src="https://github.com/lurany/cse15l-lab-reports/assets/130108693/6a3432ac-b1f2-45f9-aa68-47913d62eb7b">

To clone the repository, I simply copied the link from GitHub and typed:

`git clone <link from GitHub> <enter>` 

<h2>Step 6: Run the tests, demonstrating that they fail</h2>
<img width="422" alt="image" src="https://github.com/lurany/cse15l-lab-reports/assets/130108693/bea6afe3-afdf-48a6-a8c8-cb9efd24dc51">


During this step, we expect the tests to fail, but first we would need to compile the files in the directory. In order for me
to get into the right directory, I typed:

`$ cd la<tab>` 

which would basically bring me to *lab7* directory. I used `<tab>` because tab basically autofil the directory as long as there aren't
any files with similar names in the root directory. Next, I typed `<Ctrl-C> javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` 
to copy the command and `<Ctrl-V> javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java <enter>` to paste the command into my terminal
in order to compile the files. Afterwards, I did the same thing `<Ctrl-C> java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` to copy and `<Ctrl-V> java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests <enter>` to paste the
command to run tests on the terminal. As we could see on the screenshot above, the output showed that the test has 1 failure. 
<h2>Step 7 - Edit the code file to fix the failing test</h2>
Now that we know there is one failure on the tests, we can do open a text editor in the terminal by simply typing `$ nano ListExamples.java`. This will allow 
us to edit the code inside the terminal. It should look something like this:

<img width="426" alt="image" src="https://github.com/lurany/cse15l-lab-reports/assets/130108693/c96da625-ea31-4213-be78-b8f8405956f3">

To check on what was wrong with the code, I have to type 

`
<down>
<down> 
<down> 
<down> 
<down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down>
<down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down> <down>`

and found out that *index1* is supposed to be *index2*, so in order to fix this I have to type `<right><right><right>
<right><right><right><right><right><right><right><right>` to reach to *1* and `<delete><2>` to change it to *2*. Finally,
after making all these changes, I typed `<Ctrl-O><enter>` to write and save the changes and `<Ctrl-X>` to exit the nano 
text editor. 
<h2>Step 8: Run the tests, demonstrating that they now succeed</h2>
Now that we have finally made changes on the code, it is obvious that we would want to rerun the tests to see if it would pass or not. Since
I have previously typed all those commands in the terminal, this time I simply just need to type `<up><up><up><enter>` to go back to my compile
command then `<up><up><enter>` to run the tests. 

<img width="756" alt="image" src="https://github.com/lurany/cse15l-lab-reports/assets/130108693/f88c8cf5-b74f-4e89-b715-003eafc1512c">

As you could see, all the tests have passed!

<h2>Step 9: Commit and push the resulting change to your Github account </h2>
Since all the tests passed, we can commit and push the file into the *GitHub* repository by typing `$ git add *` to select all the files
in the curretn directory and `$ git commit -m "<updated file>"` to take a snapshot of all the changes made to the file and the message 
that you want to put after changing the file. It should look like this:

<img width="358" alt="image" src="https://github.com/lurany/cse15l-lab-reports/assets/130108693/d1e62dd0-d63a-4550-944c-c60a933bc43a">



Finally, I typed `$ git push` to forward the changes into my repository on GitHub and it should like this:



<img width="654" alt="image" src="https://github.com/lurany/cse15l-lab-reports/assets/130108693/e27777da-5567-4375-ae15-db54efd5759a">
