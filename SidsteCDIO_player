package cdio1;

public class Player 

{

	private int score;
	private boolean First12;
	
//Konstruktør
public Player()
{
	score = 0;
}
// Henter scoren
public int getScore()
{
	int result = this.score;
	return result;
}
//Gets First12
public boolean getFirst12()
{
	boolean result = this.First12;
	return result;
}
//Sets First12 to true or false
public void setFirst12(boolean set)
{
	this.First12 = set;
}
// Tilføjer en værdi til spillerens score
public void addScore(int score)
{
	this.score = this.score + score;
	if (this.score >= 40)
		{this.score = 40;}
}
// Nulstil scoren
public void resetScore()
{
	score = 0;
}

//Printer den nuværende score som én string
public String scoreString()
{
int result = this.score;
return "" + result + "";
}
}
