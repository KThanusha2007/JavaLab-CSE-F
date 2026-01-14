# EXPERIMENT 3
## TITLE : 3a.) Implement Constructor Overloading
```
 class Student {
int id;
String name;
int age;
Student() {
}
Student(int i, String n, int a) {
id = i;
name = n;
age = a;
}
void display() {
System.out.println("name:" + name);
System.out.println("age:" + age);
System.out.println("id:" + id);
System.out.println();
 }
}
public class Main {
 public static void main(String[] args) {
Student s1 = new Student();
Student s2 = new Student(102, "Anita", 20);
s1.display();
s2.display();
}
}
```

# OUTPUT 
![output of constructor](exp3a.png)

## TITLE : 3b.)Binary Search using java
```
import java.util.Scanner;
import java.util.Arrays;
class BinarySearch {
int list[];
int size;
int key = -1;
BinarySearch(int size) {
this.size = size;
list = new int[size];
 }
void set_list() {
Scanner sc = new Scanner(System.in);
for (int i = 0; i < list.length; i++) {
list[i] = sc.nextInt();
}
}
void get_list() {
for (int i = 0; i < list.length; i++) {
System.out.print(list[i] + " ");
 }
System.out.println();
    }
int binarysearch(int key) {
int low = 0;
int high = list.length - 1;
while (low <= high) {
int mid = (low + high) / 2;
if (list[mid] == key) {
 return mid;
} else if (list[mid] < key) {
low = mid + 1;
} else {
high = mid - 1;
}
}
return -1;
}
 void getItem(int index) {
System.out.println("Key element is found at index " + index);
System.out.println("Key element is " + list[index]);
}
public static void main(String[] args) {
Scanner sc = new Scanner(System.in);
System.out.print("Enter size: ");
int size = sc.nextInt();
BinarySearch s = new BinarySearch(size);
System.out.println("Enter elements:");
s.set_list();
Arrays.sort(s.list);   
System.out.println("Sorted list:");
s.get_list();
 System.out.print("Enter key to search: ");
int key = sc.nextInt();
int index = s.binarysearch(key);
if (index != -1) {
s.getItem(index);
} else {
System.out.println("Key element not found");
}
}
}
```

# OUTPUT
![output of binary search](exp3b.png)




