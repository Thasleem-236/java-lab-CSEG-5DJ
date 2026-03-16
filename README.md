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
![Output 2c]()










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
