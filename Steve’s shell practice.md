# Steve's shell practice
## Shell

Shell is a computer program which allow to run our commands, programs, and shell scripts. The shells has own st of recongnized commands and functions. if we are familiar with commands and functions, it will help us to analze large data conveniently.

## Basic commands in Shell (OS/Linux)
Bash is the GNU Project's shell. this allow us to create some commands in plain .txt file to operate through bash scripts.

## Practice 

### Initial screen (in OS terminal)
```sh
SeungHyunui-MacBook-Pro:~ seunghyunkang$
```
it can be differed based on setting of computer owner. But basically similar setting with $ sign at the end. Then, lets create shell script (shell file) by using the command. 

### Making .sh file (shell file)
You can simply make shell script by using command "touch file.sh"
```sh
SeungHyunui-MacBook-Pro:~ seunghyunkang$ touch myscirpt.sh
```
![lsimage.jpg](https://www.dropbox.com/s/6quk98327e9mv4w/lsimage.jpg?dl=0&raw=1)
When you input this command, you will findout the myscript.sh file has created in into your root dircetory. you can use command "ls" to list up your file and directory in your bash screen like the picture above. Now, Lets make directory to storage our shell file 

### Making directory and moving .sh file to the directory.
To make directory you need to use command "mkdir name". if you wan to move your file to that dircetory, you gotta use command "mv file.sh directoryname"
```sh
SeungHyunui-MacBook-Pro:~ seunghyunkang$ mkdir Practice
```
```sh
SeungHyunui-MacBook-Pro:~ seunghyunkang$ mv myscript.sh Practice
```

#! /bin/bash

## ECHO CMMAND
```sh
echo Hello World!
```

## VARIABLES
### Uppercase by convention
### letters, number, underscores
```sh
NAME="Steve"
echo "My name is $NAME"
```

## USER INPUT
```sh
read -p "Enter your name: " NAME
echo "Hello $NAME, nice meet you!"
```

## Simple if Statement
```sh
if [ "$NAME" == "Steve" ]
then
    echo "Your name is Steve"
fi
```

## IF-ELSE
```sh
if [ "$NAME" == "Steve" ]
#then
    echo "Your name is Steve"
else echo "Your name is not Steve"
fi
```

## ELSE-IF(elif)
```sh
if [ "$NAME" == "Steve" ]
then
   echo "Your name is Steve"
elif [ "$NAME" == "Rachel" ]
then 
    echo "Your name is Rachel"
else echo "Your name is not Steve nor Rachel"
fi
```
## Comparison 
```sh
NUM1=31
NUM2=5
if [ "$NUM1" -gt "$NUM2" ]
then
    echo "$NUM1 is greater than $NUM2 "
else
    echo "$NUM1 is less than $NUM2"
fi
```

## more functions
vall -eq val2 Returns True if the values are equal
vall -ne val2 Returns true if the values are not equal
vall -gt val2 Returns true if the val1 is greater than val2 
vall -ge val2 Returns true if the val1 is greater than or equal to val2
vall -lt val2 Returns true if the val1 is less than val2 
vall -le val2 Returns true if the val1 is less than or equal to val2



## File Condtion 
-d file True if the file is a directory
-e file True if the file exists (note that this is not particularly protable, thus -f is generallly used)
-f file True if the provided string is a file
-g file True if the group id is set on a file
-r file True if the file is readable
-s file True if the file has non-zero size
-u      True if the use id is set on a file
-w      True if the file is writable
-x      True if the file is an executable

```sh
FILE="test.txt"
if [ -e "$FILE" ]
then
    echo "$FILE exist "
else
    echo "$FILE does not exist"
fi
```

## Case statement 
```sh
read -p "Are you 21 or over? Y/N " ANSWER
case "$ANSWER" in 
    [yY] | [yY][eE][sS])
    echo "You can have a beer :)"
    ;;
    [nN] | [nN][oO])
    echo "Sorry, no drinking for ya"
    ;;
*)
    echo "Please enter y/yes or n/no"
    ;;
esac
```

## Simple for loop
```sh
NAMES="Steve Kevin Alice Rachel"
for NAME in $NAMES
 do 
    echo "Hello $NAME"
done
```

## For loop to rename files
```sh
FILES=$(ls *.txt)
NEW="new"
for FILE in $FILES
 do 
    echo "Renaming $FILE to new-$FILE"
    mv $FILE $NEW-$FILE
done
```

## WHILE LOOP - READ through a file line by line
```sh
LINE=1
while read -r CURRENT_LINE
 do
    echo "$LINE: $CURRENT_LINE"
    ((LINE++))
done < "./new-1.txt"
```

## FUNCTION
```sh
function sayHello() {
    echo "Hello World"
}
sayHello
```
## Function with params
```sh
function greet() {
    echo "Hello, I am $1 and I am $2"
}
greet "Brad" "28"
```

## creat folder and write to a file
```sh
mkdir hello 
touch "hello/world.txt"
echo "hello world" >> "hello/world.txt"
echo "created hello/world.txt"
```
