# Lab report 1
## **Installing VSCode**
1) First, you go to this website https://code.visualstudio.com/ to download and install VSCode on your computer.
2) If you are using the windows operating system then you should download the version for windows, if you are using Mac then you should download the version for Mac OS.
3) After you have finished downloading, you can start the installation process. You can click next on everything.
![Image](LabReport1-1.png)
## **Remotely Connecting**
1) Before you go on with this step, you first have to figure out your username for the remote access, you can find this out by going to this website https://sdacs.ucsd.edu/~icc/index.php.
2) In the Additional account section, you can find your remote access username. For example, my account user name is called `cs15lfa22fw`.
3) After figuring out your username, you have to set a new password for these additional accounts. You do so by clicking on the hot link that says “change your password” right below the Account Lookup Result. (It can take up to an hour for your password to start working) Make sure when you use "ssh" command you have to include the domain which is `@ieng6.ucsd.edu`.
![Image](CSE15L_Images\LabReport1-2.png)
![Image](CSE15L_Images\LabReport1-3.png)
![Image](CSE15L_Images\LabReport1-4.png)
## **Trying Some Commands**
1) After successfuly connecting into the school's server computer, you can start trying different commands. For example, command "cd" allows you to change directory; command "ls" allows you to see the list of all the files and folders in the directory you are currently at.
2) You can also create a new java project in your directory and have it compile and run using the terminal command line. For example, I created a java project that output the name of the operation system, the user's name, the user's home directory.
![Image](CSE15L_Images\LabReport1-5.png)
## **Moving Files with `scp`**
1) During your time at UCSD, you are going to be making a lot of new programming projects. Most of them you are going to be working at your own home, on your own computer. What happened if you want to copy those programs onto the server computers, so maybe your tutor can try to run it?
2) "scp" is the command that allows you to copy the file that you want onto the directory on the server's computer. For example, the java project I created earlier was made on my computer. I can move it to the server's computer by using the "scp" command.
3) Moving files onto the servers require access to the server which requires your password. Now you can compile and run your program from the server's computer.
![Image](CSE15L_Images\LabReport1-6.png)
## **Setting An SSH Key**
1) It can be annoying if you have to keep inputting your password to log into the server's computer. In some cases when you have bad wifi that keeps disconnecting you, it can become frustrating. We can make it better by creating a log in key that holds your password that respond to your account which eliminate the typing your password process.
2) First you have to 