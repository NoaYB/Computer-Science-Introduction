
import java.math.BigInteger;
import java.util.Random;

class Assignment3BigInteger{

    public static BigInteger sumSmaller(BigInteger n)
    {
        BigInteger sum =  new BigInteger("0");
        BigInteger currentNumber =  new BigInteger("1");
        while (currentNumber.compareTo(n) == -1)
        {
        	sum = sum.add(currentNumber);
        	currentNumber = currentNumber.add(BigInteger.ONE);
        }     
        return sum;
    }

    public static void printRandoms(int n)
    {
    	Random rnd = new Random();
    	for (int i = 0; i < n; i++)
    	{
    		System.out.println(rnd.nextInt());
    	}
    }

    public static boolean isPrime(BigInteger n)
    {
        boolean ans= true;
        if ((n.compareTo(BigInteger.ONE) == 0) | (n.compareTo(BigInteger.ZERO) == 0))
        {
        	ans = false;
        }
        BigInteger currentNumber = new BigInteger("2");
        while(ans & currentNumber.compareTo(n) == -1)
        {
        	if ((n.mod(currentNumber)).compareTo(BigInteger.ZERO) == 0)
        	{
        		ans = false;
        	}
        	currentNumber = currentNumber.add(BigInteger.ONE);
        }
        return ans;
    }

    public static BigInteger randomPrime(int n)
    {
    	Random rnd = new Random();
        BigInteger randBig = new BigInteger(n,rnd);
        while (!isPrime(randBig))
        {
        	randBig = new BigInteger(n,rnd);
        }
        return randBig;
    }

}