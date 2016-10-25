package cdio1;

import desktop_resources.GUI;
public class Ui {
	public static void main(String[] args) 

	{
		Dice dice = new Dice();
		Player player1 = new Player();
		Player player2 = new Player();
		int sum = 0;
		
		// Update score in middle of board
		GUI.displayChanceCard("Sum of dice: " + sum + ".    Player 1's score:  " + player1.scoreString() + "\n" + "     Player 2's Score:  " + player2.scoreString());
	
	while(player1.getScore()<= 40 && player2.getScore()<= 40)
	{
		int hit1 = 0;
		int hit2 = 0;
		
		// Player 1's turn *****************************************************
		
		// Create buttons and show turn (Break game)
			GUI.getUserLeftButtonPressed("Player 1's turn", "Hard roll", " Soft roll");
		for (int i=0; i<2; i++)
		{
			dice.roll();
				player1.addScore(dice.getFaceValue());
				if(i==0)
				{
				hit1 = dice.getFaceValue();					
				}
				else
				{
				hit2 = dice.getFaceValue();
				sum = hit1 + hit2;
						
				// Show dice on board
					GUI.setDice(hit1,hit2);
					
				// Update score in middle of board
				GUI.displayChanceCard("Sum of dice: " + sum + ".    Player 1's score:  " + player1.scoreString() + "\n" + "     Player 2's Score:  " + player2.scoreString());

						
				// Snakeeye => reset score
					if(Dice.SnakeEye(sum) == true)
					{
						GUI.displayChanceCard("Player 1's score is reset to 0 for hitting double 1!");
						player1.resetScore();
					}
					// Twice double six win
					
					if(sum == 12)	// Checks for double 6
					{
						if(player1.getFirst12() == true){
							GUI.displayChanceCard("Player 1 wins by hitting double 6 twice");
							GUI.getUserLeftButtonPressed("Player 1 wins!", "End game", "End game");
							System.exit(0);
						}
						else
						{
							player1.setFirst12(true);
						} }
						else 
						{
							player1.setFirst12(false);
						}	
				
				// Equal dice => extra turn
					if(Dice.Equals(hit1) == true)
					{
						
						//Win conditions
						int score1 = Integer.parseInt(player1.scoreString());
						if (score1 == 40)
						{
							GUI.displayChanceCard("Player 1 Wins!");
							GUI.getUserLeftButtonPressed("Player 1 wins!", "End game", "End game");
							System.exit(0); //Ends the game before able to see message !
						}
					i = i - 2 ;
					// Break game and announce extra turn
						GUI.getUserLeftButtonPressed("Player 1 gets an extra turn!", "Hard roll", " Soft roll");
						GUI.displayChanceCard("Sum of dice: " + sum + ".   Player 1's score:  " + player1.scoreString() + "\n" + "     Player 2's Score:  " + player2.scoreString());
					}
					
				}
					
		}
		
				
		// Change of turn to Player 2 *****************************************************
		
		GUI.getUserLeftButtonPressed("Player 2's turn", "Hard roll", " Soft roll");
		for (int i=0; i<2; i++)
		{
		dice.roll();
		player2.addScore(dice.getFaceValue()); // ADd hit to Player 2 score
			if(i==0)
			{
			hit1 = dice.getFaceValue();
			}
			else
			{
				hit2 = dice.getFaceValue();
				 int sum2 = hit1 + hit2;
				
				// Show dice on board
					GUI.setDice(hit1,hit2);
	
				// Update score in middle of board
				GUI.displayChanceCard("Sum of dice: " + sum2 + ".   Player 1's score:  " + player1.scoreString() + "\n" + "     Player 2's Score:  " + player2.scoreString());

				// Snakeeye => resetscore
					if(Dice.SnakeEye(sum2) == true)
					{
						player2.resetScore();
					}
				// Twice double six win
					
					if(sum2 == 12)	// Checks for double 6
					{
						if(player2.getFirst12() == true){
							GUI.displayChanceCard("Player 2 wins by hitting double 6 twice");
							GUI.getUserLeftButtonPressed("Player 2 wins!", "End game", "End game");
							System.exit(0);
						}
						else
						{
							player1.setFirst12(true);
						} }
						else 
						{
							player1.setFirst12(false);
						}
				
				// Equal dice => extra turn
					if(Dice.Equals(hit1) == true)
					{
						GUI.displayChanceCard("Sum of dice: " + sum2 + ".   Player 1's score:  " + player1.scoreString() + "\n" + "     Player 2's Score:  " + player2.scoreString());
						//Win conditions
						int score2 = Integer.parseInt(player2.scoreString());
						if (score2 == 40)
						{
							GUI.displayChanceCard("Player 2 Wins!");
							GUI.getUserLeftButtonPressed("Player 2 wins!", "End game", "End game");
							System.exit(0); //Ends the game before able to see message !
						}
					i = i - 2 ;
					// Break game and announce extra turn
						GUI.getUserLeftButtonPressed("Player 2 gets an extra turn!", "Hard roll", " Soft roll");
					}
			}
					}
		
		
	}	
	}
}
