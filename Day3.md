# Linux for users
### Linux Commands
Linux systems uses shell and the shell helps us  to Communicate with the Kernel and helps to execute codes.
-->shell is also called "terminal".
#### basic commands:
- ls/ list directory: lists information about the files(the current directory by default).it has some options-->ls-l: list in detail
                            >ls-a: list including hidden files.(Linux hidden files start with a dot)
                            >ls-R: recursive
                            >ls filename
                            can be used with combination, ls-Rla
- cd/change directory: used to change current working directory. 
it has some options-->cd/ : back to root
                                  >cd  :back to home
                                  >cd.. :1x back
                                  >cd../.. :2x back
                                  >cd foldername
N.B: if the folder have a space it must be inside"___ ".
- pwd/ print working directory: prints the path of the working directory starting from the root.
- echo: displays line of text/string that are passed as an argument. this is a built in command that is mostly used in shell scripts and batch files to output status text to the screen or a file.
-it possible to write texts into files: echo text>file.txt
-also possible to add texts(append): echo text>>file.txt
- cat file: used to show the contents in the file.
- head file: show the first lines of the file.
- tail file: shows the last lines of the file.
- less: shows the file in a readable format.
- touch: creates an empty file.
-  mkdir/make directory: creates a folder(not a file)
- rm/remove: removes file.
    -it has many options-->rm-r: recursive(4 folders)
                           --->rm-i: for prompt(ask)
                           --->rm-f: force delete
                    ->in combination, rm-rf 'filename'

                    
