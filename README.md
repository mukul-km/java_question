# java_question
# Java OOP Output-Based MCQ Questions

## 1. Classes and Objects

### Question 1
What is the output of the following code?

```java
class Test {
    int x = 10;
    
    public static void main(String[] args) {
        Test t1 = new Test();
        Test t2 = new Test();
        t1.x = 20;
        System.out.print(t1.x + " ");
        System.out.print(t2.x);
    }
}
```

a) 10 10  
b) 20 10  
c) 20 20  
d) 10 20  

### Question 2
What is the output of the following code?

```java
class Counter {
    static int count = 0;
    
    Counter() {
        count++;
    }
    
    public static void main(String[] args) {
        Counter c1 = new Counter();
        Counter c2 = new Counter();
        Counter c3 = new Counter();
        System.out.println(c1.count + " " + c2.count + " " + c3.count);
    }
}
```

a) 1 2 3  
b) 3 3 3  
c) 3 2 1  
d) 1 1 1  

## 2. Inheritance

### Question 3
What is the output of the following code?

```java
class Parent {
    int value = 10;
}

class Child extends Parent {
    int value = 20;
}

public class Test {
    public static void main(String[] args) {
        Parent p = new Child();
        System.out.println(p.value);
    }
}
```

a) 10  
b) 20  
c) Compilation Error  
d) Runtime Error  

### Question 4
What is the output of the following code?

```java
class Base {
    int x = 10;
    
    Base() {
        System.out.print("Base ");
    }
}

class Derived extends Base {
    int y = 20;
    
    Derived() {
        System.out.print("Derived ");
    }
}

public class Test {
    public static void main(String[] args) {
        Derived d = new Derived();
    }
}
```

a) Base  
b) Derived  
c) Base Derived  
d) Derived Base  

## 3. Polymorphism

### Question 5
What is the output of the following code?

```java
class Animal {
    void sound() {
        System.out.println("Animal makes sound");
    }
}

class Dog extends Animal {
    void sound() {
        System.out.println("Dog barks");
    }
}

public class Test {
    public static void main(String[] args) {
        Animal a = new Dog();
        a.sound();
    }
}
```

a) Animal makes sound  
b) Dog barks  
c) Compilation Error  
d) Runtime Error  

### Question 6
What is the output of the following code?

```java
class Shape {
    void draw() {
        System.out.println("Drawing Shape");
    }
    
    void area() {
        System.out.println("Calculate Area");
    }
}

class Circle extends Shape {
    void draw() {
        System.out.println("Drawing Circle");
    }
    
    void circleSpecific() {
        System.out.println("Circle Specific");
    }
}

public class Test {
    public static void main(String[] args) {
        Shape s = new Circle();
        s.draw();
        s.area();
        s.circleSpecific();
    }
}
```

a) Drawing Circle, Calculate Area, Circle Specific  
b) Drawing Circle, Calculate Area, Compilation Error  
c) Drawing Circle, Calculate Area, Runtime Error  
d) Drawing Shape, Calculate Area, Runtime Error  

## 4. Method Overloading

### Question 7
What is the output of the following code?

```java
class OverloadTest {
    static void display(int x) {
        System.out.print("Integer: " + x);
    }
    
    static void display(String s) {
        System.out.print("String: " + s);
    }
    
    public static void main(String[] args) {
        display(10);
        display("Hello");
    }
}
```

a) Integer: 10String: Hello  
b) Integer: 10 String: Hello  
c) String: Hello Integer: 10  
d) Compilation Error  

### Question 8
What is the output of the following code?

```java
class Calculator {
    int add(int a, int b) {
        return a + b;
    }
    
    double add(int a, int b) {
        return a + b + 0.0;
    }
    
    public static void main(String[] args) {
        Calculator calc = new Calculator();
        System.out.println(calc.add(5, 10));
    }
}
```

a) 15  
b) 15.0  
c) Compilation Error  
d) Runtime Error  

## 5. Method Overriding

### Question 9
What is the output of the following code?

```java
class Parent {
    void show() {
        System.out.println("Parent's show()");
    }
}

class Child extends Parent {
    void show() {
        System.out.println("Child's show()");
    }
}

public class Main {
    public static void main(String[] args) {
        Parent obj1 = new Parent();
        Parent obj2 = new Child();
        obj1.show();
        obj2.show();
    }
}
```

a) Parent's show() Parent's show()  
b) Child's show() Child's show()  
c) Parent's show() Child's show()  
d) Child's show() Parent's show()  

### Question 10
What is the output of the following code?

```java
class Base {
    private void show() {
        System.out.println("Base::show()");
    }
}

class Derived extends Base {
    public void show() {
        System.out.println("Derived::show()");
    }
}

public class Main {
    public static void main(String[] args) {
        Base b = new Derived();
        b.show();
    }
}
```

a) Base::show()  
b) Derived::show()  
c) Compilation Error  
d) Runtime Error  

## 6. Constructors and Constructor Chaining

### Question 11
What is the output of the following code?

```java
class Parent {
    Parent() {
        System.out.println("Parent Constructor");
    }
}

class Child extends Parent {
    Child() {
        System.out.println("Child Constructor");
    }
}

public class Test {
    public static void main(String[] args) {
        Child c = new Child();
    }
}
```

a) Parent Constructor  
b) Child Constructor  
c) Parent Constructor Child Constructor  
d) Child Constructor Parent Constructor  

### Question 12
What is the output of the following code?

```java
class MyClass {
    MyClass() {
        this(10);
        System.out.println("Default Constructor");
    }
    
    MyClass(int x) {
        System.out.println("Parameterized Constructor with value " + x);
    }
    
    public static void main(String[] args) {
        MyClass obj = new MyClass();
    }
}
```

a) Default Constructor  
b) Parameterized Constructor with value 10  
c) Parameterized Constructor with value 10 Default Constructor  
d) Default Constructor Parameterized Constructor with value 10  

## 7. Abstraction and Abstract Classes

### Question 13
What is the output of the following code?

```java
abstract class AbstractClass {
    AbstractClass() {
        System.out.println("Abstract Class Constructor");
    }
    
    abstract void abstractMethod();
    
    void concreteMethod() {
        System.out.println("Concrete Method");
    }
}

class ConcreteClass extends AbstractClass {
    ConcreteClass() {
        System.out.println("Concrete Class Constructor");
    }
    
    void abstractMethod() {
        System.out.println("Abstract Method Implementation");
    }
}

public class Test {
    public static void main(String[] args) {
        ConcreteClass obj = new ConcreteClass();
        obj.abstractMethod();
        obj.concreteMethod();
    }
}
```

a) Abstract Class Constructor Concrete Class Constructor Abstract Method Implementation Concrete Method  
b) Concrete Class Constructor Abstract Method Implementation Concrete Method  
c) Abstract Class Constructor Abstract Method Implementation Concrete Method  
d) Compilation Error  

### Question 14
What is the output of the following code?

```java
abstract class Shape {
    abstract double area();
    
    Shape() {
        System.out.println("Shape created");
    }
}

class Circle extends Shape {
    double radius;
    
    Circle(double r) {
        radius = r;
        System.out.println("Circle created");
    }
    
    double area() {
        return 3.14 * radius * radius;
    }
}

public class Test {
    public static void main(String[] args) {
        Circle c = new Circle(5.0);
        System.out.println("Area: " + c.area());
    }
}
```

a) Shape created Circle created Area: 78.5  
b) Circle created Area: 78.5  
c) Shape created Area: 78.5  
d) Area: 78.5  

## 8. Interfaces

### Question 15
What is the output of the following code?

```java
interface Printable {
    void print();
    
    default void show() {
        System.out.println("Default Show");
    }
}

class PrintableImpl implements Printable {
    public void print() {
        System.out.println("Print");
    }
}

public class Test {
    public static void main(String[] args) {
        Printable p = new PrintableImpl();
        p.print();
        p.show();
    }
}
```

a) Print Default Show  
b) Default Show Print  
c) Print  
d) Compilation Error  

### Question 16
What is the output of the following code?

```java
interface A {
    default void show() {
        System.out.println("A's show");
    }
}

interface B {
    default void show() {
        System.out.println("B's show");
    }
}

class C implements A, B {
    public void show() {
        System.out.println("C's show");
    }
}

public class Test {
    public static void main(String[] args) {
        C c = new C();
        c.show();
    }
}
```

a) A's show  
b) B's show  
c) C's show  
d) Compilation Error  

## 9. Access Modifiers

### Question 17
What is the output of the following code?

```java
class Parent {
    protected int x = 10;
}

class Child extends Parent {
    private int x = 20;
    
    void display() {
        System.out.println("x = " + x);
        System.out.println("super.x = " + super.x);
    }
}

public class Test {
    public static void main(String[] args) {
        Child c = new Child();
        c.display();
    }
}
```

a) x = 10 super.x = 10  
b) x = 20 super.x = 10  
c) x = 20 super.x = 20  
d) Compilation Error  

### Question 18
What is the output of the following code?

```java
class MyClass {
    private int x = 10;
    
    class Inner {
        private int x = 20;
        
        void display() {
            System.out.println(x);
            System.out.println(MyClass.this.x);
        }
    }
    
    public static void main(String[] args) {
        MyClass.Inner inner = new MyClass().new Inner();
        inner.display();
    }
}
```

a) 10 10  
b) 20 10  
c) 20 20  
d) 10 20  

## 10. Static Methods and Variables

### Question 19
What is the output of the following code?

```java
class StaticTest {
    static int x = 10;
    
    static {
        x += 5;
    }
    
    static {
        x += 10;
    }
    
    public static void main(String[] args) {
        System.out.println(x);
    }
}
```

a) 10  
b) 15  
c) 20  
d) 25  

### Question 20
What is the output of the following code?

```java
class Parent {
    static void display() {
        System.out.println("Parent's static method");
    }
}

class Child extends Parent {
    static void display() {
        System.out.println("Child's static method");
    }
}

public class Test {
    public static void main(String[] args) {
        Parent p = new Child();
        p.display();
    }
}
```

a) Parent's static method  
b) Child's static method  
c) Compilation Error  
d) Runtime Error  

## 11. Final Keyword

### Question 21
What is the output of the following code?

```java
class Parent {
    final void show() {
        System.out.println("Parent's show()");
    }
}

class Child extends Parent {
    void show() {
        System.out.println("Child's show()");
    }
    
    public static void main(String[] args) {
        Child c = new Child();
        c.show();
    }
}
```

a) Parent's show()  
b) Child's show()  
c) Compilation Error  
d) Runtime Error  

### Question 22
What is the output of the following code?

```java
class FinalTest {
    final int x;
    
    {
        x = 10;
    }
    
    FinalTest() {
        x = 20;
    }
    
    public static void main(String[] args) {
        FinalTest ft = new FinalTest();
        System.out.println(ft.x);
    }
}
```

a) 10  
b) 20  
c) 0  
d) Compilation Error  

## 12. Super and this Keywords

### Question 23
What is the output of the following code?

```java
class Parent {
    int x = 10;
}

class Child extends Parent {
    int x = 20;
    
    void display() {
        System.out.println(this.x);
        System.out.println(super.x);
    }
    
    public static void main(String[] args) {
        Child c = new Child();
        c.display();
    }
}
```

a) 10 10  
b) 20 10  
c) 20 20  
d) 10 20  

### Question 24
What is the output of the following code?

```java
class Parent {
    Parent() {
        System.out.println("Parent Constructor");
    }
    
    Parent(int x) {
        this();
        System.out.println("Parent Parameterized Constructor");
    }
}

class Child extends Parent {
    Child() {
        super(10);
        System.out.println("Child Constructor");
    }
}

public class Test {
    public static void main(String[] args) {
        Child c = new Child();
    }
}
```

a) Parent Constructor Child Constructor  
b) Parent Parameterized Constructor Child Constructor  
c) Parent Constructor Parent Parameterized Constructor Child Constructor  
d) Child Constructor Parent Constructor Parent Parameterized Constructor  

## 13. Method Hiding

### Question 25
What is the output of the following code?

```java
class Base {
    static void display() {
        System.out.println("Static method in Base");
    }
}

class Derived extends Base {
    static void display() {
        System.out.println("Static method in Derived");
    }
}

public class Test {
    public static void main(String[] args) {
        Base b = new Derived();
        b.display();
        Derived.display();
    }
}
```

a) Static method in Base Static method in Derived  
b) Static method in Derived Static method in Derived  
c) Static method in Base Static method in Base  
d) Static method in Derived Static method in Base  

### Question 26
What is the output of the following code?

```java
class Parent {
    static void staticMethod() {
        System.out.println("Parent's static method");
    }
    
    void instanceMethod() {
        System.out.println("Parent's instance method");
    }
}

class Child extends Parent {
    static void staticMethod() {
        System.out.println("Child's static method");
    }
    
    void instanceMethod() {
        System.out.println("Child's instance method");
    }
}

public class Test {
    public static void main(String[] args) {
        Parent p = new Child();
        p.staticMethod();
        p.instanceMethod();
    }
}
```

a) Parent's static method Parent's instance method  
b) Child's static method Child's instance method  
c) Parent's static method Child's instance method  
d) Child's static method Parent's instance method  

## 14. Inner Classes

### Question 27
What is the output of the following code?

```java
class Outer {
    private int outerVar = 10;
    
    class Inner {
        private int innerVar = 20;
        
        void display() {
            System.out.println("outerVar = " + outerVar);
            System.out.println("innerVar = " + innerVar);
        }
    }
    
    public static void main(String[] args) {
        Outer.Inner inner = new Outer().new Inner();
        inner.display();
    }
}
```

a) outerVar = 10 innerVar = 20  
b) outerVar = 20 innerVar = 10  
c) Compilation Error  
d) Runtime Error  

### Question 28
What is the output of the following code?

```java
class Outer {
    private int outerVar = 10;
    
    static class StaticNested {
        private int nestedVar = 20;
        
        void display() {
            System.out.println("nestedVar = " + nestedVar);
            System.out.println("outerVar = " + new Outer().outerVar);
        }
    }
    
    public static void main(String[] args) {
        Outer.StaticNested nested = new Outer.StaticNested();
        nested.display();
    }
}
```

a) nestedVar = 20 outerVar = 10  
b) nestedVar = 10 outerVar = 20  
c) Compilation Error  
d) Runtime Error  

## 15. Anonymous Classes

### Question 29
What is the output of the following code?

```java
interface Greeting {
    void greet();
}

public class Test {
    public static void main(String[] args) {
        Greeting g = new Greeting() {
            public void greet() {
                System.out.println("Hello, World!");
            }
        };
        g.greet();
    }
}
```

a) Hello, World!  
b) Compilation Error  
c) Runtime Error  
d) No output  

### Question 30
What is the output of the following code?

```java
class Outer {
    void outerMethod() {
        final int x = 10;
        
        class LocalInner {
            void innerMethod() {
                System.out.println(x);
            }
        }
        
        LocalInner inner = new LocalInner();
        inner.innerMethod();
    }
    
    public static void main(String[] args) {
        Outer outer = new Outer();
        outer.outerMethod();
    }
}
```

a) 10  
b) Compilation Error  
c) Runtime Error  
d) 0  

### Question 31
What is the output of the following code?

```java
class Base {
    void method() {
        System.out.println("Base method");
    }
}

class Derived extends Base {
    void method() {
        System.out.println("Derived method");
    }
    
    void callMethod() {
        super.method();
        this.method();
        method();
    }
}

public class Test {
    public static void main(String[] args) {
        Derived d = new Derived();
        d.callMethod();
    }
}
```

a) Base method Derived method Derived method  
b) Derived method Derived method Derived method  
c) Base method Base method Base method  
d) Derived method Base method Derived method  

### Question 32
What is the output of the following code?

```java
class Test {
    int x = 10;
    
    Test() {
        System.out.print(x + " ");
        x = 20;
    }
    
    {
        System.out.print(x + " ");
        x = 30;
    }
    
    public static void main(String[] args) {
        Test t = new Test();
        System.out.print(t.x);
    }
}
```

a) 10 30 20  
b) 10 10 20  
c) 30 10 20  
d) 10 20 30  

### Question 33
What is the output of the following code?

```java
class Base {
    int getValue() {
        return 1;
    }
}

class Derived extends Base {
    int getValue() {
        return 2;
    }
}

public class Test {
    public static void main(String[] args) {
        Base b = new Derived();
        System.out.println(b.getValue());
    }
}
```

a) 1  
b) 2  
c) Compilation Error  
d) Runtime Error  

### Question 34
What is the output of the following code?

```java
class Test {
    int i = 1;
    
    Test() {
        i = 2;
        display();
    }
    
    void display() {
        System.out.println(i);
    }
}

class SubTest extends Test {
    int i = 3;
    
    SubTest() {
        i = 4;
    }
    
    void display() {
        System.out.println(i);
    }
    
    public static void main(String[] args) {
        Test t = new SubTest();
    }
}
```

a) 1  
b) 2  
c) 3  
d) 4  

### Question 35
What is the output of the following code?

```java
class Parent {
    void m1() {
        System.out.println("Parent m1");
    }
}

class Child extends Parent {
    void m1() {
        System.out.println("Child m1");
    }
    
    void m2() {
        System.out.println("Child m2");
    }
}

public class Test {
    public static void main(String[] args) {
        Parent p = new Child();
        p.m1();
        p.m2();
    }
}
```

a) Child m1 Child m2  
b) Parent m1 Child m2  
c) Child m1 Compilation Error  
d) Parent m1 Compilation Error  

### Question 36
What is the output of the following code?

```java
class Parent {
    {
        System.out.println("Parent instance block");
    }
    
    static {
        System.out.println("Parent static block");
    }
    
    Parent() {
        System.out.println("Parent constructor");
    }
}

class Child extends Parent {
    {
        System.out.println("Child instance block");
    }
    
    static {
        System.out.println("Child static block");
    }
    
    Child() {
        System.out.println("Child constructor");
    }
    
    public static void main(String[] args) {
        Child c = new Child();
    }
}
```

a) Parent static block Child static block Parent instance block Parent constructor Child instance block Child constructor  
b) Parent static block Child static block Parent constructor Child constructor  
c) Parent instance block Parent constructor Child instance block Child constructor  
d) Child static block Parent static block Child instance block Child constructor  

### Question 37
What is the output of the following code?

```java
interface A {
    int x = 10;
}

interface B {
    int x = 20;
}

class C implements A, B {
    public static void main(String[] args) {
        System.out.println(x);
    }
}
```

a) 10  
b) 20  
c) Compilation Error  
d) Runtime Error  

### Question 38
What is the output of the following code?

```java
class A {
    int x = 10;
    
    class B {
        int x = 20;
        
        class C {
            int x = 30;
            
            void display() {
                System.out.println(x);
                System.out.println(this.x);
                System.out.println(B.this.x);
                System.out.println(A.this.x);
            }
        }
    }
    
    public static void main(String[] args) {
        A a = new A();
        A.B b = a.new B();
        A.B.C c = b.new C();
        c.display();
    }
}
```

a) 30 30 20 10  
b) 10 20 30 30  
c) 10 10 20 30  
d) 30 30 30 30  

### Question 39
What is the output of the following code?

```java
class Test {
    static int i = 10;
    
    static {
        i = 20;
    }
    
    static {
        i = 30;
    }
    
    public static void main(String[] args) {
        System.out.println(i);
    }
}
```

a) 10  
b) 20  
c) 30  
d) Compilation Error  

### Question 40
What is the output of the following code?

```java
class Base {
    final void show() {
        System.out.println("Base show");
    }
}

class Derived extends Base {
    void show() {
        System.out.println("Derived show");
    }
    
    public static void main(String[] args) {
        Derived d = new Derived();
        d.show();
    }
}
```

a) Base show  
b) Derived show  
c) Compilation Error  
d) Runtime Error  

### Question 41
What is the output of the following code?

```java
class A {
    void methodA() {
        System.out.println("Method A");
    }
}

class B extends A {
    void methodB() {
        System.out.println("Method B");
    }
}

public class Test {
    public static void main(String[] args) {
        A a = new B();
        B b = (B) a;
        b.methodB();
    }
}
```

a) Method B  
b) Method A  
c) Compilation Error  
d) Runtime Error  

### Question 42
What is the output of the following code?

```java
class Test {
    private static int counter = 0;
    
    public static void main(String[] args) {
        Test t1 = new Test();
        Test t2 = new Test();
        t1.counter = 10;
        t2.counter = 20;
        System.out.println(t1.counter);
    }
}
```

a) 0  
b) 10  
c) 20  
d) Compilation Error  

### Question 43
What is the output of the following code?

```java
class Parent {
    int value = 100;
    
    Parent() {
        print();
    }
    
    void print() {
        System.out.println("Parent value: " + value);
    }
}

class Child extends Parent {
    int value = 200;
    
    Child() {
        print();
    }
    
    void print() {
        System.out.println("Child value: " + value);
    }
    
    public static void main(String[] args) {
        Parent p = new Child();
    }
}
```

a) Parent value: 100 Child value: 200  
b) Parent value: 100 Child value: 0  
c) Child value: 0 Child value: 200  
d) Child value: 0 Child value: 0  

### Question 44
What is the output of the following code?

```java
class Test {
    static int i = 0;
    
    static {
        i = 1;
        System.out.print(i + " ");
    }
    
    public static void main(String[] args) {
        System.out.print(i + " ");
        i = 2;
        System.out.print(i);
    }
}
```

a) 0 1 2  
b) 1 1 2  
c) 1 2 2  
d) 0 0 2  

### Question 45
What is the output of the following code?

```java
abstract class Shape {
    Shape() {
        System.out.println("Shape constructor");
    }
    
    abstract void draw();
}

class Circle extends Shape {
    Circle() {
        System.out.println("Circle constructor");
    }
    
    void draw() {
        System.out.println("Draw Circle");
    }
}

public class Test {
    public static void main(String[] args) {
        Shape s = new Circle();
        s.draw();
    }
}
```

a) Shape constructor Circle constructor Draw Circle  
b) Circle constructor Draw Circle  
c) Shape constructor Draw Circle  
d) Draw Circle  

### Question 46
What is the output of the following code?

```java
class A {
    String s = "Class A";
}

class B extends A {
    String s = "Class B";
    
    {
        System.out.println(super.s);
    }
}

class C extends B {
    String s = "Class C";
    
    {
        System.out.println(super.s);
    }
}

public class Test {
    public static void main(String[] args) {
        C c = new C();
        System.out.println(c.s);
    }
}
```

a) Class A Class B Class C  
b) Class C  
c) Class A Class C  
d) Class B Class C  

### Question 47
What is the output of the following code?

```java
class Test {
    int x = 10;
    
    class Inner {
        int x = 20;
        
        void display() {
            int x = 30;
            System.out.println(x);
            System.out.println(this.x);
            System.out.println(Test.this.x);
        }
    }
    
    public static void main(String[] args) {
        Test.Inner inner = new Test().new Inner();
        inner.display();
    }
}
```

a) 10 20 30  
b) 30 20 10  
c) 30 30 30  
d) 10 10 10  

### Question 48
What is the output of the following code?

```java
class A {
    static void staticMethod() {
        System.out.println("A's static method");
    }
}

class B extends A {
    static void staticMethod() {
        System.out.println("B's static method");
    }
}

public class Test {
    public static void main(String[] args) {
        A a = null;
        B b = null;
        a.staticMethod();
        b.staticMethod();
    }
}
```

a) A's static method B's static method  
b) NullPointerException  
c) Compilation Error  
d) Runtime Error  

### Question 49
What is the output of the following code?

```java
class Test {
    public static void main(String[] args) {
        try {
            throw new Exception("Exception occurred");
        } catch (Exception e) {
            System.out.println("Caught: " + e.getMessage());
        } finally {
            System.out.println("Finally block executed");
        }
    }
}
```

a) Caught: Exception occurred  
b) Finally block executed  
c) Caught: Exception occurred Finally block executed  
d) Compilation Error  

### Question 50
What is the output of the following code?

```java
interface I1 {
    void method();
}

interface I2 {
    void method();
}

class MyClass implements I1, I2 {
    public void method() {
        System.out.println("Method implementation");
    }
    
    public static void main(String[] args) {
        MyClass obj = new MyClass();
        obj.method();
    }
}
```

a) Method implementation  
b) Compilation Error  
c) Runtime Error  
d) No output  

### Question 51
What is the output of the following code?

```java
class Test {
    public static void main(String[] args) {
        Integer i1 = 127;
        Integer i2 = 127;
        System.out.print(i1 == i2);
        
        Integer i3 = 128;
        Integer i4 = 128;
        System.out.print(" " + (i3 == i4));
    }
}
```

a) true true  
b) false false  
c) true false  
d) false true  

### Question 52
What is the output of the following code?

```java
class Super {
    static String greeting() {
        return "Goodnight";
    }
    
    String name() {
        return "Richard";
    }
}

class Sub extends Super {
    static String greeting() {
        return "Hello";
    }
    
    String name() {
        return "Dick";
    }
}

class Test {
    public static void main(String[] args) {
        Super s = new Sub();
        System.out.println(s.greeting() + ", " + s.name());
    }
}
```

a) Goodnight, Richard  
b) Hello, Dick  
c) Goodnight, Dick  
d) Hello, Richard  

## Answers

1. b) 20 10
2. b) 3 3 3
3. a) 10
4. c) Base Derived
5. b) Dog barks
6. c) Drawing Circle, Calculate Area, Runtime Error
7. a) Integer: 10String: Hello
8. c) Compilation Error
9. c) Parent's show() Child's show()
10. c) Compilation Error
11. c) Parent Constructor Child Constructor
12. c) Parameterized Constructor with value 10 Default Constructor
13. a) Abstract Class Constructor Concrete Class Constructor Abstract Method Implementation Concrete Method
14. a) Shape created Circle created Area: 78.5
15. a) Print Default Show
16. c) C's show
17. b) x = 20 super.x = 10
18. b) 20 10
19. d) 25
20. a) Parent's static method
21. c) Compilation Error
22. d) Compilation Error
23. b) 20 10
24. c) Parent Constructor Parent Parameterized Constructor Child Constructor
25. a) Static method in Base Static method in Derived
26. c) Parent's static method Child's instance method
27. a) outerVar = 10 innerVar = 20
28. a) nestedVar = 20 outerVar = 10
29. a) Hello, World!
30. a) 10
31. a) Base method Derived method Derived method
32. a) 10 30 20
33. b) 2
34. d) 4
35. c) Child m1 Compilation Error
36. a) Parent static block Child static block Parent instance block Parent constructor Child instance block Child constructor
37. c) Compilation Error
38. a) 30 30 20 10
39. c) 30
40. c) Compilation Error
41. a) Method B
42. c) 20
43. c) Child value: 0 Child value: 200
44. b) 1 1 2
45. a) Shape constructor Circle constructor Draw Circle
46. a) Class A Class B Class C
47. b) 30 20 10
48. a) A's static method B's static method
49. c) Caught: Exception occurred Finally block executed
50. a) Method implementation
51. c) true false
52. c) Goodnight, Dick
