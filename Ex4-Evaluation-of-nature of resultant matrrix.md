# Ex4 You are given a Java program that performs matrix addition. If Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension, what will be the nature (even/odd/mixed) of the resulting matrix?
## DATE: 10.01.2026
## AIM:
To write a java function to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrix.

## Algorithm
1. Read matrix dimensions Input the number of rows r and columns c.
2. Read elements of Matrix A Fill the 2D array A[r][c] by reading integers row-wise.
3. Read elements of Matrix B Fill the 2D array B[r][c] similarly by reading integers row-wise.
4. Add corresponding elements of both matrices For each position (i, j), compute A[i][j] + B[i][j].
5. Print the resulting matrix Output each sum in matrix form, one row per line.   

## Program:
```
/*
Program to ind the nature of resultant matrrix.
Developed by: VIMALA RANI A 
RegisterNumber:  212223040240
*/
```
```
import java.util.Scanner;
public class MatrixAdditionNature {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int r = sc.nextInt();
        int c = sc.nextInt();
        int[][] A = new int[r][c];
        int[][] B = new int[r][c];
        int[][] C = new int[r][c];
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                A[i][j] = sc.nextInt();
            }
        }
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                B[i][j] = sc.nextInt();
            }
        }
        boolean hasOdd = false;
        boolean hasEven = false;

        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                C[i][j] = A[i][j] + B[i][j];

                if (C[i][j] % 2 == 0)
                    hasEven = true;
                else
                    hasOdd = true;
            }
        }
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                System.out.print(C[i][j] + " ");
            }
            System.out.println();
        }
    }
}
```

## Output:
<img width="371" height="556" alt="image" src="https://github.com/user-attachments/assets/3892dfad-9eff-4501-bd61-1088e3441a52" />

## Result:
Thus, the java program to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix is implemented successfully.
