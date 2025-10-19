---
layout: default
---

####Introduction
![Command-line course on Moodle](https:helloaino.github.com/assets/images/cmdline.png)
In this course I leared to work in a command-line environment (Ubuntu for Windows in my case) and using tools for text processing, writing bash-scripts and more. The course consisted of four Modules and a Final Project.

####Module 1: Introduction to Command Line Environments
In the first module, we installed our command-line environments and took the first steps to learning the basics of working in command-line. We were introduced to managing files and directories in the UNIX file system by moving, copying and removing directories. 

Basic commands:

This one tells me what my username is:

'''console
ainojj@laptop1:~$ whoami
ainojj
'''

Here I'm creating a directory called KIK-LG221 and then getting a list of files and directories in my home directory.

'''console
ainojj@laptop1:~$ mkdir KIK-LG221
ainojj@laptop1:~$ ls
KIK-LG221
'''

I already tried to complete this course last year, but dropped out. I remembered some of this stuff from last time but feel more comfortable using cmd-line now, and I think the course is organized in a clearer way, so this time around. 


####Module 2: Text processing in UNIX
In module 2 we learned about character encodings, file formats, basic text file operations using tools like grep, sed and piping. We made a frequency list from The Life Of Bee.

Example commands from module 2:

'''console
ainojj@laptop1:~$ cat life_of_bee.txt | dos2unix | sed 's/^$/#/' | tr '\n' ' ' | less

'''

This finds instances of word final "ssa" from the file katinka_rabe.utf8.txt:

'''console
ainojj@laptop1:~$ cat katinka_rabe.utf8.txt | egrep "ssa\b"

'''

The sed command is still a struggle for me, but overall I think I managed to learn quite a bit about text processing in command-line. Regex was thankfully familiar to me from Introduction to Language Technology. Knowing how to create frequency lists, convert a text into sentence-per-line format and create a list of n-grams will be useful in my studies.

####Module 3: Scripting, Configuration Files and Installing Programs

In module 3 we learned to write and run bash-scripts and installing software and give commands as the root user using sudo. We also learned to use Python in command-line.

Command used for module 3:

Installing pip:

'''console
ainojj@laptop1:~$ sudo apt-get install python-pip
'''

Bash script comparative_step4.sh:
'''bash
#!bin/bash

while IFS= read -r line; do
if [ "${line: -1}" = "y" ]  ;then
  echo $line | sed -E 's/(.*)y$/\1ier/g'
else
  echo "$line"er
fi

done < "$1"
'''

I can now install programs in command-line, which is great. I don't fully get what I would need a virtual Python environment in my command-line for, but that is an option now. I'm glad I learned how to make ssh keys.


####Module 4

In module 4 we learned about git, Github, and version control, but first we learned about remote servers, connected to CSC supercomputer Puhti to practice how to connect to a remote server. I made sure I have git installed, I have a repository in Github, and I can add, commit, and push changes to Github.

Commands:
'''console
ainojj@laptop1:~$ git add -A
ainojj@laptop1:~$ git commit -m "added picture file"
ainojj@laptop1:~$ git push
'''

Version control is really important, so I'm glad we learned about that. However, I feel skeptical about using Github since it's owned by Microsoft (I'm still a Windows user, though) and it pushes Copilot on me constantly, which I don't want. I also don't want my data to be used as training material for Copilot.


####Final Project

Making this assignment I learned to use Jekyll and Github Pages to a basic degree. I also learned to write Markdown files. It was fun to use Overleaf again, too, but I needed to allow my data to be processed in the USA to be allowed to log in, and it also had it's own generative AI bot function, which I do not want to use. 


