
import java.util.Scanner;

public class Task4b {

    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);
        int ans = 0;

        //---------------write your code BELOW this line only!--------------
        
		//System.out.println("Enter a value for variable n :");
		int n = scanner.nextInt();
			
		int count = 0;
		
		for (int i = n; i > 1; i = i - 1)
		{
			int x = 2;
			boolean isPrime = true;
			
			while ((x <= i) & (isPrime))
			{
				if ((i % x == 0) & (i != x))
				{
					isPrime = false;
				}
				
				x = x + 1;
			}
			
			if (isPrime) {count = count + 1;}
		}
		
		ans = count;
						        	
        //---------------write your code ABOVE this line only!--------------
		
        System.out.println(ans);    
		scanner.close();    
    }
}