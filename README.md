# OOP
Object-Oriented Programming (OOP) in Java language with examples

---

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

### Structure

    public class ClassName {
        public static void main(String[] args) {
            // statements
        }
    }

### Example

    public class Main {
        public static void main(String[] args) {
            System.out.println("Hello World");
        }
    }

[⬆ Back to Topics](#topics)

---

## Loop

### For Loop Structure

    for(initialization; condition; update) {
        // statements
    }

### For Loop Example

    for(int i = 1; i <= 5; i++) {
        System.out.println(i);
    }

### While Loop Structure

    while(condition) {
        // statements
    }

### While Loop Example

    int i = 1;

    while(i <= 5) {
        System.out.println(i);
        i++;
    }

### Do-While Loop Structure

    do {
        // statements
    } while(condition);

### Do-While Loop Example

    int i = 1;

    do {
        System.out.println(i);
        i++;
    } while(i <= 5);

[⬆ Back to Topics](#topics)

---

## Array

### Structure

    dataType[] arrayName = new dataType[size];

### Example

    int[] numbers = new int[5];

    numbers[0] = 10;
    numbers[1] = 20;
    numbers[2] = 30;

    System.out.println(numbers[0]);

### Array Initialization Structure

    dataType[] arrayName = {value1, value2, value3};

### Example

    int[] numbers = {10, 20, 30, 40, 50};

    for(int i = 0; i < numbers.length; i++) {
        System.out.println(numbers[i]);
    }

[⬆ Back to Topics](#topics)

---

## Method

### Structure

    returnType methodName(parameters) {
        // statements
        return value;
    }

### Example

    class Calculator {

        int add(int a, int b) {
            return a + b;
        }

        public static void main(String[] args) {
            Calculator c = new Calculator();
            System.out.println(c.add(10, 20));
        }
    }

[⬆ Back to Topics](#topics)

---

# 2. OOP

## Class and Object

### Class Structure

    class ClassName {
        dataType variableName;

        returnType methodName() {
            // statements
        }
    }

### Class Example

    class Student {

        String name;
        int age;

        void display() {
            System.out.println(name);
            System.out.println(age);
        }
    }

### Object Structure

    ClassName objectName = new ClassName();

### Object Example

    Student s1 = new Student();

    s1.name = "Rahim";
    s1.age = 20;

    s1.display();

[⬆ Back to Topics](#topics)

---

## Constructor

### Structure

    class ClassName {

        ClassName() {
            // constructor body
        }
    }

### Example

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

### Parameterized Constructor Structure

    ClassName(dataType parameter) {
        // statements
    }

### Example

    class Student {

        String name;
        int age;

        Student(String name, int age) {
            this.name = name;
            this.age = age;
        }
    }

[⬆ Back to Topics](#topics)

---

## Method Overloading

### Structure

    returnType methodName(dataType parameter) {
        // statements
    }

    returnType methodName(dataType parameter1, dataType parameter2) {
        // statements
    }

### Example

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

[⬆ Back to Topics](#topics)

---

## Method Overriding

### Structure

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

### Example

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

[⬆ Back to Topics](#topics)

---

## Inheritance

### Structure

    class Parent {
        // parent members
    }

    class Child extends Parent {
        // child members
    }

### Example

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

[⬆ Back to Topics](#topics)

---

## Polymorphism

### Structure

    Parent objectName = new Child();

    objectName.methodName();

### Example

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

[⬆ Back to Topics](#topics)

---

## Abstraction

### Structure

    abstract class ClassName {

        abstract void methodName();
    }

### Example

    abstract class Shape {

        abstract void draw();
    }

    class Circle extends Shape {

        void draw() {
            System.out.println("Drawing Circle");
        }

        public static void main(String[] args) {

            Circle c = new Circle();

            c.draw();
        }
    }

[⬆ Back to Topics](#topics)

---

## Interface

### Structure

    interface InterfaceName {

        void methodName();
    }

    class ClassName implements InterfaceName {

        public void methodName() {
            // statements
        }
    }

### Example

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

[⬆ Back to Topics](#topics)

---

## Encapsulation

### Structure

    class ClassName {

        private dataType variableName;

        public void setVariable(dataType value) {
            variableName = value;
        }

        public dataType getVariable() {
            return variableName;
        }
    }

### Example

    class Student {

        private String name;

        public void setName(String name) {
            this.name = name;
        }

        public String getName() {
            return name;
        }

        public static void main(String[] args) {

            Student s = new Student();

            s.setName("Rahim");

            System.out.println(s.getName());
        }
    }

[⬆ Back to Topics](#topics)

---

## Access Modifiers

### Private Structure

    private dataType variableName;

### Private Example

    class Student {
        private int age = 20;
    }

### Public Structure

    public dataType variableName;

### Public Example

    class Student {
        public String name = "Rahim";
    }

### Default Structure

    dataType variableName;

### Default Example

    class Student {
        int age = 20;
    }

### Protected Structure

    protected dataType variableName;

### Protected Example

    class Parent {

        protected int number = 10;
    }

    class Child extends Parent {

        void display() {
            System.out.println(number);
        }
    }

[⬆ Back to Topics](#topics)

---

## Exception Handling

### try-catch Structure

    try {
        // risky code
    }
    catch(ExceptionType e) {
        // handling code
    }

### Example

    try {
        int x = 10 / 0;
    }
    catch(ArithmeticException e) {
        System.out.println("Cannot divide by zero");
    }

### finally Structure

    try {
        // code
    }
    catch(Exception e) {
        // handling
    }
    finally {
        // always executes
    }

### Example

    try {
        int x = 10 / 2;
    }
    catch(Exception e) {
        System.out.println(e);
    }
    finally {
        System.out.println("Done");
    }

### throw Structure

    throw new ExceptionType("message");

### Example

    int age = 15;

    if(age < 18) {
        throw new ArithmeticException("Not eligible");
    }

### throws Structure

    returnType methodName() throws ExceptionType {
        // code
    }

### Example

    import java.io.IOException;

    class Test {

        static void readFile() throws IOException {
            System.out.println("Reading file");
        }
    }

[⬆ Back to Topics](#topics)

---

## Package

### Import Package Structure

    import packageName.ClassName;

### Example

    import java.util.Scanner;

    class Main {

        public static void main(String[] args) {

            Scanner sc = new Scanner(System.in);

            int n = sc.nextInt();

            System.out.println(n);
        }
    }

### Create Package Structure

    package packageName;

### Example

    package mypack;

    public class Message {

        public void show() {
            System.out.println("Hello");
        }
    }

[⬆ Back to Topics](#topics)

---

## Static

### Static Variable Structure

    static dataType variableName;

### Example

    class Student {

        static String university = "University";
    }

### Static Method Structure

    static returnType methodName() {
        // statements
    }

### Example

    class Test {

        static void display() {
            System.out.println("Hello");
        }

        public static void main(String[] args) {
            display();
        }
    }

### Static Block Structure

    static {
        // statements
    }

### Example

    class Test {

        static {
            System.out.println("Static Block");
        }

        public static void main(String[] args) {
            System.out.println("Main Method");
        }
    }

[⬆ Back to Topics](#topics)

---

## Inner Class

### Structure

    class Outer {

        class Inner {
            // statements
        }
    }

### Example

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

[⬆ Back to Topics](#topics)

---

## ArrayList

### Structure

    import java.util.ArrayList;

    ArrayList<DataType> listName =
        new ArrayList<DataType>();

### Example

    import java.util.ArrayList;

    class Main {

        public static void main(String[] args) {

            ArrayList<Integer> numbers =
                new ArrayList<Integer>();

            numbers.add(10);
            numbers.add(20);
            numbers.add(30);

            System.out.println(numbers);
        }
    }

### ArrayList Methods Structure

    listName.add(value);
    listName.get(index);
    listName.set(index, value);
    listName.remove(index);
    listName.size();

### Example

    ArrayList<String> names = new ArrayList<>();

    names.add("Rahim");
    names.add("Karim");

    System.out.println(names.get(0));

    names.set(0, "Hasan");

    names.remove(1);

    System.out.println(names.size());

[⬆ Back to Topics](#topics)

---

## File Handling

### Structure

    import java.io.File;

    File fileName = new File("fileName");

### Example

    import java.io.File;
    import java.io.IOException;

    class Main {

        public static void main(String[] args) {

            try {

                File file = new File("demo.txt");

                if(file.createNewFile()) {
                    System.out.println("File created");
                }

            }
            catch(IOException e) {
                System.out.println("Error occurred");
            }
        }
    }

[⬆ Back to Topics](#topics)

---

## GUI

### JFrame Structure

    import javax.swing.*;

    JFrame frame = new JFrame();

    frame.setSize(width, height);

    frame.setVisible(true);

### Example

    import javax.swing.*;

    class Main {

        public static void main(String[] args) {

            JFrame frame = new JFrame("My GUI");

            frame.setSize(400, 300);

            frame.setVisible(true);

            frame.setDefaultCloseOperation(
                JFrame.EXIT_ON_CLOSE
            );
        }
    }

### JButton Structure

    JButton button = new JButton("Button");

    frame.add(button);

### Example

    import javax.swing.*;

    class Main {

        public static void main(String[] args) {

            JFrame frame = new JFrame("GUI");

            JButton button = new JButton("Click");

            frame.add(button);

            frame.setSize(300, 200);

            frame.setVisible(true);
        }
    }

[⬆ Back to Topics](#topics)

---

## Thread

### Extending Thread Structure

    class ClassName extends Thread {

        public void run() {
            // task
        }
    }

### Example

    class MyThread extends Thread {

        public void run() {
            System.out.println("Thread is running");
        }

        public static void main(String[] args) {

            MyThread t1 = new MyThread();

            t1.start();
        }
    }

### Runnable Structure

    class ClassName implements Runnable {

        public void run() {
            // task
        }
    }

### Example

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

[⬆ Back to Topics](#topics)
