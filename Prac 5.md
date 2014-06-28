Test Plan of Game 2048
======================

Introduction
============
This paper provides a complete test plan for game 2048, as main objective of 2048 game is to rotate game board to
left, right, top, or down direction to move numbers, and if there are two cells have same value they are merged into
one cell with value equals to addition of these two cells values, when board is rotated in any direction a new cell is
added to the board in random place and with value of two or four, the main target of the game is to obtain a cell that
has value equals to 2048.
When user merges cells his/her score incremented by the summation of two merged cells, when game is initially started 
the board has only two cells with value equals two and placed in random places, the game is considered to be over 
when the board is totally full and there is no empty place to add any new cells.

Software Specifications
=======================
-	Java development toolkit version 7
-	Github account and internet connection
-	NetBeans IDE version 7.3


Types of tests that will be performed
=====================================
Unit testing:
-------------
Unit testing is important to test each functionality of the application, JUnit library will be used to perform unit testing
by developing and 
executing JUnit test classed.

Regression Testing:
-------------------
This type of testing ensures that after fixing any bugs/issue while performing unit testing that no other
functionality/feature has a problem, as fixing an issue may lead to a new bug in another function that was previously working
perfectly.

User acceptance testing:
------------------------
User acceptance testing is performed by system end users to make sure that application is developed as per their need, 
and it really mapped to their requirements.

Types of tests that will not be performed
=========================================
Integration Testing:
--------------------
Integration testing is meant to make sure that application under test integrates in proper way with any third party or legacy
systems, this type of testing will not be performed because our application doesn’t integrate with any other systems.

Performance Testing:
--------------------
Performance testing is meant to ensure that application is working fine when large number of users are using it in the same time,
or when a big data is used, this type of testing is no applicable for our application.

Security Testing:
-----------------
Security testing is meant to ensure that all application data is secured and encrypted, also it ensures that only authorized
personals have access to the application; this is not applicable for our application.

Testing scenarios
==================
Game board rendering
---------------------
-	At game start the board should be rendered as grid of four rows and four columns, all cells are initially free, 
only two random cells are populated in random places with value equals to two.

Make sure that user enters a valid input
----------------------------------------
-	User should enter l, r, t, d, or x, any other input is considered as invalid.
-	Application must show an error message to notify user when invalid input is entered.

Handling user input
-------------------
-	Game board should be rotated to the left direction when player enters ‘l’
-	Game board should be rotated to the right direction when player enters ‘r’
-	Game board should be rotated to the top direction when player enters ‘t’
-	Game board should be rotated to the down direction when player enters ‘d’
-	Application should exit when player enters ‘x’

Rotate board to right direction
-------------------------------
-	Cells should not move if there is no free cell in the row
-	Cells should not move if they are all right aligned.
-	If any free cell, all cells at its left should be moved to the right direction
-	All cells should move to the right if the first cell at the right is free

Rotate board to left direction
------------------------------
-	Cells should not move if there is no free cell in the row
-	Cells should not move if they are all left aligned.
-	If any free cell, all cells at its left should be moved to the left direction
-	All cells should move to the left if the first cell at the left is free

Rotate board to top direction
-----------------------------
-	Cells should not move if there is no free cell in the column
-	Cells should not move if they are all top aligned.
-	If any free cell in any column, all cells below it should be moved to the top direction
-	All cells should  be moved to the top if the first cell at the top is free

Rotate board to down direction
------------------------------
-	Cells should not move if there is no free cell in the column
-	Cells should not move if they are all down aligned.
-	If any free cell in any column, all cells above it should be moved to the down direction
-	All cells should  be moved to the down direction if the first cell at the bottom is free

Merge two cells 
----------------
-	If there are two adjacent cells with same value they should be merged into one cell with value equals to summation of
the value of two merged cells.

Player score
------------
-	When game is started the player is initialized as zero.
-	When player merges tow cells, his score should be incremented by the value of summation of two merged cells.

Game over 
---------
-	If there is no more free cell so it is game over, application should notify user with game over message, 
and game is stopped.

Exit the game
--------------
-	If player enters “x” this means that he wants to quit the game, application should notify user that game is over,
and then application is exited.

Out of scope
============
-	Only one player can play the game, no multiplayer option is available for this game. 
-	Application has not settings menu, and no multiple levels.
-	Application is available offline, no networking option and no online option.

Dependencies and risks
======================
Dependencies
------------
-	Run the provided sample game.
-	Be aware of the rules of the game to be developed.

Risks
------
-	Poor or misunderstanding of game rules
-	Student undertakes too much assignments may lead to delay in delivery of this project.
-	Poor time management may lead to late delivery.
