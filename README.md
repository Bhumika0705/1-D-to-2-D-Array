# 1-D-to-2-D-Array
import java.util.Scanner;

public class oneDtotwoD {
    public oneDtotwoD() {
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter dimensions of Array:");
        int n = sc.nextInt();
        int m = sc.nextInt();
        int[] arr = new int[m * n];
        int[][] mat = new int[n][m];
        System.out.println("Enter the elements in 1 D array: ");

        int idx;
        for(idx = 0; idx < m * n; ++idx) {
            arr[idx] = sc.nextInt();
        }

        idx = 0;

        int i;
        int j;
        for(i = 0; i < n; ++i) {
            for(j = 0; j < m; ++j) {
                mat[i][j] = arr[idx];
                ++idx;
            }
        }

        for(i = 0; i < n; ++i) {
            for(j = 0; j < m; ++j) {
                System.out.print(mat[i][j] + " ");
            }

            System.out.println();
        }

    }
}
