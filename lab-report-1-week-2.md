# Lab Report 1 - Logging Into A Course Specific Account

## Preface
The fllowing

## Part 1 - Installing Visual Studio Code

When going about installing Visual Studio Code (VSC), the simplest manner is to download the installer found at https://code.visualstudio.com/ and follow the on-screen instructions. For most, the version suggested by the Visual Studio Code website will be the appropiate version. In cases such as mine, where the version suggested is not the most optimal or appropiate for your system, other versions of Visual Studio Code that best match your working environment/setup can be found at https://code.visualstudio.com/#alt-downloads. In my case, I ended up downloading the Mac Apple Sillicon version for most optimized experience given my working environment.

![Image](lab-report-1-images/vscode.png)

//SHOW PIC OF VS CODE

## Part 2A - Setting up your course-specific accont for remote connection.

If this is your first time utilizing your course-specific account, you must first look up your account and then activate it. The account look up tool can be found [here](https://sdacs.ucsd.edu/~icc/index.php). Once on the page, input your UC San Diego username and Student ID in the first two fields respectively. Once in, you will be shown a menu showing all available course specific accounts.
![Image](lab-report-1-images/account1.jpg)
 Click on the respective course account you are trying to activate. This will open a page that displays your course-specific account username alongside a prompt to reset your password in a yellow box if your account has not been activated. To activate your account, simply follow the steps in the prompt.
![Image](lab-report-1-images/account2.png)


## PART 2B - REMOTELY CONNECTING TO STUDENT ACCOUNT

Prior to remotely connecting to your student account, if you are using a Microsoft Windows based workstation, you must install [OpenSSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse) to enable to remote connection. This step is not necessary for Mac or Linux users. 

Once the terminal is open, you can connecect remotely to your CSE course specific account by running the following command, where X is your student username fromthe previous account.

```
$ ssh x@ieng6.ucsd.edu

```

For example:
```
$ ssh cs15lwi22@ieng6.ucsd.edu
```

A prompt will then appear, claiming that the authenticity of the host cannot be found. Type yes to proceed. You will then be prompted for the password you set for the account in Step 2A. Enter the password set to continue. Once you are succesfully connected, you will a see a terminal similar to this one. 
![Image](lab-report-1-images/terminal.png)

Congratulations, you have connected to a remote location succesfully! 

## PART 3 - TRYING SOME COMMANDS

Once connected to the remote server, you can now run commands on the server. Try some of the following commands to get acquainted with the terminal

```
ls > Lists files within the current directory

pwd > Prints the path to your current working directory

whoami > Returns information regarding your current log in session.

ls -lat > Returns a detailed breakdown for files within the current directory. 

exit > Logs you out of the remote server
```
![Image](lab-report-1-images/runningcommands.png)

## PART 4 - Moving Files with scp

One of the most noticable features of having a remote server to be able to connect too is to be able to host files on that remote server and execute/run those files.