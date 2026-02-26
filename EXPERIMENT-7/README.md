# EXPERIMENT - 7
## TITLE : 7a.) 
```java
import java.util.Scanner;
class InvalidCountryException extends Exception {
 InvalidCountryException() {
        super();
    }   InvalidCountryException(String message) {
        super(message);
    }
}
class UserRegistration {
    void registerUser(String userName, String userCountry)
            throws InvalidCountryException {
        if (!userCountry.equals("India")) {
            throw new InvalidCountryException(
                    "User outside India cannot be registered");
        } else {
            System.out.println("User registered successfully");
        }
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        UserRegistration ur = new UserRegistration();
try {
 System.out.print("Enter the user name: ");
            String uname = sc.nextLine();
            System.out.print("Enter the country name: ");
            String cname = sc.nextLine();
            ur.registerUser(uname, cname);
        } catch (InvalidCountryException e) {
            System.out.println(e.getMessage());
        } catch (Exception e) {
            System.out.println("Unknown error: " + e);
        } finally {
            sc.close();
            System.out.println("Finally block executed successfully");
        }
    }
}
```
![output of 7a](exp7a)
