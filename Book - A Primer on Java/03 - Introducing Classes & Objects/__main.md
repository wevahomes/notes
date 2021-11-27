# Introducing Classes & Objects - Main

---

## 3.1 Abstraction

---

- __(*) Introducing classes & objects.__
- __(1) What is abstraction?__

<details>

- (1) The hiding of unnecessary details.

</details>

---

## 3.2 Defining classes and objects

---

- __(*) Introducing classes & objects.__
- __(1) What is the motivation behind an object?__
- __(2) How to objects and classes relate to each other?__
- __(3) What is an instance?__
- __(4) What is the name of the type variables, that store data, that are part of the class?__
- __(5) What are the operations defined for a class called?__

<details>

- (1) So that data can be represented closer to it's true meaning.
- (2) Such composite variables are called objects and their _type_ is called a class.
- (3) An object becomes a variable of a class and is said to be an instance of it's class.
- (4)
    - Data members
    - Member variables
    - Members
- (5) Methods.

</details>

---

## 3.3 Creating a class in Java

---

- __(*) Introducing classes & objects.__
- __(1) Code a MyDate class.__
- __(2) What should you note?__
- __(3) Use the MyData class in the main function.__
- __(4) How would you compile these two files?__
- __(5) What should you note?__

<details>

- (1)

```java
// File name: MyDate.java
public class MyDate {
    private int date;
    private int month;
    private int year;

    public void setDate() {
        date = 18;
        month = 7;
        year = 1988;
    }

    public void printDate() {
        System.out.println(date + "/" + month + "/" + year);
    }
}
```

- (2)
    - There is no `main` method.

<!---->

- (3)

```java
// File name: Main.java
public class Main {
    public static void main(String[] args) {
        MyDate myDate = new MyDate();

        myDate.setDate();

        myDate.printDate();
    }
}
```

- (4) `javac MyDate.java Main.java`
- (5)
    - No need to import anything as both files are in the same directory.

</details>

---

## 3.4 Objects and references

---

- __(*) Introducing classes & objects.__
- __(1) What does the following two line object creation highlight?.__

```java
MyDate myDate;
myDate = new MyDate();
```

<details>

- (1)
    - By declaring a variable with a class type, you are creating a variable that __refers__ or points to an object of the class type specified.
    - The `new` actually allocates some memory space for the object and sends back an __object reference__ as a result.

</details>

---

- __(*) Introducing classes & objects.__
- __(1) What is happening in the following code?.__

```java
MyDate myDate;
myDate = new MyDate();
MyDate myDate2 = myDate;
```

<details>

- (1)
    - A new variable of the `MyDate` class type is created and it is set to refer to the one and only object, `myDate`.

</details>

---