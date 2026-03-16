# java-lab-CSEG-5DJ
experiments
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
![Output 3a]()
