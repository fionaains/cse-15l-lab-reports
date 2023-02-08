# CSE 15L Skill Demonstration
## Fiona Ainsworth

## Step One
Login to ieng6

`ssh cs15lwi23atc@ieng6.ucsd.edu`

Source: Week One Lab Tasks 
[Week One](https://ucsd-cse15l-w23.github.io/week/week1/#lab-tasks)

## Step Two
Clone Repository

`git clone https://github.com/ucsd-cse15l-w23/skill-demo1-server.git`

Source: Week Two Lab Tasks
[Week Two](https://ucsd-cse15l-w23.github.io/week/week2/#lab-tasks)

## Step Three
Run JUnit Tests

Compile: 
`javac -cp ./lib/junit-4.13.2.jar:./libs/hamcrest-core-1.3.jar:. FileServerTests.java`
Execute:
`java -cp ./lib/junit-4.13.2.jar:./lib/hamcrest-core-1.3.jar:. org.junit.runner.JUnitCore FileServerTests`

Source: CSE 12 PA1 Instructions
[PA1 Instructions](https://github.com/CaoAssignments/cse12-wi23-pa1-RPS-starter)

## Step Four
Clone Repository 

`git clone https://github.com/ucsd-cse15l-w23/skill-demo1-data.git`

Source: See Step Two

## Step Five 
Count "*.txt" Files

`find skill-demo1-data/written_2/ -name "*.txt" | wc`

Source: Week Four Lab Tasks
[Week Four](https://ucsd-cse15l-w23.github.io/week/week4/)

## Step Six
Find "Lucayans" File

`grep -r  -l “Lucayans" skill-demo1-data/`

Source: See Step Five

## Step Seven
Start Server

`java FileServer 7638 skill-demo1-data/written_2/`

Source: Week Two Lab Tasks
[Week Two](https://ucsd-cse15l-w23.github.io/week/week2/#lab-tasks)

## Step Eight
Find "Lucayans" File on Server

`http://ieng6-201.ucsd.edu:1234`

Source: See Step Seven

## Step Nine
Search Query "ter" to Return Four Files
