# java-lab-CSEG-5DJ
experiments
## Experiment 2
## Title:2b(implement overloading)
```
class overload{
        int add(int a,int b){
                return a+b;
                }
        double add(double a,double b){
                return a+b;
                }
        int add(int a,int b,int c){
                return a+b+c;
                }
        }
class overmain{
        public static void main(String args[]){
                overload over=new overload();
                System.out.println("add of:"+over.add(5,2));
                System.out.println("add of:"+over.add(10.2,2.1));
                System.out.println("add of:"+over.add(5,2,6));
                }
        }

```
## Output:
![Output 2b]()
