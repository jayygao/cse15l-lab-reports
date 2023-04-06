# CSE 15L Beginner Tutorial

Welcome to **CSE 15L**, compared to the previous class of either CSE 8B or CSE 11, this course will be drastically different in ways that had been described before during lecture.
## Setting up your account for lab.

* First, head over to the [UCSD Account Lookup](https://sdacs.ucsd.edu/~icc/index.php) and lookup your account.
* Afterwards, you must reset your password for your username that'll you'll be using in the lab, it should start with cs15l... and reset it through the global password change tool that was provided on the site.
* You **MUST** reset your password in order to access the server through VSC terminal in the future.
## Setting up VSC for access.

Simply open up VSC and leave it blank as of now, there is no need to create a new repository at this time

![Image](https://i.ibb.co/gJzG3jy/Screenshot-2023-04-06-094544.png)

**YOU MUST INSTALL GIT IN ORDER TO ACCESS THE REMOTE SERVER THROUGH VSC**
* Listed here is a link to install Git for Windows

[Git](https://gitforwindows.org)
* Install git, then afterwards set your terminal in VSC to utilize git bash, here is a guide

[Guide](https://stackoverflow.com/a/50527994)
* **Note: You can avoid all of this setup work if you simply use the computers provided in the lab, it is much simpler.**
## Connecting

Now, it's finally time to connect. Open up a terminal through VSC and type in the following command

`ssh (your CS15L username)@ieng6.ucsd.edu`

Once logged in, it'll prompt a message regarding something about the authenticity of host... and asking you to continue (yes/no)

Just type yes and proceed lol

It'll now prompt you to type in the password, this is important as we had just resetted our password for our CSE15L account, use the new password and type it in. Allow the terminal to work its magic. 

After it has finished setting up, your terminal should look something like this.

![Image](https://i.ibb.co/6gWDjzp/Screenshot-2023-04-06-093659.png)

**We are now connected!**

If things did not work out this smoothly reach out for help because I was fine setting up. Your problem not mine lol.

## Running commands

There are quite a lot of commands to use, I believed to have derived from linux.

Here are a few:
* `cd ~ `
* `cd (directory nname) `
* `ls`
* `ls (directory)`
* `cat (file)`
* `pwd`
* `cp (file)(directory path)`

Here is an output of the commands I ran and what it had for outputs.
![Image](https://i.ibb.co/s6wk97z/Screenshot-2023-04-06-094947.png)
![Image](https://i.ibb.co/rZfnnWR/Screenshot-2023-04-06-095004.png)

Play with this a little bit, and when you are done, type exit into the terminal and you'll logout of the remote access.
