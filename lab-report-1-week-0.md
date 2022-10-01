# Lab report 1
## **Installing VSCode**
1) First, you go to this website [https://code.visualstudio.com/](https://code.visualstudio.com/) to download and install VSCode on your computer.

2) If you are using the windows operating system then you should download the version for windows, if you are using Mac then you should download the version for Mac OS.

3) After you have finished downloading, you can start the installation process. You can click next on everything.
![Image](CSE15L_Images\LabReport1-1.png)
## **Remotely Connecting**
1) Before you go on with this step, you first have to figure out your username for the remote access, you can find this out by going to this website [https://sdacs.ucsd.edu/~icc/index.php](https://sdacs.ucsd.edu/~icc/index.php).

2) In the Additional account section, you can find your remote access username. For example, my account user name is called `cs15lfa22fw`.

3) After figuring out your username, you have to set a new password for these additional accounts. You do so by clicking on the hot link that says “change your password” right below the Account Lookup Result. (It can take up to an hour for your password to start working) Make sure when you use "ssh" command you have to include the domain which is `@ieng6.ucsd.edu`.
![Image](CSE15L_Images\LabReport1-2.png)
![Image](CSE15L_Images\LabReport1-3.png)
![Image](CSE15L_Images\LabReport1-4.png)
## **Trying Some Commands**
1) After successfuly connecting into the school's server computer, you can start trying different commands. For example, command "cd" allows you to change directory; command "ls" allows you to see the list of all the files and folders in the directory you are currently at.

2) You can also create a new java project in your directory and have it compile and run using the terminal command line. For example, I created a java project that output the name of the operation system, the user's name, the user's home directory.
![Image](CSE15L_Images\LabReport1-5.png)
## **Moving Files with "scp"**
1) During your time at UCSD, you are going to be making a lot of new programming projects. Most of them you are going to be working at your own home, on your own computer. What happened if you want to copy those programs onto the server computers, so maybe your tutor can try to run it?

2) "scp" is the command that allows you to copy the file that you want onto the directory on the server's computer. For example, the java project I created earlier was made on my computer. I can move it to the server's computer by using the "scp" command.

3) Moving files onto the servers require access to the server which requires your password. Now you can compile and run your program from the server's computer.
![Image](CSE15L_Images\LabReport1-6.png)
## **Setting An SSH Key**
1) It can be annoying if you have to keep inputting your password to log into the server's computer. In some cases when you have bad wifi that keeps disconnecting you, it can become frustrating. We can make it better by creating a log in key that holds your password that respond to your account which eliminate the typing your password process.

2) First you have to generate a pair of keys using the command `ssh-keygen`, the terminal will says it is generating public/private rsa key pair, then it will ask you to enter file in which to save the key. For that you just have to press enter, it will save that pair of key to the default path at **/Users/user.name/.ssh/id_rsa**. Next, it will ask you to set a passphrase, you can choose to set a passphrase, but I chose to have an empty passphrase, so I just pressed enter. You have to enter your passphrase to confirm setting your passphrase. Finally, it will automatically generate your keys.

![Image](CSE15L_Images\LabReport1-7.png)

3) The next step is copying the public key into a directory on the server's computer. However, we have to create a new directory in the server's computer first. We do that by logging into the server and then use the command `mkdir .ssh`. Then you want to use command `exit` to log back out to your computer. Finally, you will use this specific command `scp /Users/<user.name>/.ssh/id_rsa.pub cs15lfa22<last 2 character>@ieng6.ucsd.edu:~/.ssh/authorized_keys` to copy the public key onto the key directory on your server's computer.

4) Once you are done, you will be able bypass the password process to log into your server's computer.
![Image](CSE15L_Images\LabReport1-8.png)
## **Optimizing Remote Running**
1) First of all, if you have reached this step, then I want to congrats you on successfully setting up your account. You can now freely connect to the supercomputer and use it to compile and run any program you want. This part is only a small tip that I can give you to save you some time while you are using terminal.

2) First tip is that you can combine multiple commands at a time. For example, you want to compile and run a program in a different directory, you can combine all three commands "cp", "javac", and "java" separated by a "semi-colon(;)".
![Image](CSE15L_Images\LabReport1-9.png)

3) The last tip I have is that you if you want to use a command you have used recently, you can press the up arrow on your keyboard and you can browse through the list of commands you have used in the past. This tip will save you a lot of time in the long run

---
# *Thank you and Good luck*