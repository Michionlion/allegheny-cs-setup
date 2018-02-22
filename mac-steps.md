# Software Installation Guide for macOS

## Department of Computer Science, Allegheny College

Please follow the installation instructions for the tools listed under **Everyone** and your specific computer science course. Make sure to install the tools in the order they are listed.

**Everyone**
- [Homebrew](#homebrew)
- [Git](#git)
- A text editor of your choice (I recommend [Atom](https://atom.io/))

**CMPSC 111 and CMPSC 112**
- [Java](#java)
- [Gradle](#gradle)
- [GatorGrader](#gatorgrader)

**CMPSC 103**
- [Serve](#serve)

Students in CS 111 with macOS should install Homebrew, Git, Java, Gradle, and GatorGrader in that order. Other classes should install the relevant modules that are in use in that class. You will almost always want to install Homebrew.

Do not repeat a step if you have already completed it!

### Homebrew<a name="homebrew"></a>

Homebrew is a package manager for macOS. It helps you download programs, such as Gradle, or Ruby.

#### Install

Run the following commands in your terminal window:

```
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
$ brew update
```

### Git<a name="git"></a>

#### Install

Run the following command:

```
$ brew install git
```

#### Usage

##### SSH

You will need to set up a SSH key on your laptop. The following comes from [Github's official guide on SSH keys](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/). Start by running the command:

```
$ ssh-keygen -t rsa -b 4096 -C "your_email_used_to_create_github_account@example.com"
```

Press enter when prompted to enter the file in which to save the key. Press enter twice more when it says to enter a passphrase.

Then, run the command `$ cat ~/.ssh/id_rsa.pub`. This should display your public SSH key. Copy to your clipboard from the `ssh-rsa` to the last letter of your email or machine name at the end. Go to `github.com` and navigate to (upper right hand corner) `Settings > SSH and GPG keys` and press the `New SSH key` button. Give your new SSH key a cool title (e.g. "Maria's Macbook") and paste from your clipboard the SSH key you just copied. Then, press `Add SSH key`.

##### Accessing a Git repository

To clone a repository, go to the repository's page and press `Clone or download`. In the "Clone with SSH" option, copy the repository URL to your clip board. Then, open a terminal and change into the directory you want to store your repository in. Type the following command `$ git clone <GITHUB REPOSITORY URL HERE>`. Now, you can change into the repository and do your usual `git add`, `git commit` and `git push` commands.

### Java<a name="java></a>

You should only do these steps if you do not already have Java installed. To see if Java is installed, run `javac -version` in a terminal. If `java version x` is displayed, where `x` starts with `8`, `1.8`, or any higher version, then you do no need to complete the Java steps, as you already have a JDK installed.

#### Install

Run the following commands:

```
$ brew tap caskroom/cask
$ brew cask install java
```

### Gradle<a name="gradle"></a>

#### Install

Run the following command:

```
$ brew install gradle
```

Then test if it was installed correctly by running `$ gradle --version`. If `Gradle 4.5.1` is printed (perhaps after a few warning messages about Java), you have completed this step. If not, ask for help.

### GatorGrader<a name="gatorgrader"></a>

To run GatorGrader on MacOS, you will need to install Python, gnu-getopt, mdl, and proselint.

#### Install

Run the following commands:

```
$ brew install pyenv
$ echo -e 'eval "$(pyenv init -)"\n' >> ~/.bash_profile
```

Now you should restart your terminal window (&#8984;Q) and run the following commands:

```
$ pyenv install 3.5.4
$ pyenv global 3.5.4
$ brew install gnu-getopt
$ brew link --force gnu-getopt
$ pip install proselint
$ gem install mdl
```

If you encounter permission problems, add `sudo` to the beginning of the command and enter your user password (i.e. the password you use to log into your laptop) when prompted.


### Serve<a name="serve"></a>

In 103, you will use a Ruby gem called, "[Serve](https://github.com/jlong/serve)," to serve your website files. 

#### Install

To install, run:

```
$ gem install serve
$ gem install thin
```

### End

There you go! You are now all set to use your Mac to work on your class assignments. If you get an error when you are trying to use these tools, first try Googling the error. Chances are that you are not the first person to encounter the issue and someone has already asked how to solve it on StackOverflow or the GitHub issue tracker. If you are still stuck, feel free to send Saejin or me (Maria) a message on Slack, or email us at our school emails (`mahlauheinerts@allegheny.edu` or `kimy@allegheny.edu`) if we are not part of any of your Slack teams.

Best of luck in your computer science courses!
