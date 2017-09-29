Installing Scala and Apache Spark on Mac OS

Hi! I’m Jose Portilla and I teach over 200,000 students about programming, data
science, and machine learning on Udemy! You can check out all my courses here.

If you’re interested in learning Python for Data Science and Machine learning,
check out my course here. (I also teach Full Stack Web Development with Django!)

Here is a Step by Step guide to installing Scala and Apache Spark on Mac OS Step
1: Get Homebrew

Homebrew makes your life a lot easier when it comes to installing applications
and languages on a Mac OS. You can get homebrew by following the instructions on
it’s website. Which basically just tells you to open your terminal and type:

/usr/bin/ruby -e "$(curl -fsSL
/https://raw.githubusercontent.com/Homebrew/install/master/install)"
/
There are more detailed instructions on installing on the project’s GitHub page.
Installing everything through Homebrew should automatically add all the
appropriate PATH settings to your profile. Step 2: Installing xcode-select

In order to install Java, Scala, and Spark through the command line we will
probably need to install xcode-select and command line developer tools. Go to
you terminal and type:

xcode-select --install

You will get a prompt that looks something like this:

Go ahead and select install. Step 3: Use Homebrew to install Java

Scala is dependent on Java, you may or may not need to install it. The easiest
way to install it is to just use HomeBrew:

In your terminal type:

brew cask install java

You may need to enter your password at some point to complete the java
installation. After running this Homebrew should have taken care of the Java
install. Now we can move on to Scala. Step 4: Use Homebrew to install Scala

Now with Homebrew installed go to your terminal and type:

brew install scala

Step 5: Use Homebrew to install Apache Spark

Now with Scala installed go to your terminal and type:

brew install apache-spark

Homebrew will now download and install Apache Spark, it may take some time
depending on your internet connection. Step 5: Start the Spark Shell

Now try this command:

spark-shell

You should see a flood of text and warnings but eventually see something like
this:

Welcome to 	____              __
     / __/__  ___ _____/ /__
    _\ \/ _ \/ _ `/ __/  '_/
   /___/ .__/\_,_/_/ /_/\_\   version 2.0.1
      /_/
      /
Using Scala version 2.11.8 (Java HotSpot(TM) 64-Bit Server VM, Java 1.8.0_102)
Type in expressions to have them evaluated. Type :help for more information.

scala>

You can confirm that it is working by typing the scala code:

val s = "hello world"

Congratulations! You’re all set up!

Common Issue: Setting PATH in bash.

Homebrew should have taken care of all of this, but in case you need to add
spark to your PATH, you’ll want to use:

export SPARK_HOME=/usr/local/Cellar/apache-spark/2.0.1/libexec export
PYTHONPATH=/usr/local/Cellar/apache-spark/2.0.1/libexec/python/:$PYTHONP$