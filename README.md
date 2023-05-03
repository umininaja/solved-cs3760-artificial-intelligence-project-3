Download Link: https://assignmentchef.com/product/solved-cs3760-artificial-intelligence-project-3
<br>



<h1>Overview</h1>

The goal is to help Pacman navigate a game board and survive the ghosts. The game is a little different then the arcade version:

<ul>

 <li>There is a fixed amount of time your agent has to decide on its move.</li>

 <li>The ghosts always move closer to you (except when they’re scared)</li>

 <li>You get 10 points for eating each food pellet</li>

 <li>Every turn you lose 1 point, so you need to be efficient</li>

 <li>Eating a blue power up gives you 40 turns where the ghosts are scared. You get 200 points for each on you catch. During this time they move away from you at half speed.</li>

 <li>If you clear all of the food pellets you get 500 points and the game ends</li>

 <li>If a ghost catches you, then you lose 500 points and the game ends.</li>

</ul>

If you have cs1graphics, you can watch everything happen using a graphics screen. Otherwise, you can see the game board in text form.

<strong>Files: </strong>The files are available in the class git repo (and also on Moodle). The the course page for instructions on access the git server. The name of this assignment is project3. You should only edit MyPlayer.py and description.txt.

<strong>Grading:      </strong>Each assignment will be graded as follows:

<table width="460">

 <tbody>

  <tr>

   <td width="124">50%</td>

   <td width="336">Performance on final version relative to reference implementation</td>

  </tr>

  <tr>

   <td width="124">30%</td>

   <td width="336">Code quality: correctness, use of AI methods, clarity, etc. this will be based on both the initial and final version</td>

  </tr>

  <tr>

   <td width="124">20%</td>

   <td width="336">Description of algorithm used, why it is effective and the steps to took to improve it</td>

  </tr>

  <tr>

   <td width="124">up to 5% bonus</td>

   <td width="336">Performance relative to your classmates</td>

  </tr>

 </tbody>

</table>




<h1>What to change in MyPlayer.py</h1>

You should carefully go through the code in MyPlayer, you don’t have to worry about the code in the other files. You will be implementing the findMove methods. You can add any helper functions you want and make additions to the constructor.

<h1>Running your program</h1>

In either the Python shell or Idle run Run.py. It will ask you to enter a few parameters and then will run.

<h1>Useful methods</h1>

Player class (which MyPlayer inherits from):

<ul>

 <li>timeRemaining() return True or False depending on whether there is time remaining to determine your move</li>

 <li>setMove(move) sets the move you want to use. You can call this multiple times as you find better move options. If time is up, this does nothing.</li>

</ul>

State class:

<ul>

 <li>getScaredTurnsLeft() returns how many turns are left for the ghosts being scared. 0 if they are not.</li>

 <li>getPlayerPosition() returns (row,col) for the position of the players</li>

 <li>getGhostPositions() return a list of (row,col) positions for all of the ghosts</li>

 <li>getPellets() returns a set of the locations (row,col) of all of the pellets</li>

 <li>getPowerUps() returns a set of the locations (row,col) of all of the power ups</li>

 <li>gameOver() returns true if the game is over</li>

 <li>getScore() returns the score</li>

 <li>getTurn() the current turn of the game</li>

 <li>actions() return a list of the possible actions the player can make from it’s current positions. Possibilities are ’Stay’, ’Left’, ’Right’, ’Up’, ’Down’.</li>

 <li>result(action) returns a new state that is the result of the player taking the given action</li>

 <li>ghostResultDistribution() return a list of (state, probability) pairs. These include all possibilities of where the ghosts may have moved.</li>

</ul>

<ul>

 <li></li>

</ul>