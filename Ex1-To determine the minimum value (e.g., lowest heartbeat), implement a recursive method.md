# EX 1 You’re creating a health monitoring device which stores several sensor readings in an array. To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
## DATE: 09.01.2026
## AIM:
To write a JAVA program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.

## Algorithm
1. Read the number of elements n and input all n integers into an array arr.
2. Start the recursive function getMin(arr, 0, n) to find the minimum element.
3. Inside the recursive function, check if the current index i is the last index (i      == n−1).If yes, return arr[i] as the minimum.
4. Otherwise, recursively call getMin(arr, i+1, n) to find the minimum of the remaining elements.
5. Compare the current element arr[i] with the minimum of the rest and return the smaller value.   

## Program:
```
/*
Program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
Developed by: VIMALA RANI A
RegisterNumber:  212223040240
*/
```
```
import java.util.*;
public class Main {
    static int getMin(int[] arr, int i, int n) 
    {
        if (i == n - 1) {
            return arr[i];
        }
        int minOfRest = getMin(arr, i + 1, n);
        return Math.min(arr[i], minOfRest);
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for(int i=0; i<n; i++) {
            arr[i] = sc.nextInt();
        }
        System.out.println(getMin(arr, 0, n));
    }
}
```

## Output:
<img width="403" height="233" alt="image" src="https://github.com/user-attachments/assets/ab59116b-dc6b-4603-81bb-270092b285b4" />

## Result:
Thus the JAVA program to find the minimum value (e.g., lowest heartbeat), implement a recursive method has implemented successfully
