# Ex5 Count Inversions in an Array
## DATE: 10.01.2026
## AIM:
To write a Java program  to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j

## Algorithm
1. Read n and the array elements.
2. Use merge sort to split the array into halves.
3. Count inversions in the left half and right half.
4. Merge the halves and count cross-inversions when right element < left element.
5. Add all inversion counts and print the result. 

## Program:
```
/*
Program toto Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j
Developed by: VIMALA RANI A 
RegisterNumber:  212223040240
*/
```
```
import java.util.Scanner;
public class CountInversions {
    public static int mergeSortAndCount(int[] arr, int left, int right) 
    {
        int count = 0;
        if (left < right) {
            int mid = (left + right) / 2;
            count += mergeSortAndCount(arr, left, mid);
            count += mergeSortAndCount(arr, mid + 1, right);
            count += mergeAndCount(arr, left, mid, right);
        }
        return count;
    }
    private static int mergeAndCount(int[] arr, int left, int mid, int right)
    {
        int[] temp = new int[right - left + 1];
        int i = left;      
        int j = mid + 1;   
        int k = 0;
        int invCount = 0;
        while (i <= mid && j <= right) {
            if (arr[i] <= arr[j]) {
                temp[k++] = arr[i++];
            } 
            else {
                temp[k++] = arr[j++];
                invCount += (mid - i + 1);
            }
        }
        while (i <= mid) {
            temp[k++] = arr[i++];
        }
        while (j <= right) {
            temp[k++] = arr[j++];
        }
        for (i = left, k = 0; i <= right; i++, k++) {
            arr[i] = temp[k];
        }

        return invCount;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) arr[i] = sc.nextInt();
        System.out.println(mergeSortAndCount(arr, 0, n - 1));
    }
}
```

## Output:
<img width="365" height="385" alt="image" src="https://github.com/user-attachments/assets/d827c093-aa20-4ea6-8afd-0dbcf8339f2e" />

## Result:
Thus the Java program to to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < jis implemented successfully.
