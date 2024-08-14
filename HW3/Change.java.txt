
class Change{

    public static boolean change(int [] coins, int n)
    {
        boolean ans = false;
        ans = change(coins, n, 0);
        return ans;
    }
    
    public static boolean change(int [] coins, int n, int i)
    {
        boolean ans = false;
        if (n == 0)
        {
        	ans = true;
        }
        else if ((n < 0) | (i >= coins.length))
        {
        	ans = false;
        }
        else
        {   
        	ans = change(coins,n-coins[i],i) || change(coins,n-coins[i],i + 1);
        }      
        return ans;
    }

	public static boolean changeLimited(int[] coins, int n, int numOfCoinsToUse)
	{
        boolean ans = false;
        ans = changeLimited(coins, n, numOfCoinsToUse, 0);
        return ans;
	}
	
	public static boolean changeLimited(int[] coins, int n, int numOfCoinsToUse, int count)
	{
        boolean ans = false;
        if (n == 0 & count <= numOfCoinsToUse)
        {
        	ans = true;
        }
        else if (n < 0 | count > numOfCoinsToUse) 
        {
        	ans = false;
        }
        else
        {   
        	for(int j : coins)
        	{
        		if (changeLimited(coins,n-j,numOfCoinsToUse,count + 1)) {ans = true;}
        	}
        }      
        return ans;
	}

    public static void printChangeLimited(int[] coins, int n, int numOfCoinsToUse)
    {
    	boolean[] array = {true};
     	printChangeLimited(coins, n, numOfCoinsToUse, 0, "", array);  
    }
    
    public static void printChangeLimited(int[] coins, int n, int numOfCoinsToUse, int count, String acc, boolean[] toContinue)
    {
        if (n == 0 & count <= numOfCoinsToUse)
        {
        	if (toContinue[0]) {System.out.println(acc.substring(0, acc.length()-1)); toContinue[0] = false;}
        }
        else
        {   
        	for(int j : coins)
        	{
        		if (!(n < 0 | count > numOfCoinsToUse))
        		{
        			printChangeLimited(coins,n-j,numOfCoinsToUse,count + 1,acc + j + ",", toContinue);
        		}
        	}
        }
    }

    public static int countChangeLimited(int[] coins, int n, int numOfCoinsToUse)
    {
    	int[] options = {0};
        countChangeLimited(coins, n, numOfCoinsToUse, options,coins[0]);
        return options[0];
    }
      
    public static void countChangeLimited(int[] coins, int n, int numOfCoinsToUse, int[] options, int value)
    {     
        if (n == 0 & numOfCoinsToUse >= 0)
        {
        	options[0] = options[0] + 1;
        }
        else
        {          	
        	for (int i = 0; i < coins.length; i++)
        	{
        		if ((!(n < 0 | numOfCoinsToUse < 0) & (value <= coins[i])))
        		{
        			countChangeLimited(coins,n-coins[i],numOfCoinsToUse - 1,options,coins[i]);
        		}
        	}
        }      
    }

    public static void printAllChangeLimited(int[] coins, int n, int numOfCoinsToUse)
    {  	
    	printAllChangeLimited(coins, n, numOfCoinsToUse,"",coins[0]);
    }
       
    public static void printAllChangeLimited(int[] coins, int n, int numOfCoinsToUse, String acc, int value)
    {
        if (n == 0 & numOfCoinsToUse >= 0)
        {
        	System.out.println(acc.substring(0, acc.length()-1));
        }
        else
        {   
           	for (int i = 0; i < coins.length; i++)
        	{
        		if ((!(n < 0 | numOfCoinsToUse < 0) & (value <= coins[i])))
        		{
        			printAllChangeLimited(coins,n-coins[i],numOfCoinsToUse - 1,acc + coins[i] + ",",coins[i]);
        		}
        	}
        }
    }
}

