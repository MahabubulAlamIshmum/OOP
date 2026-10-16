# OOP
Object-Oriented Programming (OOP) in Java language with examples

---

# Java OOP Cheatsheet

## Table of Contents

1. [Basic Concept](#1-basic-concept)
   - [Java Structure](#java-structure)
   - [Loop](#loop)
   - [Array](#array)
   - [Method](#method)

2. [OOP](#2-oop)
   - [Class and Object](#class-and-object)
   - [Constructor](#constructor)
   - [Method Overloading](#method-overloading)
   - [Method Overriding](#method-overriding)
   - [Inheritance](#inheritance)
   - [Polymorphism](#polymorphism)
   - [Abstraction](#abstraction)
   - [Interface](#interface)
   - [Encapsulation](#encapsulation)
   - [Access Modifiers](#access-modifiers)
   - [Exception Handling](#exception-handling)
   - [Package](#package)
   - [Static](#static)
   - [Inner Class](#inner-class)
   - [ArrayList](#arraylist)
   - [File Handling](#file-handling)
   - [GUI](#gui)
   - [Thread](#thread)

---

# 1. Basic Concept

## Java Structure

**Structure**

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello World");
         // more statements
    }
}
```

[⬆ Back to Table of Contents](#table-of-contents)

---

## Loop

### For Loop

**Structure**

```java
for(initialization; condition; update) {
    // statements
}
```

**Example**

```java
for(int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

### While Loop

**Structure**

```java
while(condition) {
    // statements
}
```

**Example**

```java
int i = 1;

while(i <= 5) {
    System.out.println(i);
    i++;
}
```

### Do-While Loop

**Structure**

```java
do {
    // statements
} while(condition);
```

**Example**

```java
int i = 1;

do {
    System.out.println(i);
    i++;
} while(i <= 5);
```

[⬆ Back to Table of Contents](#table-of-contents)

---

## Array

**Structure**

```java
dataType[] arrayName = new dataType[size];
```

**Example**

```java
int[] numbers = new int[5];

numbers[0] = 10;
numbers[1] = 20;
numbers[2] = 30;

System.out.println(numbers[0]);
```

### Array Initialization

**Structure**

```java
dataType[] arrayName = {value1, value2, value3};
```

**Example**

```java
int[] numbers = {10, 20, 30, 40, 50};

for(int i = 0; i < numbers.length; i++) {
    System.out.println(numbers[i]);
}
```

[⬆ Back to Table of Contents](#table-of-contents)

---

## Method

**Structure**

```java
returnType methodName(parameters) {
    // statements
    return value;
}
```

**Example**

```java
class Calculator {

    int add(int a, int b) {
        return a + b;
    }

    public static void main(String[] args) {
        Calculator c = new Calculator();
        System.out.println(c.add(10, 20));
    }
}
```

[⬆ Back to Table of Contents](#table-of-contents)

---

# 2. OOP

## Class and Object

### Class

**Structure**

```java
class ClassName {
    dataType variableName;

    returnType methodName() {
        // statements
    }
}
```

**Example**

```java
class Student {
    String name;
    int age;

    void display() {
        System.out.println(name);
        System.out.println(age);
    }
}
```

### Object

**Structure**

```java
ClassName objectName = new ClassName();
```

**Example**

```java
Student s1 = new Student();

s1.name = "Rahim";
s1.age = 20;

s1.display();
```

[⬆ Back to Table of Contents](#table-of-contents)

---

## Constructor

**Structure**

```java
class ClassName {
    ClassName() {
        // constructor body
    }
}
```

**Example**

```java
class Student {
    String name;

    Student() {
        name = "Rahim";
    }

    public static void main(String[] args) {
        Student s = new Student();
        System.out.println(s.name);
    }
}
```

### Parameterized Constructor

**Structure**

```java
ClassName(dataType parameter) {
    // statements
}
```

**Example**

```java
class Student {
    String name;
    int age;

    Student(String name, int age) {
        this.name = name;
        this.age = age;
    }
}
```

[⬆ Back to Table of Contents](#table-of-contents)

---

## Method Overloading

**Structure**

```java
returnType methodName(dataType parameter) {
    // statements
}

returnType methodName(dataType parameter1, dataType parameter2) {
    // statements
}
```

**Example**

```java
class Calculator {

    int add(int a, int b) {
        return a + b;
    }

    int add(int a, int b, int c) {
        return a + b + c;
    }

    public static void main(String[] args) {
        Calculator c = new Calculator();

        System.out.println(c.add(10, 20));
        System.out.println(c.add(10, 20, 30));
    }
}
```

[⬆ Back to Table of Contents](#table-of-contents)

---

## Method Overriding

**Structure**

```java
class Parent {
    void methodName() {
        // parent method
    }
}

class Child extends Parent {
    @Override
    void methodName() {
        // child method
    }
}
```

**Example**

```java
class Animal {
    void sound() {
        System.out.println("Animal makes sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }

    public static void main(String[] args) {
        Dog d = new Dog();
        d.sound();
    }
}
```

[⬆ Back to Table of Contents](#table-of-contents)

---

## Inheritance

**Structure**

```java
class Parent {
    // parent members
}

class Child extends Parent {
    // child members
}
```

**Example**

```java
class Animal {
    void eat() {
        System.out.println("Animal eats");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Dog barks");
    }

    public static void main(String[] args) {
        Dog d = new Dog();
        d.eat();
        d.bark();
    }
}
```

[⬆ Back to Table of Contents](#table-of-contents)

---

## Polymorphism

**Structure**

```java
Parent objectName = new Child();
objectName.methodName();
```

**Example**

```java
class Animal {
    void sound() {
        System.out.println("Animal sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

class Main {
    public static void main(String[] args) {
        Animal a = new Dog();
        a.sound();
    }
}
```

### Compile Time Polymorphism

**Structure**

```java
void method(int a) {
    // statements
}

void method(String a) {
    // statements
}
```

**Example**

```java
class Display {
    void show(int x) {
        System.out.println(x);
    }

    void show(String x) {
        System.out.println(x);
    }

    public static void main(String[] args) {
        Display d = new Display();
        d.show(10);
        d.show("Hello");
    }
}
```

### Run Time Polymorphism

**Structure**

```java
Parent reference = new Child();
reference.method();
```

**Example**

```java
class Animal {
    void sound() {
        System.out.println("Animal sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

class Main {
    public static void main(String[] args) {
        Animal a = new Dog();
        a.sound();
    }
}
```

[⬆ Back to Table of Contents](#table-of-contents)

---

## Abstraction

**Structure**

```java
abstract class ClassName {
    abstract void methodName();
}
```

**Example**

```java
abstract class Shape {
    abstract void draw();
}

class Circle extends Shape {
    @Override
    void draw() {
        System.out.println("Drawing Circle");
    }

    public static void main(String[] args) {
        Circle c = new Circle();
        c.draw();
    }
}
```

[⬆ Back to Table of Contents](#table-of-contents)

---

## Interface

**Structure**

```java
interface InterfaceName {
    void methodName();
}

class ClassName implements InterfaceName {
    public void methodName() {
        // statements
    }
}
```

**Example**

```java
interface Animal {
    void sound();
}

class Dog implements Animal {
    public void sound() {
        System.out.println("Dog barks");
    }

    public static void main(String[] args) {
        Dog d = new Dog();
        d.sound();
    }
}
```

[⬆ Back to Table of Contents](#table-of-contents)

---

## Encapsulation

**Structure**

```java
class ClassName {
    private dataType variableName;

    public void setVariable(dataType value) {
        variableName = value;
    }

    public dataType getVariable() {
        return variableName;
    }
}
```

**Example**

```java
class Student {
    private String name;

    public void setName(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }

    public static void main(String[] args) {
        Student s
```
---

## Access Modifiers

### Private

**Structure**

```java
private dataType variableName;
```

**Example**

```java
class Student {
    private int age = 20;
}
```

### Public

**Structure**

```java
public dataType variableName;
```

**Example**

```java
class Student {
    public String name = "Rahim";
}
```

### Default

**Structure**

```java
dataType variableName;
```

**Example**

```java
class Student {
    int age = 20;
}
```

### Protected

**Structure**

```java
protected dataType variableName;
```

**Example**

```java
class Parent {
    protected int number = 10;
}

class Child extends Parent {
    void display() {
        System.out.println(number);
    }
}
```

[⬆ Back to Table of Contents](#table-of-contents)

---

## Exception Handling

### try-catch

**Structure**

```java
try {
    // risky code
} catch (ExceptionType e) {
    // handling code
}
```

**Example**

```java
class Main {
    public static void main(String[] args) {
        try {
            int x = 10 / 0;
        } catch (ArithmeticException e) {
            System.out.println("Cannot divide by zero");
        }
    }
}
```

### finally

**Structure**

```java
try {
    // code
} catch (Exception e) {
    // handling
} finally {
    // cleanup code
}
```

**Example**

```java
class Main {
    public static void main(String[] args) {
        try {
            int x = 10 / 2;
        } catch (Exception e) {
            System.out.println(e);
        } finally {
            System.out.println("Done");
        }
    }
}
```

### throw

**Structure**

```java
throw new ExceptionType("message");
```

**Example**

```java
class Main {
    public static void main(String[] args) {
        int age = 15;

        if (age < 18) {
            throw new ArithmeticException("Not eligible");
        }
    }
}
```

### throws

**Structure**

```java
returnType methodName() throws ExceptionType {
    // code
}
```

**Example**

```java
import java.io.IOException;

class Test {
    static void readFile() throws IOException {
        System.out.println("Reading file");
    }
}
```

[⬆ Back to Table of Contents](#table-of-contents)

---

## Package

### Import Package

**Structure**

```java
import packageName.ClassName;
```

**Example**

```java
import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        System.out.println(n);
        sc.close();
    }
}
```

### Create Package

**Structure**

```java
package packageName;
```

**Example**

```java
package mypack;

public class Message {
    public void show() {
        System.out.println("Hello");
    }
}
```

[⬆ Back to Table of Contents](#table-of-contents)

---

## Static

### Static Variable

**Structure**

```java
static dataType variableName;
```

**Example**

```java
class Student {
    static String university = "University";
}
```

### Static Method

**Structure**

```java
static returnType methodName() {
    // statements
}
```

**Example**

```java
class Test {
    static void display() {
        System.out.println("Hello");
    }

    public static void main(String[] args) {
        Test.display();
    }
}
```

### Static Block

**Structure**

```java
static {
    // statements
}
```

**Example**

```java
class Test {
    static {
        System.out.println("Static Block");
    }

    public static void main(String[] args) {
        System.out.println("Main Method");
    }
}
```

[⬆ Back to Table of Contents](#table-of-contents)

---

## Inner Class

**Structure**

```java
class Outer {
    class Inner {
        // statements
    }
}
```

**Example**

```java
class Outer {
    int x = 10;

    class Inner {
        void show() {
            System.out.println(x);
        }
    }

    public static void main(String[] args) {
        Outer o = new Outer();
        Outer.Inner i = o.new Inner();
        i.show();
    }
}
```

[⬆ Back to Table of Contents](#table-of-contents)

---

## ArrayList

**Structure**

```java
import java.util.ArrayList;

ArrayList<DataType> listName = new ArrayList<>();
```

**Example**

```java
import java.util.ArrayList;

class Main {
    public static void main(String[] args) {
        ArrayList<Integer> numbers = new ArrayList<>();

        numbers.add(10);
        numbers.add(20);
        numbers.add(30);

        System.out.println(numbers);
    }
}
```

### ArrayList Methods

**Structure**

```java
listName.add(value);
listName.get(index);
listName.set(index, value);
listName.remove(index);
listName.size();
```

**Example**

```java
import java.util.ArrayList;

class Main {
    public static void main(String[] args) {
        ArrayList<String> names = new ArrayList<>();

        names.add("Rahim");
        names.add("Karim");

        System.out.println(names.get(0));

        names.set(0, "Hasan");
        names.remove(1);

        System.out.println(names.size());
    }
}
```

[⬆ Back to Table of Contents](#table-of-contents)

---

## File Handling

**Structure**

```java
import java.io.File;

File fileName = new File("fileName");
```

**Example**

```java
import java.io.File;
import java.io.IOException;

class Main {
    public static void main(String[] args) {
        try {
            File file = new File("demo.txt");

            if (file.createNewFile()) {
                System.out.println("File created");
            } else {
                System.out.println("File already exists");
            }
        } catch (IOException e) {
            System.out.println("Error occurred");
        }
    }
}
```

[⬆ Back to Table of Contents](#table-of-contents)

---

## GUI

### JFrame

**Structure**

```java
import javax.swing.*;

JFrame frame = new JFrame("Title");
frame.setSize(width, height);
frame.setVisible(true);
```

**Example**

```java
import javax.swing.*;

class Main {
    public static void main(String[] args) {
        JFrame frame = new JFrame("My GUI");

        frame.setSize(400, 300);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setVisible(true);
    }
}
```

### JButton

**Structure**

```java
JButton button = new JButton("Button");
frame.add(button);
```

**Example**

```java
import javax.swing.*;
import java.awt.FlowLayout;

class Main {
    public static void main(String[] args) {
        JFrame frame = new JFrame("GUI");
        JButton button = new JButton("Click");

        frame.setLayout(new FlowLayout());
        frame.add(button);
        frame.setSize(300, 200);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setVisible(true);
    }
}
```

[⬆ Back to Table of Contents](#table-of-contents)

---

## Thread

### Extending Thread

**Structure**

```java
class ClassName extends Thread {
    public void run() {
        // task
    }
}
```

**Example**

```java
class MyThread extends Thread {
    public void run() {
        System.out.println("Thread is running");
    }

    public static void main(String[] args) {
        MyThread t1 = new MyThread();
        t1.start();
    }
}
```

### Runnable

**Structure**

```java
class ClassName implements Runnable {
    public void run() {
        // task
    }
}
```

**Example**

```java
class MyTask implements Runnable {
    public void run() {
        System.out.println("Thread is running");
    }

    public static void main(String[] args) {
        MyTask task = new MyTask();
        Thread t = new Thread(task);
        t.start();
    }
}
```

[⬆ Back to Table of Contents](#table-of-contents)

---
