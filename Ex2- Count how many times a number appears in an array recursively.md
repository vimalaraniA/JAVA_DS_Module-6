# Ex2 Count how many times a number appears in an array recursively.
## DATE: 10.01.2026
## AIM:
To write a Java program to Count how many times a number appears in an array recursively.

## Algorithm
1. Read the value of n, input n elements into array arr, and read the number key whose occurrences must be counted.
2. Call the recursive function countOccurrences(arr, n, 0, key) starting from index 0.
3. Inside the recursive function, check if the current index equals n;if yes, return 0 because the entire array has been checked.
4. If arr[index] equals key, return 1 + countOccurrences(arr, n, index + 1, key);otherwise return countOccurrences(arr, n, index + 1, key).
5. Return the final count to the main program and print how many times key appears in the array.     

## Program:
```
/*
Program Count how many times a number appears in an array recursively.
Developed by: VIMALA RANI A 
RegisterNumber:  212223040240
*/
```
```
import java.util.Scanner;
public class CountOccurrences {
    public static int countOccurrences(int[] arr, int n, int target) {
        if (n == 0) {
            return 0;
        }
        if (arr[n - 1] == target) {
            return 1 + countOccurrences(arr, n - 1, target);
        } else {
            return countOccurrences(arr, n - 1, target);
        }
    }
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int size = scanner.nextInt();
        if (size <= 0) {
            System.out.println("Invalid array size. Must be positive.");
            return;
        }
        int[] arr = new int[size];
        for (int i = 0; i < size; i++) {
            arr[i] = scanner.nextInt();
        }
        int target = scanner.nextInt();
        int count = countOccurrences(arr, size, target);
        System.out.println("The number " + target + " appears " + count + " time(s) in the array.");
        scanner.close();
    }
}
```

## Output:
<img width="954" height="551" alt="image" src="https://github.com/user-attachments/assets/c1379b70-22fa-4bbd-bfb5-534bc8267102" />

## Result:
Thus, the Java program to Count how many times a number appears in an array recursively is implemented successfully.
