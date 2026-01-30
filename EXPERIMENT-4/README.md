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

## TITLE :4b.)Implement Multi-level Inheritance
```java
public class Bicycle {
    String pedalType;
 public void showBicycleInfo() {
 System.out.println("This is a bicycle with pedals.");
        System.out.println("Pedal Type: " + pedalType);
    }
}
public class Motorbike extends Bicycle {
 int engineCapacity;
 public void showMotorbikeInfo() {
 System.out.println("This motorbike has an engine.");
 System.out.println("Engine Capacity: " + engineCapacity + " cc");
  }
}
public class ElectricBike extends Motorbike {
 int batteryCapacity;
  public void showElectricBikeInfo() {
  System.out.println("This electric bike has an electric motor and battery.");
  System.out.println("Battery Capacity: " + batteryCapacity + " Wh");
    }
}
public class TestVehicle {
    public static void main(String[] args) {
        ElectricBike eBike = new ElectricBike();
        eBike.pedalType = "Standard Pedals";
        eBike.engineCapacity = 150;
        eBike.batteryCapacity = 500;
        eBike.showBicycleInfo();       
        eBike.showMotorbikeInfo();      
        eBike.showElectricBikeInfo();   
    }
}
```
![output of multi-level inheritance](exp4b.png)
