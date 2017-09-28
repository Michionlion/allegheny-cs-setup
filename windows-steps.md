# Software Installation Guide for Windows
## Department of Computer Science, Allegheny College

To install Git, do GIT STEPS
To install Java, do JAVA STEPS
To install Gradle, do GRADLE STEPS
To install Travis CI, do RUBY STEPS then TRAVIS-CI STEPS
To install Python, do PYTHON STEPS
To install R, do R STEPS

Students in CS111 should install Java, Git, Gradle, and Travis CI in that order. Other classes should install the relevant modules that are in use in that class.


### JAVA STEPS
##### DOWNLOAD
Download [Java SE JDK 9](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
Make sure to select the correct version for Windows.

##### INSTALL
Execute the exe file that was downloaded previously, and click through the options. You can choose all defaults, or customize it to your liking - be sure to remember any directory changes for the next step!

To test that this step was completed successfully, open a command prompt (search `cmd`), and execute `java -version`. If `java version "9"` is printed (perhaps along with some other stuff), you have completed this step. If not, ask for help.


##### ENVIRONMENT VARIABLES
Right-click on Start, then select "System", then in the upper left of the window that appears select System info. In the window that appears, select Advanced system settings. In the window that appears choose "Environment Variables" on the bottom right. In the window that appears, click "New" below the bottom scroll box. Enter JAVA_HOME as the variable name, and browse to where the java jdk was installed (default: `C:\Program Files\Java\jdk-9`). Select OK. Now find the entry with Variable name "Path" in the lower scroll box. Select it, and press "Edit". Click "New", and write `%JAVA_HOME%\bin`. Select OK until the windows close.

To test that this step was completed successfully, open a command prompt (search `cmd`), and execute `javac -version`. If `javac 9` is printed, you have completed this step. If not, ask for help.

### GIT STEPS
##### DOWNLOAD
Download [Git](https://git-scm.com/download/win)


##### INSTALL
Execute the exe file that was downloaded previously.
Ensure that you select `Git Bash Here`, `Git LFS (Large File Support)`, and both options starting with `Associate`. Other options are optional.

In the next step, choose either `Use Git from Git Bash only` or `Use Git from Windows Command Prompt`. These do exactly as they say.

In the following steps, the defaults should be chosen unless you understand the implications.

To test that this step was completed successfully, right-click on your desktop and select `Git Bash Here`. Then, in the terminal that appears, type `git --version`. If `git version 2.14.2.windows.1` is printed, you have completed this step. If not, ask for help.

### GRADLE STEPS



### RUBY STEPS

### TRAVIS-CI STEPS

### PYTHON STEPS

### R STEPS