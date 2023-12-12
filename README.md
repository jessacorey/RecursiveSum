import java.util.Scanner;

public class RecursiveSum {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int[] numbers = new int[5];

        System.out.println("Enter five numbers:");

        // Input numbers
        for (int i = 0; i < numbers.length; i++) {
            System.out.print("Number " + (i + 1) + ": ");
            numbers[i] = scanner.nextInt();
        }

        // Calculate and display the sum
        System.out.println("Sum of the numbers: " + calculateSum(numbers, 0));

        scanner.close();
    }

    // Recursive method to calculate sum
    private static int calculateSum(int[] array, int index) {
        // Base case: return 0 when index reaches the length of the array
        if (index == array.length) {
            return 0;
        }

        // Recursive case: add the current element and call the method with the next index
        return array[index] + calculateSum(array, index + 1);
    }
}
