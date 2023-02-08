---
title: Software
layout: default
---

# Software to Install or Configure (and/or update as needed)

Instructions on installing these follow below.

* The latest version of git
* Java 17
* Maven 3.8
* nvm
* Node 16
* npm 8
* Heroku CLI

## Recommmended for Everyone

1. VSCode Text Editor for your local computer

   While Eclipse is a perfectly fine IDE, we recommend using something you may be more likely to see in industry in this course.
   
   We have found that VSCode (a free download for Windows/Mac/Linux) is in the sweet spot between too few features, and too complicated.
  
   If you haven't worked with it before, we suggest you download it and start getting used to it.
   
   What it does for you:
   * Autocompletion
   * Syntax highlighting and checking
   * Automatic import detection
   * Ability to see an entire directory tree at once
   * Search and replace across multiple files
   * and much much more...
   
   Download it here: <https://code.visualstudio.com/download>
  
  
2. Install Java 17 on your local system.  **Please install Java 17**, and NOT Java 8, Java 11, or a preview version of Java 18 or 19.   It won't matter for the `"Hello World"` program in the first week, but when we move on to complex Java applications involving third-party libraries, it will definitely matter.
   
For Mac users, instructions for installing with Homebrew appear below.

## Recommmended for MacOS Users

If you have questions about this section, please attend office hours or email the instructor.

1. Command Line Tools XCode for MacOS, including `git`

   On MacOS, `git` typically gets installed as part of the "Command Line XCode Tools" the first time you ask to use it.  To be sure that `git` is installed,
   try typing:
   
   ```
   git --version
   ```
   
   If it shows something like this, you are good:
   
   ```
   git version 2.24.3 (Apple Git-128)
   ```

   Otherwise, you might get a message that you need to install the XCode Command Line Tools.  In that case, please just follow the instructions given.

2. Brew (package manager)

   For MacOS, we'll be installing several packages for Java and JavaScript (node) development.  
   In many cases, installing those is easier if you *first* install the brew package manager.
   
   To install `brew`, visit <https://brew.sh/> and follow the instructions.
   
3. Java 17
   
   To install Java with homebrew, use:
   
   ```
   brew update
   brew install openjdk@17
   ```
   
   After this command finishes executing, there will be a line printed in the terminal that looks like this:
   ```
   sudo ln -sfn /usr/local/opt/openjdk/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk.jdk
   ```
   
   You will need to find this line in the text outputted by `brew install openjdk@17` and run it in the terminal. It should be near the end of the output. 
  
   The command pasted above **will not work**; it is an example provided so you know what you're looking for. This links the software you just installed with the path **your** computer expects – some macs are different and will have different file structures. That's why you must use the command outputted by `brew install openjdk@17`.

   To check if you now have Java 17, open a new Terminal window and do:

   ```
   java -version
   ```

   If it worked, you should see something like this:

   ```
   # java -version
   openjdk 17.0.1 2021-10-19
   OpenJDK Runtime Environment Homebrew (build 17.0.1+1)
   OpenJDK 64-Bit Server VM Homebrew (build 17.0.1+1, mixed mode, sharing)
   ```

4. Maven

   After installing Java 17, you can use `brew` to install maven:

   ```
   brew update
   brew install maven
   ```

   Or if you already have Maven installed, do this to upgrade your version to the latest one:

   ```
   brew update
   brew upgrade maven
   ```

   Then to check that it is installed, do:

   ```
   mvn --version
   ```

   Be sure that you have Maven version 3.8 or higher, as Java 17 requires this version to work.

4. nvm, Node, and npm

   It is recommended to install Node and npm through Node Version Manager (nvm). The instructions for installing this are the same as those for Linux and WSL users, so please follow the instructions listed there.

   [Install nvm and Node on WSL](https://ucsb-cs156.github.io/topics/windows/windows_wsl.html#install-nvm-and-node-on-wsl)

   [Update npm on WSL](https://ucsb-cs156.github.io/topics/windows/windows_wsl.html#update-npm-on-wsl)

## Recommmended for Windows Users

Install Windows Subsystem for Linux.

It turns out that almost everything in terms of installing software (Java, Maven, Node, etc.) is easier under Linux than under native Windows.
Therefore we strongly suggest that if you have a Windows environment, you install the Windows Subsystem for Linux (WSL) and then follow the 
instructions under Linux/WSL.
   
If you are unable to install WSL because of limitations on your machine, please reach out to the course staff via email. In that case, we will try to find an alternative for you.
 
## Recommended for Ubuntu Linux / WSL Users
 
Instructions for installing Windows Subsystem for Linux (WSL), as well as environment setup instructions for Ubuntu systems, is available here: [https://ucsb-cs156.github.io/topics/windows_wsl/](https://ucsb-cs156.github.io/topics/windows/windows_wsl.html)

Native Ubuntu users (those not using Ubuntu through WSL) can skip the Windows-specific setup and go directly to [Install / Update Git on WSL](https://ucsb-cs156.github.io/topics/windows/windows_wsl.html#install--update-git-on-wsl) and follow all instructions from there on.

The following programs will be installed in the above guide:

* The latest version of git
* Java 17
* Maven 3.8
* nvm
* Node 16
* npm 8
* Heroku CLI

If you're using a Linux distribution that is not Ubuntu (or a similar Debian-based distribution with access to `apt`), the commands listed in the setup guide linked above may not work. The staff cannot provide support on finding equivalent commands for your desired distribution, but community resources such as Stack Overflow can help here.

