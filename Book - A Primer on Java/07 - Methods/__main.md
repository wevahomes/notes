# Methods - Main

---

- __(*) Methods.__
- __(1) What is a method?__
- __(2) What is a method closely related to?__
- __(3) What is the difference?__
- __(4) What is the general syntax of a method?__
- __(5) What is the method signature?__

<details>

- (1) An operation of a class.
- (2) A procedure or function - i.e. a block of statements performing a task.
- (3) A method is always declared inside a class.
- (4)

```java
accessModifier returnType methodName (optional parameter list) {
    // ...
}
```

- (5) The method name along with it's parameter list.

</details>

---

## 7.1 Parameters & Return Values

---

- __(*) Methods.__
- __(1) Code a class that calculates interest using methods etc.__
- __(2) What are passed into a method call? What happens next?__
- __(3) How do you refer to the calling object in a class method? What is it commonly used for?__
- __(4) Notes.__

<details>

- (1)

```java
// File name: Main.java
public class Main {
    public static void main(String[] args) {
        SimpleInterest applicant = new SimpleInterest();
        applicant.initValues(100f, 0.06f, 2);
        float amount = 100f + applicant.calcInterest();
        System.out.println("Amount after time period: " + amount);
    }
}

// File name: SimpleInterest.java
public class SimpleInterest {
    float amount;
    float rate;
    int timePeriod;

    public void initValues (float principal, float rateOfInterest, int numOfYears) {
        this.amount = principal;
        this.rate = rateOfInterest;
        this.timePeriod = numOfYears;
    }

    public float calcInterest() {
        float simpleInterest = amount * rate * timePeriod;
        return simpleInterest;
    }
}
```

- (2)
    - Arguments.
    - These arguments of the method call pass their values onto the parameters in the method signature.
- (3)
    - Using `this`.
    - Commonly used to access the member variables.
    - It will differentiate between parameters and instance (member) variables.
    - However, if there is no naming conflict between the parameter variable identifiers and the member variable identifiers then `this.` is not needed.
- (4)
    - One method returns a `float`, the other returns `void`.
        - This is taken into account when the methods are called.

</details>

---

## 7.2 Constructors

---

- __(*) Methods.__
- __(1) What is a constructor?__
- __(2) Details of the constructor.__
- __(3) When are the parameters of the constructor method set?__

<details>

- (1) A special method that is called when an object is created using `new`.
- (2)
    - Same name as the class it is contained in.
    - No return type.
- (3) During the instantiation (`new`).

</details>

---