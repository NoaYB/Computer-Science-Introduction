
import java.util.Scanner;

public class Task3a {

    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);
        int ans = 1; // Change the value from 0 to 1 to calculate the square number correctly

        //---------------write your code BELOW this line only!--------------
        
		//System.out.println("Enter a value for variable n :"); // n >= 0
		int n = scanner.nextInt();
		
		for (int i = n; i > 0; i = i - 1)
		{
			ans = ans * 2;
		}
				
        //---------------write your code ABOVE this line only!--------------
		
        System.out.println(ans);
		scanner.close();
    }
}