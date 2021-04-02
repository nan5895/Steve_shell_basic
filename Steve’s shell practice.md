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
