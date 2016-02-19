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

   FIXME: write something here about how to actually run code safely: firewalls, not on the internet

2. Don't leave this code running when you're not using it.  This limits the
window of opportunity for Project PoopyPants agents to find a way in.

  FIXME: some specific advice here too

# Aquiring the code

We're going to start by using Google Gryere because Project Rainbow
love cheese.

## For Windows

## For Linux

## For Mac OS X

### Open a Terminal

1. Open 'Launchpad'
2. Open or search for 'Terminal' application

### Install Homebrew

1. In terminal type: ```which brew```
2. If you see a path like '/usr/local/bin/brew', then brew is installed on your system and you can skip the next step.
3. If you see nothing when you type 'which brew' then copy and paste the following into a terminal:
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### Install Python

1. In terminal type: 
```which python```
2. If you see a path like '/usr/bin/python', then python is installed on your system and you can skip the next step.
3. If you see nothing when you type 'which python' then copy and paste the following into a terminal:
```
brew install python
```

### Install Wget

1. In terminal type: 
```which wget```
2. If you see a path like '/usr/local/bin/python', then wget is installed on your system and you can skip the next step.
3. If you see nothing when you type 'which wget' then copy and paste the following into a terminal:
```
brew install wget
```

### Install Gruyere

1. In terminal type:
```wget https://google-gruyere.appspot.com/gruyere-code.zip```

```unzip gruyere-code```

```python ./gruyere.py```

2. Your terminal should say:
```
Gruyere started...
http://127.0.0.1:8008/
http://127.0.0.1:8008/###################/
```

Where ################### is your unique ID.

### Open your vulnerable WebApp in a browser

1. Copy the url that looks like http://127.0.0.1:8008/###################/ from your terminal.
2. Type COMMAND + T to open a new Tab
3. In new terminal tab, type:
```open http://127.0.0.1:8008/7041939091716429204/'```
⋅⋅* -OR-
3. Copy & Paste the url into your web browser of choice

### You are ready to earn your Security Gems!
### Go on to [Mission 1]: https://github.com/terriko/sparklesecurity/mission1.md

## Resources
..* HomeBrew (packagemanager for Mac OS X): http://brew.sh
..* Gruyer (Google project page): https://google-gruyere.appspot.com/




