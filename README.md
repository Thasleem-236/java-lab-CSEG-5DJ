# java-lab-CSEG-5DJ
experiments
## Experiment 2
## Title:2c(implement constructor)
```
class student{
        String name;
        int age;
        double marks;
        student(String name, int age, double marks){
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
class stdmain{
        public static void main(String args[]){
                student std=new student("thasleem",19,80.0);
                std.display();
                }
        }

```
## Output:
![Output 2c](https://github.com/Thasleem-236/java-lab-CSEG-5DJ/blob/14e654d5c77085e94f5f01f11ee798a2334c5259/2c.png)
