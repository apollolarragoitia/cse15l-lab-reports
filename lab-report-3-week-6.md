# Lab Report 3 - Copying Whole Directories with SCP -R

## Step 1 - Copying markdown-parse To ieng6

![image](lab-report-3-images/screenshot1.png)

In order to copy the markdown-parse directory into ieng6, the directory must first be accessed in terminal. This can be done by using cd, and verified using pwd and ls to verify both the path and contents of the directory. Once the current directory is verified, we can copy the entirty of the markdown-parse directory into an ieng6 account using the following command.

`$ scp -r . cs15lwi22aay@ieng6.ucsd.edu:~/markdown-parse`

This tells the terminal to recurssively copy the current directory, which is markdown-parse into the directory markdown-parse on the server `cs15lwi22aay@ieng6.ucsd.edu.` If the directory of markdown-parse does not exist on the server, it will create the directory and the local directory into th remote directory. The name of the directory on the server is indepdent of the directory being copied, meaning we can change the name of the directory on the remote server to be anything.

Upon executing the command to copy the directory, the terminal will print the following, showing the status of
the files being copied.

![image](lab-report-3-images/screeshot2.png).

Once the files are done copying, we can verify this by accessing the ieng6 account and inspecting the directory of markdown-parse. This can be done by doing the following command `ssh cs15lwi22aay@ieng6.ucsd.edu "ls markdown-parse"`. This connects to the ieng6 server and then list the contents of directory markdown-parse.
![image](lab-report-3-images/screenshot3.png).

## Step 2 - Compiling and Running markdown-parse

Once the directory of markdown-parse is on the ieng6 server, the contents of the directory can be compiled by connecting to the ieng6 server through `ssh cs15lwi22aay@ieng6.ucsd.edu`, accessing the markdown-parse directory with `cd markdown-parse` and compiling and executing MarkdownParse.java and MarkdownParseTest.java.

![image](lab-report-3-images/acess.png)
Accessing the markdown-parse directory.




This is done by using `javac MarkdownParse.java` to compile the MarkdownParse.java file. Since then MarkdownParseTest.java uses the jUnit library, the following command must be executed to first compile it: 
`javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar MarkdownParseTest.java`
and then run int using 
`java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest`

![image](lab-report-3-images/compile.png)
Compiling and executing the MarkdownParseTest.

## 








