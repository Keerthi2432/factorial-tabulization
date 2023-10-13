# factorial-tabulization
this is the i have written for factorial tabulization in this we get factorial given n numbers

package datastructurespractice;

public class factorialtabulization {
	public static void main(String[] args) {
		int n = 10; // Adjust this value to set the range for which you want to calculate factorials.
        long[] factorialTable = computeFactorials(n);

        for (int i = 0; i <= n; i++) {
            System.out.println("Factorial of " + i + " is " + factorialTable[i]);
        }
    }

    public static long[] computeFactorials(int n) {
        long[] factorialTable = new long[n + 1];
        factorialTable[0] = 1; // Factorial of 0 is 1

        for (int i = 1; i <= n; i++) {
            factorialTable[i] = factorialTable[i - 1] * i;
        }

        return factorialTable;
    }

	}
