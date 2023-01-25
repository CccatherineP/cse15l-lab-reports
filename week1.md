# Installing VScode
1. The first step we did is to make sure that we have VScode installed on our computers<br />
* Go to the Visual Studio Code website [Link](https://code.visualstudio.com/) and follow the instructions to download the VScode to your own computer
* pay attention that there are versions for all the major operating systems, like macOS (for Macs) and Windows (for PCs).
* when you finish downloading the VScode, you would be able to see the window as below when you open the VScode. 
<img width="1440" alt="Untitled" src="https://user-images.githubusercontent.com/122485099/211921441-9caf3397-6295-4026-a2f3-3e148cbd7366.png"> <br />

# Change CSE15L account
2. The second step we do is to change our password for the CSE15L account, we just need to follow the steps which the course has already provided<br />
* We first need to look up the course-specific account for CSE15L here:[Link](https://sdacs.ucsd.edu/~icc/index.php)
* If you need further help, please follow the the tutorial [Link](https://docs.google.com/document/d/1hs7CyQeh-MdUfM9uv99i8tqfneos6Y8bDU0uhn1wqho/edit)
* In this situation, we usually need to wait couple of minutes during the process

# Remotely Connecting
3. After changing our passwords, we need to go to the terminal and connect our laptops to the server, and when we finish that, we can see the screen just like the screenshot I took.<br />
In order to open the terminal, you can basically find the terminal entrance from the bar
Here are several steps during the process:<br />
1)Type `ssh cs15lwi23zz@ieng6.ucsd.edu` in the terminal, which I typed `ssh xpang@ieng6.ucsd.edu` into my terminal<br />
2)Then we type "yes"<br />
3)Type our password we just changed and everything will work<br />
![Untitled](https://user-images.githubusercontent.com/122485099/211921702-75a4eb3b-e9d2-40fd-a1dd-6d71334e0e95.jpg)

# Running Command
4. The last step is to put in some commands and see if it works, and the screenshot is the picture below<br />
In this case, you can try different things: `ls`, `cd`, `pwd`, `mkdir`, `cp`, `ls -lat` and so on...<br />
* You can try entering these commands on both your own computer and the remote computer, you could find out the outputs might be different
* The most interesting output I received is when I type `ls -lat` into my terminal, which I got a long result which is showed in my screenshot
* Here are also some hints to log out of the remote server in your terminal:<br />
1)Ctrl-D<br />
2)Run the command `exist`<br />
![2](https://user-images.githubusercontent.com/122485099/211921771-bab5011c-33a8-40ac-b7dd-7e159ce86af5.jpg)<br />
Then, everything will be working fine! If you follow the instructions step by step and I think that wouldn't take too much time and effort!
