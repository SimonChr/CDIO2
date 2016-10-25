package cdio1;

public class Dice 

{
	private final int MAX = 6; 	// maximum øjne værdi
	private static int faceValue; // nuværende øjne værdi

	// Konstruktør
	public Dice()	
	{
		faceValue = 0;
	}

	// Kast terning og returner øjne værdi
	public int roll()	
	{
		faceValue = (int)(Math.random() * MAX) + 1;
	return faceValue;
	}
	
	public int getFaceValue()
	{
		return faceValue;
	}
	public static boolean Equals(int hit)
	{
		boolean result = false;
		if(faceValue == hit)
		{
			result = true;
		}
		return result;
	}	
	public static boolean SnakeEye(int sum)	
	{
		boolean result = false;
		if(sum == 2)
		{
			result = true;
		}
		return result;
	}		
}
