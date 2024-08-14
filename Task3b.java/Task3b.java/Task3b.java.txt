
import java.util.Scanner;

public class Task3b {

    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);
        int ans = 0;

        //---------------write your code BELOW this line only!--------------
        
		//System.out.println("Enter a value for variable n :");
		int n = scanner.nextInt();
		
		//System.out.println("Enter a value for variable k :"); // (k > 1) & (k < MVsqrt2)
		int k = scanner.nextInt();
				
		int count = n;
		int sum = 0;
		
		if (n > 1)
		{	
			sum = 1;
			while (count > 0) // Finding the value of (2^n) % k
			{
				sum = sum * 2;
				if (sum > k) {sum = sum % k;}
				count = count - 1;
			}
		}
		
		ans = sum;
			
        //---------------write your code ABOVE this line only!--------------
		
        System.out.println(ans);
		scanner.close();
    }
}