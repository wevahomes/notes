# Arrays - Main

---

- __(*) Arrays.__
- __(1) What are the name of the things in an array?__
- __(2) What do the things in an array have in common?__

<details>

- (1) Elements.
- (2) Data type.

</details>

---

## 6.1 Array Initialization

---

- __(*) Arrays.__
- __(1) Code: Declare an array: Two ways.__
- __(2) What is that special notation when declaring arrays?__
- __(3) What should you note about declaring arrays?__

<details>

- (1)

```java
int myArray1[];
int[] myArray2; // Preferred way.
```

- (2) `[]` is the indexing operator.
- (3)
    - They just *associate* the *variable identifier* with the *type* of an array.
    - No storage is allocated for the array.

</details>

---

- __(*) Arrays.__
- __(1) What is the mechanism (/keyword) used to define an array.__
- __(2) Code: Define an array.__
- __(3) Notes.__

<details>

- (1) `new`.
- (2)

```java
int[] myArray = new int[10]
```

- (3)
    - You must specify the number of elements within the `[]`.
    - Each array is given an initial value depending on the array type.
    - Numeric types are assigned a 0 (zero).

</details>

---

- __(*) Arrays.__
- __(1) What is the mechanism used to initialise an array with values.__
- __(2) Code: Initialise an array with values.__
- __(3) Notes.__
- __(3) Question 3.__

<details>

- (1) Curly braces, `{}`.
- (2)

```java
String[] sentence = {"The", "quick", "brown", "fox", "jumped", "over", "the", "lazy", "dog."};
```

- (3)
    - A comma is used to separate the elements.
    - A `new` keyword was not needed. And so nor was the size of the array, it was taken from the number of elements in the curly brackets.

</details>

---

## 6.2 Using Arrays

---

- __(*) Arrays.__
- __(1) Name for an array location / element number?__
- __(2) What is the number of the first element?__
- __(3) What is the mechanism used to refer to an array element?__
- __(4) Example.__
- __(5) How do you get the length of an array?__

<details>

- (1) index (or subscript).
- (2) 0.
- (3) Square brackets, `[]`.
- (4) `myArray[0]`.
- (5) `myArray.length`.

</details>

---

## 6.3 The enhanced for loop

---

- __(*) Arrays.__
- __(1) What is the name of the normal for loop?__
- __(2) What is another type of for loop that can iterate over an array?__
- __(3) What other things can this for loop iterate over?__
- __(4) Code: What is the structure of this for loop?__
- __(5) Code: Example?__

<details>

- (1)
    - 3-part for loop, or
    - C-style for loop.
- (2)
    - Enhanced for loop, or
    - For-each loop.
- (3)
    - Other composite types.
    - Collections.
- (4)

```java
for (/* type */ /* variable */ : /* collection */) {
    // ...
}
```

- (5)

```java
String[] sentence = {"The", "quick", "brown", "fox", "jumped", "over", "the", "lazy", "dog."};

for (String word : sentence) {
    System.out.println(word);
}
```

</details>

---