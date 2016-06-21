# Sparkle Security Mission 0: Opsec and setup

This mission is intended to help you find and set up a vulnerable web
application to play with.

# Introduction

Agent Sparkle, you have been recruited as a security expert to use your skills
to protect the kingdom of Project Rainbow.  You might not feel qualified yet,
but Project Rainbow has great faith in your ability to learn.

# Sparkle Opsec

Before we start downloading vulnerable applications for training, Agent
Sparkle, you need to know a bit about OpSec.  "OpSec" is short-form for
"operational security."  Wikipedia defines it like this:

"Operations security (OPSEC) is a term originating in U.S. military jargon, as
a process that identifies critical information to determine if friendly actions
can be observed by enemy intelligence, determines if information obtained by
adversaries could be interpreted to be useful to them, and then executes
selected measures that eliminate or reduce adversary exploitation of friendly
critical information."

![SECURITY RULES!](http://www.quickmeme.com/img/e0/e0ab7d30d57972802de828fe13459fb3bdac3b61496ea58988f6d4c038f32b9f.jpg "Security Rules!")

That might seem like a big mouthful, but the important part of opsec right now
is that we want to make sure that you and your computer stay safe while you
work on building skills. The agents of Project PoopyPants are determined to
derail your training so that Project Rainbow won't succeed!

Remember, Agent Sparkle, that the code you are running will be vulnerable to
people other than you.  That means Project PoopyPants agents could use this
code to get to you.  Don't let that happen!

1. Make sure other people don't gain access.
	You don't want Project PoopyPants's agents to catch you while
   you're learning.

	Gruyere already has some built in protections: it only accepts local input and it has a "magic" url that would be hard for a dangerous agent to guess. But you, Agent Sparkle, can supplement this with other ways to keep PoopyPants out: the easiest way is to just disconnect from the internet when you're using Gruyere.  There's also lots of technologies to help you run unsafe code more safely: you might want to search for "firewalls" or "sandboxing" if you want to start learning about those.

2. Don't leave this code running when you're not using it.  This limits the
window of opportunity for Project PoopyPants agents to find a way in.

	It's often good to use many layers of security: think of it like a car.  You wear your seatbelt, but cars also have crumple zones and air bags to help protect you.  This is often called "defense in depth" and it's too big a topic for today, but remember that it's worth using more than one way to keep yourself safe!


# Acquiring the code

We're going to start by using Google Gruyere because Project Rainbow
loves cheese.

## For Windows
### Get Python
If you don't already have a copy of Python on your Windows machine, you can download one here:

(https://www.python.org/downloads/windows/)

Gruyere has been better tested on Python 2.7 so that is probably the choice of least resistence.

### Get Gruyere

You can download gruyere using your web browser: (https://google-gruyere.appspot.com/gruyere-code.zip)

Unzip the file into an appropriate directory, and run the "gruyere.py" script. Not sure how to do that?  [Here's a tutorial on running a python script](http://pythoncentral.io/execute-python-script-file-shell/). It includes windows instructions at the top of the page.

Your terminal should say
```
Gruyere started...

http://127.0.0.1:8008/

http://127.0.0.1:8008/###################/
```
* Where ################### is your Magic Number.

### Open your vulnerable WebApp in a browser

* Copy the url that looks like http://127.0.0.1:8008/###################/ from your terminal.
* Open up that vulnerable WebApp in the browser of your choice.

## For Linux Ubuntu
### Open a Terminal

* Open or search for 'Terminal' application

### Update list of packages

* In terminal type: 
```
sudo apt-get update
```

### Install Python

* In terminal type: 
```
which python
```
* If you see a path like '/usr/bin/python', then python is installed on your system and you can skip the next step.
* If you see nothing when you type 'which python' then copy and paste the following into a terminal:
```
sudo apt-get install python
```

### Install Wget

* In terminal type: 
```
which wget
```
* If you see a path like '/usr/bin/python', then wget is installed on your system and you can skip the next step.
* If you see nothing when you type 'which wget' then copy and paste the following into a terminal:
```
sudo apt-get install wget
```

### Install Gruyere and Get Your Magic Number

* In terminal type:
```
mkdir gruyere-code

cd gruyere-code 

wget https://google-gruyere.appspot.com/gruyere-code.zip

unzip gruyere-code
```
### Open a new tab before running Gruyere
* Type CTRL + SHIFT + T to open a new Tab
* In the old terminal tab type: 
```
python ./gruyere.py
```
* Your terminal should say:
```
Gruyere started...

http://127.0.0.1:8008/

http://127.0.0.1:8008/###################/
```
* Where ################### is your Magic Number.

### Open your vulnerable WebApp in a browser

* Copy the url that looks like http://127.0.0.1:8008/###################/ from your terminal.
* In new terminal tab, type:
```
firefox http://127.0.0.1:8008/###################/'
```

OR 

* Copy & Paste the url into your web browser of choice

### Resources
* HomeBrew (packagemanager for Mac OS X): http://brew.sh
* Gruyere (Google project page): https://google-gruyere.appspot.com/

## For Mac OS X

### Open a Terminal

* Open 'Launchpad'
* Open or search for 'Terminal' application

### Install Homebrew

* In terminal type: 
```
which brew
```
* If you see a path like '/usr/local/bin/brew', then brew is installed on your system and you can skip the next step.
* If you see nothing when you type 'which brew' then copy and paste the following into a terminal:
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### Install Python

* In terminal type: 
```
which python
```
* If you see a path like `/usr/bin/python`, then python is installed on your system and you can skip the next step.
* If you see nothing when you type `which python` then copy and paste the following into a terminal:
```
brew install python
```

### Install Wget

* In terminal type: 
```
which wget
```
* If you see a path like `/usr/local/bin/python`, then wget is installed on your system and you can skip the next step.
* If you see nothing when you type `which wget` then copy and paste the following into a terminal:
```
brew install wget
```

### Install Gruyere and Get Your Magic Number

* In terminal type:
```
mkdir gruyere-code

cd gruyere-code

wget https://google-gruyere.appspot.com/gruyere-code.zip

unzip gruyere-code

python ./gruyere.py
```
* Your terminal should say:
```
Gruyere started...

http://127.0.0.1:8008/

http://127.0.0.1:8008/###################/
```
* Where ################### is your Magic Number.

### Open your vulnerable WebApp in a browser

* Copy the url that looks like http://127.0.0.1:8008/###################/ from your terminal.
* Type COMMAND + T to open a new Tab
* In new terminal tab, type:
```
open http://127.0.0.1:8008/###################/'
```

OR 

* Copy & Paste the url into your web browser of choice

### Resources
* HomeBrew (packagemanager for Mac OS X): http://brew.sh
* Gruyere (Google project page): https://google-gruyere.appspot.com/

## You are ready to earn your Security Gems!
![SECURITY GEMS!](http://www.clipartbest.com/cliparts/7ca/Knx/7caKnxMdi.png "Security Gems!")

### Go on to [Mission 1](https://github.com/terriko/sparklesecurity/blob/master/Mission1.md)




