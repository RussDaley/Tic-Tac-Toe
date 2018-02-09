# Tic-Tac-Toe #

My version of the age old game tic-tac-toe


///--------------------------------------------V2---------------------------------------------///
Decided to Take Jarids Challenge and Create an AI. I started out with a simple AI that would choose a random box number between 0 and 8
This version works well.

v2.1
	I took the randomized AI code from v2 and tried to put logic in it, so the computer would think of possible wins before it chooses a number.
	this version was a failure the AI wasn't good at finding or selecting the correct possible wins

v2.2
	was a bit better, the AI would know what tiles to choose for to win, but if there was ever a point durning a match where there was no possible wins, AI was a poor sport and GAVE UP. I couldn't correct this behavior mainly due to messy code

OVERALL v2 has messy code, Creating v3....

///--------------------------------------------V3---------------------------------------------///
I need to create a click function that has the complicated logic deciding which final number the AI is will be choosing But multiple functions that are simple. ie. the turns function shouldn't have the logic in it

V3
	Decided to make this version very specific, such as the User will always start. One thing I have run into is trying to determine when the board is completely filled. for now I'm using a turns count, I would like to find a better way to do this. need to start on creating the logic for the AI choice.
	For the AI to choose a good box number i need to factor in:
		1.What the AI has already choosen.
		2.What the user chooses.
		3.If at any time AI has 2 boxes in a row that are already filled to take the 3rd and win.
	SUCCESS!! AI Thinks throught the above 3 factors, as so:
		1.The first box AI chooses is at random, but after that it thinks through combinations that would equal a win, and chooses from that list.
		2.When the User takes a number the AI will mark combinations that are no longer possible to win with.
		3.AI will win(on purpose, not at random) AND wont be a poor sport(like in V2.2) if User blocks AI's win.
	I'm leaving V3 as is, for a back up and reference file.
	COMP DOESN'T DETECT A WINNER

V3.1
	Implimented the checkForWinners. Which I needed to create an if statement specific to the AI's turn.
	Removed the turns counter. but also had to put another if stagement into the AI's turn...Maybe figure out a way to make things cleaner.
	AI successfully blocks the user if there are two X in a row. AI first looks for possible instant wins if there are none then the AI will block the User. Also i found that if the AI had no possible wins It would straight away choose a random nubmer instead of first looking to block the User. So i put some logic there as well to first block the user but if no possible block exsit then choose a random number.




IDEAS instead of making the first box AI chooses random...make it straght away block the user.(Impossible Version.)
	Delay AI
	Alternate turns

///--------------------------------------------V4---------------------------------------------///
This will be the appealing UI

V4
	Functionality is based off of V3.1
	For some reason the Startover button is making the AI loose it's thought process. after the startover button is click the AI wont block the User. (After testing it more i cant seem to see where the AI is making a wrong move. Maybe it's working just fine)
