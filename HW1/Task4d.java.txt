
import java.util.Scanner;

public class Task4d {

    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);
        int ans1 = 0;
        int ans2 = 0;

        //---------------write your code BELOW this line only!--------------
              
		//System.out.println("Enter a value for variable n :"); 
		int n = scanner.nextInt();
		boolean Continue = true;
		      
        if (n > 1)
        {
        	int d = 1;
        	int s = 1;
        	int TwoPowerS = 1;
        	       	
        	while(Continue) // Finds the values d and s
        	{
        		TwoPowerS = TwoPowerS * 2;
        		d = (n - 1) / TwoPowerS;
        		if (d % 2 == 1) {Continue = false;}
        		if (Continue) {s = s + 1;}
        	}
        	ans1 = s;
        	ans2 = d;
        }

        //---------------write your code ABOVE this line only!--------------
   
        System.out.println(ans1);
        System.out.println(ans2);
		scanner.close();
    }
}