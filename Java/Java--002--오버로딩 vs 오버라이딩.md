# 오버로딩 vs 오버라이딩
### 오버로딩
- 오버로딩(Overloading)이란 동일한 이름의 함수를 여러번 정의하여 사용할 수 있다는 것이다.
- 동일한 이름의 메소드를 매겨 변수나 유형을 달리하여 다양한 방법으로 호출하여 사용할 수 있다.
```
public class Overloading {
  
  public void func() {
    System.out.println("매개변수 없음");
  }
  
  public void func(int a) {
    System.out.println("매개변수 : "+a);
  }
  
  public void func(int a, int b) {
    System.out.println("a + b = "+a+b);
  }
  
  public static void main(String[] args) {
    Overloading over = new Overloading();
    
    over.func(); // 매개변수 없음
    over.func(1); // 매개변수 : 1
    over.func(1, 2); // a + b = 3
  }
}
```
***
### 오버라이딩
- 오버라이딩(Overriding)이란 부모 클래스로부터 상속받은 메소드를 재정의하여 사용하는 것이다.
```
public class Overriding {
  
  public class ParentClass {
    public void Parent() {
      System.out.println("Parent Method");
    }
  }
  
  public class ChildClass1 extends ParentClass {
    public void Parent() {
      System.out.println("Child1 Method");
    }
  }
  
  public class ChildClass2 extends ParentClass {
    public void Parent() {
      System.out.println("Child2 Method");
    }
  }
  
  public static void main(String[] args){
        Overriding over = new Overriding();
        
        ParentClass pc = over.new ParentClass();
        pc.Parent(); // Parent Method
        
        ParentClass pc1 = over.new ChildClass1();
        pc1.Parent(); // Child1 Method
        
        ParentClass pc2 = over.new ChildClass2();
        pc2.Parent(); // Child2 Method
        
        ChildClass1 cc1 = over.new ChildClass1();
        cc1.Parent(); // Child1 Method
        
        ChildClass2 cc2 = over.new ChildClass2();
        cc2.Parent(); // Child2 Method
    }
    
  }
  
```
