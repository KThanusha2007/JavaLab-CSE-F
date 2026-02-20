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

## TITLE- Illustrating Multiple catch classes
```java
import java.util.Scanner;
import java.util.InputMismatchException;
public class MultipleCatchExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int[] arr = {10, 20, 30, 40, 50};
        try {
            System.out.print("Enter first number: ");
            int a = sc.nextInt();
            System.out.print("Enter second number: ");
            int b = sc.nextInt();
            int result = a / b;
            System.out.println("Result = " + result);
            System.out.print("Enter index to access array element: ");
            int index = sc.nextInt();
            System.out.println("Element at index = " + arr[index]);
        }
        catch (ArithmeticException e) {
            System.out.println("Error: Division by zero is not allowed.");
        }
        catch (InputMismatchException e) {
            System.out.println("Error: Please enter numeric values only.");
        }
  catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Error: Invalid array index.");
        }
        catch (Exception e) {
            System.out.println("Some other error occurred.");
        }
        System.out.println("Program continues...");
        sc.close();
    }
}
```

OUTPUT  :
1[output of multiple catch class](exp6b.png)

