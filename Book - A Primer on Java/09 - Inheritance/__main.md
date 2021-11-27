# Inheritance - Main

---

- __(*) Inheritance.__
- __(1) What are the names of the classes related to each other by inheritance?__

<details>

- (1)
    - Base class (parent).
    - Derived class (child, subclass).

</details>

---

## 9.1 Extending a class

---

- __(*) Inheritance.__
- __(1) What keyword configures a class to inherit from another?__
- __(2) Syntax?__
- __(3) From one parent class, how many children classes can you have?__
- __(4) From one child class, how many parent classes can you have?__
- __(4) Can you subclass a subclass?__

<details>

- (1) `extends`.
- (2)

```java
public class __ChildClass__ extends __ParentClass__ {

}
```

- (3) Unlimited.
- (4) 1.
- (5) Yes.

</details>

---

- __(*) Inheritance.__
- __(1) Code example.__
- __(2) Notes.__

<details>

- (1)

```java
// File name: Animal.java
public class Animal {
    String name;
    public String hello() {
        return "Hello, I'm " + name + "!";
    }
}

// File name: Dog.java
public class Dog extends Animal {
    public Dog(String name) {
        this.name = name;
    }
    public String hello() {
        return "Woof, I'm " + this.name + "!";
    }
}
```

- (2)
    - The subclass did not need to redefine any member variables.
    - The `hello` method was redefined.

</details>

---

- __(*) Inheritance.__
- __(1) Something interesting about class types.__
- __(2) Code: Example.__
- __(3) Question 3.__

<details>

- (1)
    - When defining an object variable, it's parent class can be used as the type.
    - Logic: Regardless of the subclass, it would at least have the behaviour (think methods) of it's parent.
- (2)
    - `Dog myDog = new Dog("Fido");`.
    - `Animal myDog = new Dog("Fido");`.

</details>

---

## 9.2 Access Specifiers

---

- __(*) Inheritance.__
- __(1) What does an access specifier do?.__
- __(2) What things can use an access specifier?.__
- __(3) What access specifiers exist in Java?__

<details>

- (1) Controls the access and visibility of it's member.
- (2)
    - A class member field (variable?).
    - A class method.
    - (Others too from a Google.)
- (3)
    - `private`
    - `protected`
    - `public`

</details>

---

- __(*) Inheritance.__
- __(1) What are the names of public methods that read and write to private variables?__
- __(2) Benefit?__
- __(3) Access modifiers' impact on inheritance?__

<details>

- (1) Getters and setters.
- (2) Allows the flexibility to impose sensible restrictions on the values that a member can take.
- (3)
    - `public` members are inherited.
    - `protected` members are inherited but behave as private to outside the class.
    - `private` members are not inherited.

</details>

---

- (Insufficient detail in book.)

---

## 9.3 The super Keyword

---

- __(*) Inheritance.__
- __(1) What does the `super()` function do?__
- __(2) What does `super.` do?__
- __(2) What does overriding mean?__

<details>

- (1) Call the parent class' constructor function.
- (2) Provide access to the parent class' methods.
- (2) When a child class defines a method that replaces a parent's method of the same name.

</details>

---

## 9.4 The Object class

---

- __(*) Inheritance.__
- __(1) What is the `Object` class?__
- __(2) What are the implications of the `Object` class?__
- __(3) What can you do to mitigate the implications of above?__

<details>

- (1) The parent class to all other classes.
- (2)
    - The `Object` class contains a number of methods.
    - All classes inherit these methods.
    - E.g. `toString()`.
- (3) Override these methods.

</details>

---