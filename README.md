# PerfectNumberChecker
PerfectNumberChecker
import java.util.Scanner;

public class PerfectNumberChecker {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Введите число: ");
        int number = scanner.nextInt();

        boolean isPerfectNumber = checkPerfectNumber(number);
        if (isPerfectNumber) {
            System.out.println("Число является совершенным!");
        } else {
            System.out.println("Число не является совершенным.");
        }
    }

    public static boolean checkPerfectNumber(int number) {
        int sum = 0;
        for (int i = 1; i < number; i++) {
            if (number % i == 0) {
                sum += i;
            }
        }
        return sum == number;
    }
}
