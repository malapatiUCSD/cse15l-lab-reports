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

Example 1
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

<h3>Grep -i Command</h3>

Example 1
```
madhavalapati@Madhavs-MacBook-Pro-2 911report % grep -i "door" chapter-9.txt
```
```
                hallways contained within the stairwell proper. Each hallway contained smoke doors
                kept closed but not locked. Doors leading from tenant space into the stairwells were
            Doors leading to the roof were locked. There was no rooftop evacuation plan. The
                hallways and smoke doors. Neither full nor partial evacuation drills were held.
                evacuations were not part of the evacuation plan, or that doors to the roof were
                stairwells, and impeded by doors that appeared to be locked but actually were jammed
                became confused when he reached a smoke door that caused him to believe the stairway
            Others ascended to attempt to reach the roof but were thwarted by locked doors. At
                complex controlled by the buildings' computerized security system, including doors
            Others, attempting to descend, were frustrated by jammed or locked doors in
                units to chiefs either in the North Tower lobby or at the outdoor command post.
            A chief at the overall outdoor command post was under the impression that he was to
                Tower, and Field Comm then attempted to convey that report to chiefs at the outdoor
                extensive air rescue. Several factors made this impossible. Doors leading to the
                command station prevented a lock release order from taking effect. Even if the doors
                civilians were not informed in fire drills that roof doors were locked, that rooftop
                the deviations in the stairways and by smoke doors. This confusion delayed the
```

Example 2
```
madhavalapati@Madhavs-MacBook-Pro-2 911report % grep -i "west" chapter-13.3.txt
```
```
                everywhere, even in rural midwestern churches. Qutb's views were best set out in
                friendly, pliable neighbor on the west due to its hostile relationship with India on
                11, 2001," undated. For the focus on the Southwest border, see Commission analysis
            15. See Madeleine Albright, speech at Nashir Bagh refugee camp in western Pakistan,
```
The `grep -i` command takes in a string argument and a text file and prints every line in the text file that contains the string input, but unlinke `grep -n` it is not case sensitive nor does it return the line number that the string argument occurs on. This command is useful to understand where in the text the string input is regardless of being upper-case or lower-case. It is good to use `grep -i` if a string is likely to be used both upper-case and lower-case throughout a text.

<h3>Grep -n Command</h3>

Example 1
```
madhavalapati@Madhavs-MacBook-Pro-2 911report % grep -n "once" chapter-10.txt
```
```
29:                returned to Air Force One. The next destination was discussed: once again the Secret
162:                chapter 3). Ashcroft told us he was determined to take every conceivable action,
280:                making substantial concessions in allowing use of its territory and that he would
440:                concerned that Iraq would take advantage of the 9/11 attacks. She recalled that in
445:            A Defense Department paper for the Camp David briefing book on the strategic concept
```

Example 2
```
madhavalapati@Madhavs-MacBook-Pro-2 911report % grep -n "stairwells" chapter-9.txt
```
```
26:            Each tower contained three central stairwells, which ran essentially from top to
34:                mezzanine. All three stairwells ran essentially straight up and down, except for two
35:                deviations in stairwells A and C where the staircase jutted out toward the perimeter
39:                kept closed but not locked. Doors leading from tenant space into the stairwells were
40:                never kept locked; reentry from the stairwells was generally possible on at least
59:                lighting systems failed. The unlit stairwells filled with smoke and were so dark as
63:                of the towers' occupants via the stairwells took more than four hours.
82:                markings were added in and near stairwells. The Port Authority also installed a
104:            But during these drills, civilians were not directed into the stairwells, or provided
273:                of the building's stairwells became impassable from the 92nd floor up. Hundreds of
366:                stairwells, and impeded by doors that appeared to be locked but actually were jammed
480:                not know if any stairwells into the impact zone were clear; and they did not know
633:                NorthTower-one of the stairwells (A) initially remained passable from at least the
683:                stairwells or confused by the structure of the stairwell deviations. By the lower
684:                70s, however, stairwells A and B were well-lit, and conditions were generally
755:                stairwells, conditions were otherwise fairly normal on floors below the impact. At
771:                should "be careful, stay near the stairwells, and wait for the police to come up."
850:                much damage was done on the upper floors, whether the stairwells were intact or
1068:                of the Twin Towers' stairwells. While he continued to monitor the citywide SOD
1108:                the North Tower, directing civilians leaving stairwells A and C to evacuate down an
1279:                the stairwells and shouted the evacuation order:"All FDNY, get the fuck out!"As a
1630:                damage to or impassable conditions in the building's three stairwells. The only hope
1640:                event that all stairwells were impassable below.
```

The `grep -n` command takes in a string argument and a text file and prints entire line including the line numbers in that text file that contain the given string input. This command is useful to understand which lines in the text include the string input and where it is used.

---
**Source:** For all of the `grep` commands, I used the site [https://www.geeksforgeeks.org/grep-command-in-unixlinux/](https://www.geeksforgeeks.org/grep-command-in-unixlinux/) in order to understand the command line options and their functionalities.


