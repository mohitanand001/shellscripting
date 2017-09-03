# Bash Scripting
Some useful links <br>

## Scripting vs Programming<br>
Scripting languages are those which do not require an explicit compilation step.
ex: Javascript,Lua. <br>
Programming Languages on the other hand require an explicit compilation step.
ex: C,C++. <br> 
Infact whether a language is programming or scripting, depends on the environment,meaning<br> 
to say, we can actually write a 'C interpreter' or a 'Javascript compiler'.<br>
https://stackoverflow.com/questions/17253545/scripting-language-vs-programming-language

## What is Shebang?<br>
You probably have seen the starting line of many shell scripts, as the following<br> 
```
#!/bin/bash
```
This is called shebang
It actually defines which program actually runs the current script.In fact we can use shebang on any file
be it Python, Javascript.. <br>
https://unix.stackexchange.com/questions/87560/does-the-shebang-determine-the-shell-which-runs-the-script <br>

## What is $PATH? <br>
$PATH is an environment variable, which lists colon seperated list of directories. <br>
```
echo $PATH
/home/mohit123/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:
/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/home/mohit123/bin
```
Whenever you type a command on the shell, the command is searched in these directoris, in the order <br> of their occurrance.
If the command is not found here, an error is displayed.<br>
https://askubuntu.com/questions/551990/what-does-path-mean
<br>
Adding a command to one of these directories will make your command accessible from anywhere.<br>
https://unix.stackexchange.com/questions/3809/how-can-i-make-a-program-executable-from-everywhere

## Floating point numbers in Bash
How to use floating point in bash.(Bash does not support floating point arithmetic inherently)
https://stackoverflow.com/questions/12722095/how-do-i-use-floating-point-division-in-bash

## Storing in a variable
```
var1=5                                  #store a constant
var2=$var1                              #store a variable
var3=$((var1+var2))                     #store the result of an arithmetic expression   
var4=$(($var1+$var2))                   #store the result of an arithmetic expression
var5=$( ls | wc -l )                    #substituting a command/or return value from a function
var6=$( func_name $param1 $param2 )     #storing the return value  from a function
```
It is important that there is no space between the varialble the '=' sign and the rhs.<br>
## Directory existence
How to detect whether a directory exists or not. <br>
https://stackoverflow.com/questions/59838/check-if-a-directory-exists-in-a-shell-script?answertab=votes#tab-top

## Single quotes vs Double quotes!!
```
var1=5
echo 'the value of var1 is $var1'
echo "the value of var1 is $var1"
```
The first one will print <br>
```
the value of var1 is $var1
```
The second one will print <br>
```
the value of var1 is 5
```

## I/O
1. Simple Read
2. Read with prompt (p)
3. Read with silence (s)
4. echo 