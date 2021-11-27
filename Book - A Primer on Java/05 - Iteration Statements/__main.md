# Iteration Statements - Main

---

- __(*) Iteration statements.__
- __(1) What is another name for iteration?__
- __(2) What are the three iteration statements in Java?__

<details>

- (1) Loop.
- (2)
    - `while`
    - `do-while`
    - `for`

</details>

---

## 5.1 The while loop

---

- __(*) Iteration statements.__
- __(1) While loop.__

<details>

- (1)

```java
while (/* boolean expression */) {
    // ...
}
```

</details>

---

## 5.2 The do-while loop

---

- __(*) Iteration statements.__
- __(1) Do-while loop.__
- __(2) What is the difference between the do-while loop and the while loop?__
- __(3) What should you note about the syntax?__

<details>

- (1)

```java
do {
    // ...
} while (/* boolean expression */);
```

- (2)
    - The boolean expression is evaluated at the end of the loop.
    - This means the loop will be executed at least once.
- (3)
    - There is a semicolon after the while boolean expression.

</details>

---

## 5.3 The for loop

---

- __(*) Iteration statements.__
- __(1) What are the three parts of a for loop construct (before the loop block)?__
- __(2) For loop.__
- __(3) What do you note about the example?__

<details>

- (1)
    - Initialisation
    - Condition
    - Step
- (2)

```java
for (/* initialisation */; /* boolean condition */; /* step */) {
    // ...
}

// Example:

int sum = 0;
for (int ctr = 1; ctr <= 20; ctr++) {
    sum += ctr;
}
```

- (3) That you can declare and initialise a variable in the initialisation part.

</details>

---

## 5.4 break and continue

---

- __(*) Iteration statements.__
- __(1) What is a `break` statement in the context of a loop block?__
- __(2) What is a `continue` statement in the context of a loop block?__
- __(3) Example.__
- __(4) What does the example do?__

<details>

- (1) `break`
    - Exits the current loop.
    - Exits the loop statement. I.e. no subsequent loops are called.
- (2) `continue`
    - Exits the current loop.
    - Does not exit the loop statement. I.e. subsequent loops are called.
- (3)

```java
    int ctr = 0;
    int sum = 0;

    while(true){
        ctr++;

        if (ctr == 20)
            break;

        if ((ctr % 2) == 0)
            continue;

        sum = sum + ctr;
    }

    System.out.println("Oddsum:" + sum);
```

- (4) To print out the sum of only odd natural numbers below 20.

</details>

---