# Lab Report 3, Week 5

## The "grep" Command
* For this week's lab report, I have decided to learn more about the "grep" command
and research different nuances to be aware of when using the "grep" command.
* The "grep" command is used to search through files to find which one contains a 
specified string input.
* The source for this research is ChatGPT, which I used to find different ways 
to use the command "grep" and to ask about their specific usages. 

------ 

## The "fgrep" Command

------

* The "fgrep" command is used when searching for exact matches to the inputted string.
Therefore, if the inputted string contains extra characters or punctuation that are not
contained in the file, it will not be returned by "fgrep" whereas it will be by "grep".
* I will demonstrate the difference between "fgrep" and "grep" by giving examples of 
different outputs searching for the same string using each command.

Example 1

Input:
` grep -r -l "Bond Stores." * ` 
Output:
```
non-fiction/OUP/Abernathy/ch2.txt
non-fiction/OUP/Abernathy/ch1.txt
```

Input:
` fgrep -r -l "Bond Stores." * `
Output:
Nothing returned

Example 2

Input:
` grep -r -l "La Muerte." * `
Output:
```
non-fiction/OUP/Castro/chC.txt
non-fiction/OUP/Castro/chM.txt
```

Input: 
` fgrep -r -l "La Muerte." * `
Output: Nothing returned

## The "egrep" Command

* The "egrep" command, according to ChatGPT, has "advanced pattern matching capabilities"
as it introduces a couple of new characters. For example, * is used to denote repeated
characters and [] are used to match a range of characters.
* It is important to note that, in trial, the outputs of using the "grep" command versus
the "egrep" command while searching through "written_2" were identical. ChatGPT inferred 
that the "grep" command, in this case, is a version that supports the special characters
which are usually only supported by egrep.

Example 1

Input: 
` egrep -r -l "Padil*" * `
Output: 
```
non-fiction/OUP/Castro/chC.txt
travel_guides/berlitz1/WhereToFrance.txt
travel_guides/berlitz2/Costa-WhereToGo.txt
travel_guides/berlitz2/Algarve-WhereToGo.txt
```

Example 2

Input:
` egrep -r -l "Skelet.." * `
Output:
```
non-fiction/OUP/Castro/chC.txt
travel_guides/berlitz1/WhereToLosAngeles.txt
```

## The "--color" Command

* The --color command is important because it will not only search for the given 
string within a series of files, it returns the file which is edited to that the 
specified string is highlighted and in red. This is important because when doing 
research, for example, one might want to refer to exactly in the text where the 
given subject is mentioned. The highlight and color of the text helps us to find
this information very quickly.

Example 1
Input: 
` grep -r --color "baffled, bewildered" * `

Output:
```
non-fiction/OUP/Berk/ch1.txt:baffled, bewildered parents
```
*It is important to note that the output of this example has the phrase "baffled, 
bewildered" in red text.*

Example 2

Input: 
` grep -r --color "Acquiring and Enacting" * `

Output: 
```
non-fiction/OUP/Berk/CH4.txt:Acquiring and Enacting the Rules of Social Life
```
*It is important to note that the output of this example has the phrase "Acquiring and 
Enacting" in red text.*

## The "-w" Command

* The "-w" command is used to denote that the inputted string must be the whole 
word when searching for it in the given files. This means that the inputted string
cannot be a substring and will not return the file if it only contains the whole word.
* This is helpful because it narrows down the search. For example, if one were to search
for the file that contains the word "an", the results will not be filled with files
that contain other words containing "an" such as "animal".

Example 1
Input:
` grep -r -l "himpered" * `
Output: 
```
non-fiction/OUP/Berk/CH4.txt
```

However, when we use the -w command:
Input:
` grep -r -l -w "himpered" * `
Output:
No output

* This is because the file contains the word "whimpered", so it shows up in grep 
but not for grep -w.

Example 2
Input:
` grep -r -l "dentifiable" * `
Output: 
```
non-fiction/OUP/Castro/chP.txt
travel_guides/berlitz1/WhereToDublin.txt
travel_guides/berlitz1/WhereToMadeira.txt
travel_guides/berlitz1/WhereToJerusalem.txt
```

With -w command:
Input:
` grep -r -l -w "dentifiable" * `
Output:
No output
