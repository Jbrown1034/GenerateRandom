package techFiosProject;

import java.util.Arrays;
import java.util.Random;
import java.util.Scanner;

public class RandomNum {

	public static void main(String[] args) {

		
		int[] numbers = new int[500];
		Random random = new Random();

		for (int i = 0; i < numbers.length; i++) {
			numbers[i] = random.nextInt(1000); // Random numbers between 0 and 999
		}

		Scanner scanner = new Scanner(System.in);
		System.out.print("Enter the value of n: ");
		int n = scanner.nextInt();

		Arrays.sort(numbers);

		if (n > 0 && n <= numbers.length) {
			System.out.println("The " + n + "the smallest number is: " + numbers[n - 1]);
		} else {
			System.out.println("Invalid input. Please enter a value between 1 and 500.");
		}

		scanner.close();

	}

}
