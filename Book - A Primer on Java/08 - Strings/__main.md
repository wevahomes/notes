# Strings - Main

---

- __(*) Strings.__
- __(1) What is a string?__
- __(2) What is a `String`?. Data type?__
- __(3) Code: Create a "Hello, World!" string.__
- __(4) What operator is used to concatenate a string?__

<details>

- (1) A collection of characters.
- (2)
    - A class supplied with Java which allows you to deal with strings.
    - It is an object of type String.
- (3)

```java
String message = "Hello, World!";
```

- (4) `+`.

</details>

---

## 8.1 String Methods

---

- __(*) Strings.__
- __(1) String length? Return type?__
- __(2) What is the position of a character called?__
- __(3) Substring?__

<details>

- (1)
    - `string.length();`.
    - Integer.
- (2) The index.
- (3)
    - `string.substring(startIndexInt);` - Ends at the end of the string.
    - `string.substring(startIndexInt, endIndexInt);`.

</details>

---

## 8.2 Escape Characters

---

- __(*) Strings.__
- __(1) How to include special characters in a string - Name?.__
- __(2) What is the character for this?__
- __(2) List some special characters.__

<details>

- (1) Escape characters / escape sequences.
- (2) `\`.
- (3)
    - `\n` - New line.
    - `\t` - Tab.
    - `\"` - Double quote (").
    - `\(singlequote) ` - Single quote (`).

</details>

---

## 8.3 Comparing Strings

---

- __(*) Strings.__
- __(1) How do you compare strings?__
- __(2) What does the `==` operator do in the case of strings? Details.__

<details>

- (1)
    - Using the equals method.
    - `s1.equals(s2)`.
- (2)
    - Checks if the two strings are the same object.
    - Even if two string objects contain the same string, `==` will still return false.

</details>

---