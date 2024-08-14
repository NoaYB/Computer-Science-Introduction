
import java.util.Scanner;

public class Task2 {

    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);
        int ans = 0;

        //---------------write your code BELOW this line only!--------------
        
		//System.out.println("Enter a value for variable a :");
		int a = scanner.nextInt();
		
		//System.out.println("Enter a value for variable b :"); // b >= a
		int b = scanner.nextInt();
		
		int range = (b - a) + 1; // We add 1 to the range because it is a semi-open field
		
		ans = (int) (Math.random() * range) + a; // We add the minimum value (a) to reach the required range
		
        //---------------write your code ABOVE this line only!--------------
		
        System.out.println(ans);
		scanner.close();
    }
}