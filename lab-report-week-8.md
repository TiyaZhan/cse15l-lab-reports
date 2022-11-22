# LAB REPORT WEEK 8

### Script for `grade.sh`
```
rm -rf student-submission
git clone $1 student-submission
CPATH=".:../lib/hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar"
cd student-submission
if [[ -e ListExamples.java ]]
then
    echo "Correct files submitted"
else
    echo "Wrong files submitted! Score 0/4"
    exit
fi

cp ../TestListExamples.java ./
javac -cp $CPATH *.java
if [[ $? -eq 0 ]]
then   
    echo "Successfully Compiled"
else   
    echo "Compile Error! Score 0/4"
    exit
fi

java -cp $CPATH org.junit.runner.JUnitCore TestListExamples > ../result.txt

cd ../
grep "Failures: 1" result.txt
if [[ $? -eq 0 ]]
then 
    echo "Score: 3/4"
    exit
fi
grep "Failures: 2" result.txt
if [[ $? -eq 0 ]]
then 
    echo "Score: 2/4"
    exit
fi
grep "Failures: 3" result.txt
if [[ $? -eq 0 ]]
then 
    echo "Score: 1/4"
    exit
fi
grep "Failures: 4" result.txt
if [[ $? -eq 0 ]]
then 
    echo "Score: 0/4"
    exit
fi

echo "Great Work! Score: 4/4"
```

# Student submission Example 1
![exp1](/images/w8-1.1.png)

# Student submission Example 2
![exp2](/images/w8-1.2.png)

# Student submission Example 3
![exp3](/images/w8-1.3.png)


I will trace the `grade.sh` using the submission from example 3.

## Trace

```
rm -rf student-submission
```
There is not standard output or standard error for this command. The return code is zero.

```
git clone $1 student-submission
```
There is no standard output for this command.  The standard error for this command is `Cloning into 'student-submission'...`. The return code is zero.

```
CPATH=".:../lib/hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar"
```
This line is just storing the path to a variable, so it's not necessary a command.

```
cd student-submission
```
This command changes the current directory to student-submission. There are no standard output and error for this command. The return code is zero. 

```
if [[ -e ListExamples.java ]]
then
    echo "Correct files submitted"
else
    echo "Wrong files submitted! Score 0/4"
    exit
fi
```
The if statement here checks for if the path ListExample.java exist in the current directory. The exit code will be 0 if it does, and will be 1 if it does not. In the case of this submission, the student has the file `ListExamples.java` inside, so the exit code will be 0 and condition is satisfied. Then, the then-command is run. 

Inside the then-command, the `echo` command has a standard output `Correct files submitted` and no standard error. The return code is zero. The command inside of else-command was not ran, because the condition for if statement was evaluated as true.

```
cp ../TestListExamples.java ./
```
This command copies the TestListExamples.java into the student-submission directory. There are no standard output or standard error for this command. The return code is still zero.

```
javac -cp $CPATH *.java
```
This `javac` command compiles the java files inside student-submission directory. There is no standard output for this command. The standard error is:
```
ListExamples.java:15: error: ';' expected
        result.add(0, s)
                        ^
1 error
```
The return code for this command is non-zero.

```
if [[ $? -eq 0 ]]
then   
    echo "Successfully Compiled"
else   
    echo "Compile Error! Score 0/4"
    exit
fi
```
For this if statement, it compares the exit code produced by the last command with 0. If the exit code equals 0, the condition is evalutated as true, and false otherwise. Since the last command is the `javac -cp $CPATH *.java` command and it has a exit code of non-zero. The condition for the if statement is not statisfied, so **the command inside of then-command was not ran**. The command inside of else-command was ran. The `echo` command produces a standard output `Compile Error! Score 0/4`. There is no standard errro for this command. The exit code is zero. Then, the `exit` was ran to quit the bash script early. There is no standard output or error for `exit` command. **All the command after the `exit` command were not ran in this case.**