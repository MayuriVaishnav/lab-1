# lab-1
**1. accept no and check it is prime no or not**
**Ans.**
import java.util.Scanner;

public class PrimeNumber {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        while(true) {
        System.out.print("Enter a number: ");
        int number = scanner.nextInt();
        if (isPrime(number)) {
            System.out.println(number + " is a prime number.");
        } else {
            System.out.println(number + " is not a prime number.");
        }
    }
    }
    public static boolean isPrime(int num) {
        switch (num) {
            case 0:
            case 1:
                return false;
            default:
                for (int i = 2; i*i <= num; i++) {
                    if (num % i == 0) {
                        return false;
                    }
                }
                return true;
        }
    }
}
