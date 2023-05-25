<h1>LAB REPORT 3: RESEARCHING COMMANDS</h1>
<h2>Command Options: Grep Command</h2>

<h3>Grep -c Command</h3>
Example 1
```
madhavalapati@Madhavs-MacBook-Pro-2 911report % grep -c "and" chapter-6.txt
```
```
484
```
Example 2
```
madhavalapati@Madhavs-MacBook-Pro-2 911report % grep -c "Air" chapter-10.txt 
```
```
12
```
The `grep -c` command is command option that takes in the string input and .txt file and returns the number of lines containing the given string in the .txt file. This command is useful because it allows users to understand and count the prevalence and occurances of a given string in a .txt file.


<h3>Grep -l Command</h3>
Eaxmple 1
```
madhavalapati@Madhavs-MacBook-Pro-2 911report % grep -l "Bomb" *
```


```
chapter-12.txt
chapter-13.3.txt
chapter-13.4.txt
chapter-13.5.txt
chapter-2.txt
chapter-9.txt
```

Example 2

```
madhavalapati@Madhavs-MacBook-Pro-2 911report % grep -l "9/11" *
```
```
chapter-1.txt
chapter-10.txt
chapter-11.txt
chapter-12.txt
chapter-13.1.txt
chapter-13.2.txt
chapter-13.3.txt
chapter-13.4.txt
chapter-13.5.txt
chapter-2.txt
chapter-3.txt
chapter-5.txt
chapter-6.txt
chapter-7.txt
chapter-8.txt
chapter-9.txt
preface.txt
```
The `grep -l` command is a great command option that prints the name of the text files in the current directory that have the given string argument. This command option is used to find files and sort the files together based on if they contain the string argument.


<h3>Grep -n Command</h3>







