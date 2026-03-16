# java-lab-CSEG-5DJ
experiments
## experiment 1
## Title:1a(default primdatatypes)
```
class DefaultPrimitiveType {
    byte primbyte;
    short primshort;
    int primint;
    double primdouble;
    char primchar;
    float primfloat;
    long primlong;
    boolean primboolean;
    public static void main(String args[]) {
        DefaultPrimitiveType dDpt = new DefaultPrimitiveType();
        System.out.println("default value of byte:" + dDpt.primbyte);
        System.out.println("default value of short:" + dDpt.primshort);
        System.out.println("default value of int:" + dDpt.primint);
        System.out.println("default value of double:" + dDpt.primdouble);
        System.out.println("default value of char:" + dDpt.primchar + " '");
        System.out.println("default value of float:" + dDpt.primfloat);
        System.out.println("default value of long:" + dDpt.primlong);
        System.out.println("default value of boolean:" + dDpt.primboolean);
    }
}
```
## Output:
![Output 1a](https://github.com/Thasleem-236/java-lab-CSEG-5DJ/blob/a4043e365ccc6161c5483a2cb955b132112e8fb6/1a.png)
## Title:1b(quadratic equation)
```
import java.util.Scanner;
class Quadraticequation{
     public static void main(String args[]){
         Scanner sc=new Scanner(System.in);
         System.out.println("Enter value of a:");
         double a=sc.nextDouble();
          System.out.println("Enter value of b:");
         double b=sc.nextDouble();
          System.out.println("Enter value of c:");
         double c=sc.nextDouble();
         double D=b*b-4*a*c;
         if(D>0){
            System.out.println("Roots are real and distinct");
            double root1=(-b+Math.sqrt(D))/(2*a);
            double root2=(-b-Math.sqrt(D))/(2*a);
            System.out.println("Root1:"+root1);
            System.out.println("Root2:"+root2);
            }
         else if(D==0){
            System.out.println("Roots are equal and real");
            double root=-b/(2*a);
            System.out.println("Root:"+root);
            }
         else{
            System.out.println("Roots are complex and imaginary");
            double realpart=-b/(2*a);
            double imaginarypart=Math.sqrt(-D)/(2*a);
            System.out.println("Roots are complex and imaginary");
            System.out.println("Root1="+realpart+"+i"+imaginarypart);
            System.out.println("Root2="+realpart+"-i"+imaginarypart);
            }
        sc.close();
        }
   }
```
## Output:
![Output 1b](https://github.com/Thasleem-236/java-lab-CSEG-5DJ/blob/50ccf13769df89807b6314c80c3985cfc4e26c64/1b.png)

## experiment 2
## Title:2a(implement class mechanism)
```
class myclass{
        void displaymessage(){
                System.out.println("hello world");
                }
        }
class main{
         public static void main(String args[]){
                myclass my=new myclass();
                my.displaymessage();
                }
        }
```
## Output:
![Output 2a](https://github.com/Thasleem-236/java-lab-CSEG-5DJ/blob/1458fe1563e9900ed3c8af08cba939c01312bed9/2a.png)
## Title:2b(implement method overloading)
```
class overload{
  int sum(int a ,int b){
    return a+b;
  }
  int sum(int a ,int b,int c){
  return a+b+c;
  }
  double sum(double a ,double b){
   return a+b;
  }
}
class overmain{
 public static void main(String args[]){
   overload over= new overload();
   System.out.println("sum of 2 integers:"+over.sum(5,2));
   System.out.println("sum of 3 integers:"+over.sum(5,2,6));
   System.out.println("sum of two real numbers:"+over.sum(10.2,2.1));
  }
}
```
## Output:
![Output 2b](https://github.com/Thasleem-236/java-lab-CSEG-5DJ/blob/fca2c7589ef40c3c1abd374eea534a06f86c2c38/2b.png)
## Title:2c(implement constructor)
```
class student{
 String sname;
 int sage;
 double smarks;
 student(String name,int age,double marks){
   sname=name;
   sage=age;
   smarks=marks;
  }
 void display(){
  System.out.println("student name is :"+sname);
  System.out.println("student age is :"+sage);
  System.out.println("stduent marks is:"+smarks);
  }
}
class main{
 public static void main(String args[]){
  student std= new student("sree",12,960);
  std.display();
  }
}
```
## Output:
![Output 2c](https://github.com/Thasleem-236/java-lab-CSEG-5DJ/blob/0d77ef38a4c7d5470b1ba48e9eba9d3ccb1ce858/2c.png)

## Experiment 3
## Title:3a(implement constructoroverload)

```
class student{
 String name;
 int age;
 double marks;
 student(){
 }
 student(String name,int age,double marks){
  this.name=name;
  this.age=age;
  this.marks=marks;
}
void display(){
  System.out.println("name:"+name);
  System.out.println("age:"+age);
  System.out.println("marks:"+marks);
  }
}

class main{
 public static void main(String args[]){
   student std= new student();
   std.display();
   student std1=new student ("thasleem",19,60);
   std1.display();
 }
}

        

```
## Output:
![Output 3a](https://github.com/Thasleem-236/java-lab-CSEG-5DJ/blob/06a60f7cb4583bf64d32add08a34ecdf30d7c855/3a.png)
## Title:3b(implement binarysearch)
```
import java.util.Scanner;
class Binary {
    int list[];
    int size;
    Binary(int size) {
        this.size = size;
        list = new int[size];
    }
    void setList() {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter items in ascending order:");
        for (int i = 0; i < size; i++) {
            System.out.println("Enter value of " + (i + 1) + ":");
            list[i] = sc.nextInt();
        }
    }
    void getList() {
        System.out.println("List elements:");
        for (int i = 0; i < size; i++) {
            System.out.print(list[i] + " ");
        }
        System.out.println();
    }
    int binary(int key) {
        int low = 0;
        int high = size - 1;
        while (low <= high) {
            int mid = (low + high) / 2;
            if (list[mid] == key)
                return mid;
            else if (list[mid] < key)
                low = mid + 1;
            else
                high = mid - 1;
        }
        return -1;
    }
}
class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter size of list:");
        int size = sc.nextInt();
        Binary b = new Binary(size);
        b.setList();
        b.getList();
        System.out.println("Enter a key to search:");
        int key = sc.nextInt();
        int index = b.binary(key);
        if (index == -1) {
            System.out.println("Key item does not exist");
        } else {
            System.out.println("Key item exists at position: " + (index + 1));
        }
    }
}
```
## Output:
![Output 3b](https://github.com/Thasleem-236/java-lab-CSEG-5DJ/blob/53c771bacc366f22cb691bc5c42ffd235c7b3434/3b.png)
## Title:3c(implement bubblesort)
```
class BubbleSort {
    BubbleSort(int arr[]) {
        int n = arr.length;
        for (int i = 0; i < n - 1; i++) {
            for (int j = 0; j < n - i - 1; j++) {
                if (arr[j] > arr[j + 1]) {
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }

            }
        }
    }
}
import java.util.Scanner;
class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter size of array:");
        int n = sc.nextInt();
        int arr[] = new int[n];
        System.out.println("Enter elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        new BubbleSort(arr);
        System.out.println("Sorted array:");
        for (int i = 0; i < n; i++) {
            System.out.print(arr[i] + " ");
        }
    }
}
```
## Output:
![Output 3c](https://github.com/Thasleem-236/java-lab-CSEG-5DJ/blob/a17d4f34396204ea7761c1b0f3769c1f65f166fb/3c.png)
## Experiment 4
## Title:4a(implement single Inheritance)
```
class Person {
    String name;
    int age;

    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    void displayPersonDetails() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}

class Employee extends Person {
    double annualSalary;
    int yearOfJoining;
    String nationalInsuranceNumber;

    Employee(String name, int age, double salary, int year, String nin) {
        super(name, age);
        annualSalary = salary;
        yearOfJoining = year;
        nationalInsuranceNumber = nin;
    }

    void displayEmployeeDetails() {
        displayPersonDetails();
        System.out.println("Annual Salary: " + annualSalary);
        System.out.println("Year of Joining: " + yearOfJoining);
        System.out.println("National Insurance Number: " + nationalInsuranceNumber);
    }
}

public class TestEmployee {
    public static void main(String[] args) {
        Employee emp = new Employee("thasleem", 19, 60000, 2022, "NJ123456A");
        emp.displayEmployeeDetails();
    }
}
```
## Output:
![Output 4a](https://github.com/Thasleem-236/java-lab-CSEG-5DJ/blob/460a2d1aa63b4e3d7640451df974544ba7fa2c71/4a.png)
## Title:4b(implement multiple level Inheritance)
```
class Bicycle {
    String pedalType;

    void showBicycleInfo() {
        System.out.println("This is a bicycle with pedals");
        System.out.println("Pedal Type: " + pedalType);
    }
}

class Motorbike extends Bicycle {
    int engineCapacity;

    void showMotorbikeInfo() {
        System.out.println("This motorbike has an engine");
        System.out.println("Engine Capacity: " + engineCapacity + " cc");
    }
}

class ElectricBike extends Motorbike {
    int batteryCapacity;

    void showElectricBikeInfo() {
        System.out.println("This electric bike has an electric motor & battery");
        System.out.println("Battery Capacity: " + batteryCapacity + " Wh");
    }
}

public class TestVehicle {
    public static void main(String[] args) {
        ElectricBike eBike = new ElectricBike();

        eBike.pedalType = "Standard Pedals";
        eBike.engineCapacity = 250;
        eBike.batteryCapacity = 500;

        eBike.showBicycleInfo();
        eBike.showMotorbikeInfo();
        eBike.showElectricBikeInfo();
    }
}
```
## Output:
![Output 4b](https://github.com/Thasleem-236/java-lab-CSEG-5DJ/blob/d474aee9169aea1c96061189ed3551a16047b670/4b.png)
## Title:4c(implement abstract class)
```
abstract class Figure {
    double dim1, dim2;

    Figure(double d1, double d2) {
        dim1 = d1;
        dim2 = d2;
    }

    abstract double area();
}

class Rectangle extends Figure {
    Rectangle(double length, double breadth) {
        super(length, breadth);
    }

    double area() {
        return dim1 * dim2;
    }
}

class Triangle extends Figure {
    Triangle(double base, double height) {
        super(base, height);
    }

    double area() {
        return 0.5 * dim1 * dim2;
    }
}

public class TestFigure {
    public static void main(String[] args) {
        Figure f1 = new Rectangle(23.4, 14.5);
        Figure f2 = new Triangle(12.3, 15.6);

        System.out.println("Area of Rectangle = " + f1.area());
        System.out.println("Area of Triangle = " + f2.area());
    }
}
```
## Output:
![Output 4c](https://github.com/Thasleem-236/java-lab-CSEG-5DJ/blob/026237bc3660c38ff59973b51cbbd8fddb03b917/4c.png)
## expriment 5
## Title:5a(implement intrface)
```
interface Sortable{
  void sort(int [] arr);
  }
class Bubblesort implements Sortable{
  public void sort(int [] arr){
   int size =arr.length;
   int temp=0;
   for(int i=0;i<size-1;i++){
    for(int j=0;j<size-i-1;j++){
      if(arr[j]>arr[j+1]){
         temp=arr[j];
         arr[j]=arr[i];
         arr[i]=temp;
          }
       }
     }
  }
}
class Selectionsort implements Sortable {
   public void sort (int [] arr){
    int size=arr.length;
    int minindex=0;
    int min;
    for(int i=0;i<size;i++){
      min =arr[i];
     for(int j=i+1;j<size;j++){
       if(min>arr[j]){
          min=arr[j];
          minindex=j;
         }
       }
     arr[i]=min;
    }
   }
 }
class Testsort {
    static void display(int arr[]) {
        for (int ele : arr) {
            System.out.print(ele + ", ");
        }
        System.out.println();
    }
    public static void main(String args[]) {
        int arr1[] = {9, 7, 4, 3, 6, 8};
        int arr2[] = {8, 6, 3, 4, 7, 9};
        Sortable s;
        s = new Bubblesort();
        s.sort(arr1);
        System.out.println("After Bubble Sort:");
        display(arr1);

        s = new Selectionsort();
        s.sort(arr2);
        System.out.println("After Selection Sort:");
        display(arr2);
    }
}
```
## Output:
![Output 5a](https://github.com/Thasleem-236/java-lab-CSEG-5DJ/blob/50738e08f694fd2e31747067f47002c9cdb1890f/5a.png)
## Title:5b(implement polymorphism)
```
class Vehicle{
    void run(){
          System.out.println(" vechicle is running:");
     }
  }
class car extends Vehicle{
    void run(){
           System.out.println("car is running :");
      }
  }
class bike extends Vehicle{
     void run(){
       System.out.println("bike is running:");
    }
  }
class TestVehicle{
   public static void main(String args[]){
     Vehicle v ;
     v=new car();
     v.run();
     v=new bike();
     v.run();
     v=new Vehicle();
     v.run();
    }
}
```
## Output:
![Output 5b](https://github.com/Thasleem-236/java-lab-CSEG-5DJ/blob/71e1c8cb60868143c17d53fbc4fa083752e3e9ff/5b.png)
## Title:5c(implement stringbuffer)
```
class Deletechar{
  public static void main(String args[]){
    StringBuffer sb =new StringBuffer("java programming");
    System.out.println(sb);
    sb.deleteCharAt(4);
    System.out.println(sb);
    sb.delete(0,4);
    System.out.println(sb);

   }
}
```
## Output:
![Output 5c](https://github.com/Thasleem-236/java-lab-CSEG-5DJ/blob/c8dd7ef8eb0347cbc5beb13d55a3c2965dd88cb7/5c.png)
## Experiment 6
## Title:6a(implement exception handling)
```
import java.util.Scanner;
class ArrayIndexExceptionDemo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter size of array: ");
        int n = sc.nextInt();
        int[] arr = new int[n];
        System.out.println("Enter " + n + " elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        try {
            System.out.print("Enter index to access: ");
            int index = sc.nextInt();
            System.out.println("Element at index " + index + " is " + arr[index]);
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Array index out of bounds!");
        }
        sc.close();
    }
}
```
## Output:
![Output 6a](https://github.com/Thasleem-236/java-lab-CSEG-5DJ/blob/e36c1836d828ee375830644020cddeaebaf51503/6a.png)
## Title:6b(implement multiple catch blocks)
```
import java.util.Scanner;

class MultipleCatchDemo {
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

            System.out.print("Enter index to access array: ");
            int index = sc.nextInt();
            System.out.println("Element = " + arr[index]);
        }
        catch (ArithmeticException e) {
            System.out.println("Arithmetic Exception occurred");
        }
        catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Array Index Out Of Bounds Exception occurred");
        }
        catch (Exception e) {
            System.out.println("Some other exception occurred");
        }

        sc.close();
        System.out.println("Program continues...");
    }
```
## Output:
![Output 6b](https://github.com/Thasleem-236/java-lab-CSEG-5DJ/blob/976d91f2ac765422fd579db81017d35084db85a2/6b.png)
## Title:6c(implementing java built-in exception)
```
import java.util.Scanner;

class BuiltInException {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        try {
            System.out.print("Enter a number to divide 100: ");
            int n = sc.nextInt();

            int result = 100 / n;
            System.out.println("Result = " + result);

            int[] arr = new int[3];
            System.out.println(arr[5]);
        }
        catch (ArithmeticException e) {
            System.out.println("Arithmetic Exception occurred");
        }
        catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Array Index Out Of Bounds Exception occurred");
        }
        catch (Exception e) {
            System.out.println("General Exception occured");
        }
       finally{
           System.out.println("Program execution continue...");
           sc.close();
       }
   }
}
```
## Output:
![Output 6c](https://github.com/Thasleem-236/java-lab-CSEG-5DJ/blob/8aaea8c1a5c3d4afababecc77a67d4c80cc7b5a5/6c.png)
## Experiment 7
## Title:7a(user defined exception)
```
class InvalidCountryException extends Exception {
          InvalidCountryException() {
              super();
              }
              InvalidCountryException(String message) {
              super(message);
              }
            }
class UserRegion {

    void registerUser(String userName, String userCountry) throws InvalidCountryException {

        if (!userCountry.equals("India")) {
            throw new InvalidCountryException("User outside India cannot be registered");
        } else {
            System.out.println("User registration done successfully");
        }
    }

    public static void main(String args[]) {

        UserRegion ur = new UserRegion();

        try {
            ur.registerUser("Ravi", "USA");
        }
        catch (InvalidCountryException e) {
            System.out.println(e.getMessage());
        }
    }
}
```
![Output 7a]()
## Title:7b(creating threads by extending thread class)
```
class GoodMorningThread extends Thread {
    public void run() {
        while (true) {
            System.out.println("Good Morning");
            try {
                Thread.sleep(1000); 
            } catch (InterruptedException e) {
                System.out.println(e);
            }
        }
    }
}
  class HelloThread extends Thread {
     public void run() {
          while(true) {
            System.out.println("Hello");
         try {
            Thread.sleep(2000);
         }
         catch(InterruptedException e) {
               System.out.print(e);
           }
        }
    }
  }
   class WelcomeThread extends Thread {
         public void run() {
          while(true) {
        System.out.println("Welcome");
         try {
           Thread.sleep(3000);
         }
         catch(InterruptedException e) {
         System.out.print(e);
         }
       }
     }
   }
  class TestThreads {
     public static void main(String args[]) {
            GoodMorningThread t1 = new GoodMorningThread();
            HelloThread t2 = new HelloThread();
            WelcomeThread t3 = new WelcomeThread();


            t1.start();
            t2.start();
            t3.start();
           }
         }
```
![Output 7b]()
## Title:7c(isAlive() and join())
```
class LongRunningTask extends Thread {
        public void run() {
      System.out.println("Long running task started...");
      try {
            for(int i=1;i<= 5;i++) {
      System.out.println("Working..." +i);
            Thread.sleep(1000);
        }
     }
      catch(InterruptedException e) {
       System.out.println(e);
   }
  System.out.println("Long running task completed!");
      }
     }
public class ThreadDemo {
    public static void main(String[] args) {

        LongRunningTask task1 = new LongRunningTask();

        System.out.println("Before starting task1: " + task1.isAlive());

        task1.start();

        System.out.println("After starting task1: " + task1.isAlive());

        try {
            System.out.println("Main thread waiting for task1 to complete using join()...");
            task1.join();
        } catch (InterruptedException e) {
            System.out.println(e);
        }

        System.out.println("After task1 completion: " + task1.isAlive());
        System.out.println("Main thread continues execution.");
    }
}
```
![Output 7c]()
## Experiment 8
## Title:8a(Deamon Threads)
```
class DaemonThread extends Thread {
     public void run() {
      while(true) {
     System.out.println("Daemon thread running");
      try {
      Thread.sleep(500);
       }catch(InterruptedException e) {
        System.out.print(e);
         }
      }
}
}
  class UserThread extends Thread {
     public void run() {
          while(true) {
          for(int i=1;i<=5;i++) {
            System.out.println("User thread iteration:" +i);
            try {  
         Thread.sleep(1000);
          }catch(InterruptedException e) {
             System.out.print(e);
        }
      }
    }
}
}
class TestDaemon{
    public static void main(String[]args){
              UserThread userThread=new UserThread();
              DaemonThread daemonThread=new DaemonThread();
              daemonThread.setDaemon(true);
              userThread.start();
              daemonThread.start();
         }
}
```
![Output 8a]()
## Title:8b(ProducerConsumer Problem)
```
class Buffer {
    int[] buffer;
    int count = 0;
    int in = 0, out = 0;

    Buffer(int size) {
        buffer = new int[size];
    }

    synchronized void produce(int item) {
        while (count == buffer.length) {
            try {
                wait();
            } catch (InterruptedException e) {}
        }

        buffer[in] = item;
        in = (in + 1) % buffer.length;
        count++;

        System.out.println("Produced: " + item);

        notify();
    }

    synchronized int consume() {
        while (count == 0) {
            try {
                wait();
            } catch (InterruptedException e) {}
        }

        int item = buffer[out];
        out = (out + 1) % buffer.length;
        count--;

        System.out.println("Consumed: " + item);

        notify();
        return item;
    }
}

class Producer extends Thread {
    Buffer buffer;
    int N;

    Producer(Buffer buffer, int N) {
        this.buffer = buffer;
        this.N = N;
    }

    public void run() {
        for (int i = 1; i <= N; i++) {
            buffer.produce(i);
        }
    }
}

class Consumer extends Thread {
    Buffer buffer;
    int N;

    Consumer(Buffer buffer, int N) {
        this.buffer = buffer;
        this.N = N;
    }

    public void run() {
        for (int i = 1; i <= N; i++) {
            buffer.consume();
        }
    }
}

public class ProducerConsumerDemo {
    public static void main(String[] args) {

        Buffer buffer = new Buffer(5);
        int N = 10;

        Producer p = new Producer(buffer, N);
        Consumer c = new Consumer(buffer, N);

        p.start();
        c.start();
    }
}
```
![Output 8b]()
## Title:8c(packages)
```
package arithmetic;

public class ArithmeticOperations {

    public int add(int x, int y) {
        return x + y;
    }

    public int subtraction(int x, int y) {
        return x - y;
    }

    public int multiplication(int x, int y) {
        return x * y;
    }

    public int division(int x, int y) {
        return x / y;
    }
}
import arithmetic.ArithmeticOperations;

class Calculate {
    public static void main(String[] args) {

        ArithmeticOperations ae = new ArithmeticOperations();

        int sum = ae.add(10, 5);
        System.out.println("Addition: " + sum);

        int diff = ae.subtraction(10, 5);
        System.out.println("Subtraction: " + diff);

        int prod = ae.multiplication(10, 5);
        System.out.println("Multiplication: " + prod);

        int div = ae.division(10, 5);
        System.out.println("Division: " + div);
    }
}
```
![Output 8c]()


























