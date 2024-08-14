
import java.util.Scanner;

public class Task4a {

    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);
        boolean ans = true;

        //---------------write your code BELOW this line only!--------------
        
		//System.out.println("Enter a value for variable n :");
		int n = scanner.nextInt();
		
		int MV = Integer.MAX_VALUE;
		boolean Continue = true;
		int x = 2;
		
		if ((n > 1) & (n <= MV))
		{
			while ((x*x <= n) & (Continue))
			{
				if (n % x == 0)
				{
					ans = false;
					Continue = false;
				}		
				x = x + 1;
			}	
		}

        //---------------write your code ABOVE this line only!--------------

        System.out.println(ans);
		scanner.close();
    }
}