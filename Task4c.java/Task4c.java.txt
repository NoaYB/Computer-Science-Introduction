
import java.util.Scanner;

public class Task4c {

    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);
        int ans = 0;

        //---------------write your code BELOW this line only!--------------
              
		//System.out.println("Enter a value for variable n :");
		int n = scanner.nextInt();
		                         
        if (n > 1)
        {
			int range = ((n - 1) - 2) + 1; // We add 1 to the range because it is a semi-open field
			int b = (int) (Math.random() * range) + 2; // We add the minimum value (2) to reach the required range			       	
        	ans = b;      	
        }

        //---------------write your code ABOVE this line only!--------------
        
        System.out.println(ans);
		scanner.close();
    }
}