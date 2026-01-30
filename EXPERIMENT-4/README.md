# EXPERIMENT-4
## TITLE :4a.)Implement Single Inheritance
```java
public class Person {
    String name;
    int age;
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
    public void displayPersonDetails() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}
public class Employee extends Person {
double annualSalary;
int yearOfJoining;
    String nationalInsuranceNumber;
 public Employee(String name, int age, double annualSalary, int yearOfJoining, String nationalInsuranceNumber) {
 super(name, age); 
  this.annualSalary = annualSalary;
this.yearOfJoining = yearOfJoining;
  this.nationalInsuranceNumber = nationalInsuranceNumber;
    }
    public void displayEmployeeDetails() {
        displayPersonDetails(); 
        System.out.println("Annual Salary: " + annualSalary);
        System.out.println("Year of Joining: " + yearOfJoining);
        System.out.println("National Insurance Number: " + nationalInsuranceNumber);
    }
}
public class TestEmployee {
    public static void main(String[] args) {
        Employee emp1 = new Employee("Monitha Sree", 28, 55000.50, 2018, "NI12345");
        emp1.displayEmployeeDetails();
    }
}
```
![output of single inheritance](exp4a.png)
