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
