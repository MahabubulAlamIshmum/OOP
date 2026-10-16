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
