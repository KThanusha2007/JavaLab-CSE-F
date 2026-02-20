# EXPERIMENT-6
## TITLE - Exception handling Mechanism
```java
import java.util.Scanner;
public class ArrayIndexException {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter size of array: ");
        int n = sc.nextInt();
        int[] arr = new int[n];
        System.out.println("Enter array elements:");
        for(int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        System.out.print("Enter index to access: ");
        int index = sc.nextInt();
        try {
            System.out.println("Element at index " + index + " is: " + arr[index]);
        }
        catch(ArrayIndexOutOfBoundsException e) {
            System.out.println("Invalid index! Please enter index between 0 and " + (n-1));
        }
        sc.close();
    }
}
```

OUTPUT :
![output of exception handling](exp6a.png)
