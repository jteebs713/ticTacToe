
Game logic:

	
	-Checkout micah's president thing: grab things an object and have arrays inside of the object 
	-only ready Dans when I'm trying to learn how to switch players
	

	make a player constructor
		-include name
		-selected image
		-tile array

	

	make a function:
		-when a player clicks on an tile the image they've selected shows up
		-when a player click on a tile, the index of the tile they clicked gets stored to their array

	make a checkWin function:
		-if player.tile.array length is equal to or greater than 3 check to see if they player has any of the winning combinations:
			
			-Winning combinations-if a specific player has boxes with the following indexes in their tile array player wins:
						**index[0], [1], [2]
						**index[3], [4], [5]
						**index[6], [7], [8]
						**index[0], [3], [6]
						**index[1], [4], [7]
						**index[2], [5], [8]
						**index[0], [4], [8]
						**index[2], [4], [6]



****inHTML
DONE-give the main > section a active-board id
DONE-within the #active-board section make a div with a .game-board class
DONE-within the .game-board div make a div with a class of .board-squares
	**.board-squares div**
		DONE-make an ng-repeat and track by $index
		DONE-make an ng-class 
		DONE-make an ng-click 
		-put {{ $index }} between .board-square divs > < to make sure its counting them all out


-Make a Gameboard 
DONE-create a toggle square function
DONE-create array of SQUARE_STATES with 'unselected'  'x' 'apple'
DONE-create Accompaning classes CSS and input background colors or images
DONE-create a "get square state" function
DONE-declare toggle square above the actual function
DONE-declare  "get square state" above the actual function
DONE-make a for loop for the squares in the gameboard
DONE-return GameBoard
DONE-script js/GameBoard.js to HTML

****playersController
DONE-$inject GameBoard into playersController 
DONE-pass the name of Gameboard factory into PlayerControllerFunc
DONE-create a new active GameBoard with 9 as the parameter ** this.activeBoard = new GameBoard(9);***




***********************************************************initial planning below**********


-Render a game board in the browswer

obj Board
	attr 
		- 9 slots
			3 by 3 
			height
			width
		-make it as a table
		-title
		
	behr
		-registers a click
			- attributes it to a specific player
		-calls() the winner combination




-Switch Turns between X and O (user 1 and user 2)
	
	behavior of the ojbect board

	Obj users: use object constructor
		attr
			-element
		behr
			-squares chosen


-declare a winner if a player gets three in a row, tie/cat's game if its neither
	obj game
		
		attr
			-user 1 and user 2

		behr
			-behavior function(user input)
				-has to have 3 to activate this
				-winner = 3 of a specific users inputs in a row horizontally,
				-winner = 3 of a specific users inputs in a row vertically,
				-ties,
				-lose


-allow for two players to compete on separate devices
	attr-
		user1 & user2

	behr
		-connect users

Create player constructor that as part of the player constructor it will take in an ng-click function that attributes the square to a specific player

USE TWO WAY BINDING!!!*** init stuff in 
==============================================================

<!-- <table> -->
				<!-- <thead>Tic Tac Toe</thead> -->

				<!-- <img ng-src="images/x.png"> -->

			<!-- 	<tbody>
					<tr>
						<td><button ng-repeat="user in gameBoard.player['image']">{{ player.image }}</button></td>
						<td><button ng-repeat="user in gameBoard.player['image']">{{ player.image }}</button></td>
						<td><button ng-repeat="user in gameBoard.player['image']">{{ player.image }}</button></td>
					</tr>
					<tr>
						<td><button ng-repeat="user in gameBoard.player['image']">{{ player.image }}</button></td>
						<td><button ng-repeat="user in gameBoard.player['image']">{{ player.image }}</button></td>
						<td><button ng-repeat="user in gameBoard.player['image']">{{ player.image }}</button></td>
					</tr>
					<tr>
						<td><button ng-repeat="user in gameBoard.player['image']">{{ player.image }}</button></td>
						<td><button ng-repeat="user in gameBoard.player['image']">{{ player.image }}</button></td>
						<td><button ng-repeat="user in gameBoard.player['image']">{{ player.image }}</button></td>
					</tr>
					
				</tbody>

				<tfoot></tfoot>
			</table> -->
					
			

		  <!-- <div>
		  	<input class="addBtn" type="text" ng-model="userName">
		  	<button class="addBtn" ng-click="gameBoard.addPlayer(userName)">Add {{ userName }}</button>
		  </div>
 -->