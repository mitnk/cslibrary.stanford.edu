This is the Readme for the Stanford Tetris package --
suitable for playing around with tetris or creating a tetris
based project.

Created by Nick Parlante, nick.parlante@cs.stanford.edu

This package is free and available as article #112 in the
Stanford CS Education Library at http://cslibrary.stanford.edu/112/
This material may be redistributed so long as it is
intact and unmodified.

Materials
	Readme.txt -- this introduction
	JTetris.jar -- a functioning Tetris
	
TetrisProject.zip -- things you need to compile tetris code
	Tetris-Architecture.html -- the architecture of the classes
	TetrisAssignment -- handout for the full assignment
    *.java -- starter files and support files

This Readme introduces the Tetris materials, explains how to
run the program, and gives some assignment ideas.
Tetris-Architecture.html describes the overall design architecture
of the tetris classes. The .java starter files are also
heavily commented.

-------
Running
-------

The provided JTetris.jar contains a runnable Java version of tetris
which supports the brain features (below). The program needs Java 1.2
or later -- the free download from Sun is http://java.sun.com/j2se/1.3/jre/
JTetris.jar can be run by double clicking it, or with the command line
incantation "java -jar JTetris.jar".

JTetris will work work on MacOS 8/9 as well.
Install Java from http://www.apple.com/java/
Download swingall.jar from http://www.stanford.edu/class/cs108/jar/swingall.jar
and install it in: System Folder > Extensions > MRJ Libraries > MRJClasses.
Then download the separate MacJTetris application (you can throw out the
folder created by Stuffit expander).

The program includes a little slider that controls the speed.
The "Brain Active" button will turn on the AI brain to
play for you. The "Adversary" slider uses the AI brain to
figure out which next piece will be hardest for the player (hah!).
Set the adversary slider to 25%, and 25% of the pieces will be
very hard to play instead of being chosen randomly.
It's fun to put the adversary at about 25%, and then ask
a victim to play without telling them about the adversary.
The "Load Brain" button can load in a user-written brain.


--------
Projects
--------

1. Fun: Brain

A fun project that's not too hard is designing a tetris brain.
The code to implement a brain is surprisingly short.
The default brain in JTetris is called LameBrain, and it's
game playing logic is less than a page long.
Writing a brain requires just basic Java and OOP skills.
Look at the Brain.java and LameBrain.java files to get an idea of
how the system works. Write your own subclass of LameBrain and override the
rateBoard() method with your own rating logic.

Run JTetris and use the "Load Brain" button with the name of your class,
such as "MyBrain", to load your brain into JTetris.
By default, Java finds classes that are in the current directory,
so just put your .class file in the same directory as the program so it
will be found when you click the Load Brain button.

See the Tetris-Architecture.html document for ideas on Brain design and some
basic information on how to message the Piece and Board classes.
Designing your own brain is a creative and wide-open sort of challenge.

If you run the program with the command line option "test", then
it will play the same sequence of pieces every time -- seeing the
same sequence of pieces each time makes it easier to interpret
what the brain is doing. (perhaps this should be a control in the GUI.)


2. Hard: The Whole Thing

The obvious tetris project is to implement the whole thing --
most of the work is in the Piece and Board classes which
implement the core tetris logic. The implementation is more
complex than you might think, since it needs to support the
brain efficiently.

It's a pretty difficult project, but it's fun.
We have our 2nd year CS undergraduates do this project.

See the TetrisAssignment.rtf for the assignment handout
we use.

The basic steps are...

a. Read the Tetris-Architecture.html to get a feel for the
overall architecture. Also, the .java files are heavily
commented.

(For each of the following classes, there is a "starter"
file that has some of the basic syntax done for you.)

b. Build the Piece class in Piece.java

c. Build the JPieceTest class in JPieceTest.java.
Use this to test the functionality of your Piece.
(This requires a little understanding of Java drawing.)

d. Build the Board class in Board.java (this is the hardest part)

e. Use the provided JBoardTest class to test your Board implementation

f. Use the provided JTetris class to play tetris using your Piece and Board
implementations.

g. (optional) Implement your own JBrainTetris subclass of JTetris
that combines JTetris with the Brain AI to implement self-playing
tetris and the adversary.

h. (optional) You can also implement your own Brain -- the provided
LameBrain is quite simple.

It's a challenging project, but it's fun once it works.
It's a nice example of using OOP to divide and conquer a
complex system.

Share and Enjoy!


Nick Parlante
nick.parlante@cs.stanford.edu

