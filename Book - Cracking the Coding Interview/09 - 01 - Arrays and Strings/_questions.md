# Arrays and Strings - Questions

---

## Interview Questions

---

### Question 1

#### Question

![](./interviewQuestion01_.png)

#### Hints

<details><summary>Hint #44</summary>

![](./hint044.png)

</details>

<details><summary>Hint #117</summary>

![](./hint117.png)

</details>

<details><summary>Hint #132</summary>

![](./hint132.png)

</details>

#### Solution

<details><summary>Key points</summary>

- ASCII vs Unicode.
- Boolean flags.
- Initial check based on string length.
- Complexity:
    - Fixed character set:
        - Time: `O(n)` or `O(1)`.
        - Space: `O(1)`.
    - Variable character set:
        - Time: `O(min(c, n))` or `O(c)`.
        - Space: `O(c)`.
    - Where:
        - `n`: Length of the string.
        - `c`: Size of the character set.
- Bit vector.
    - Boolean: Data size in Java: 8 bits (?).
- No additional data structures: (!understand)
    - Compare all.
        - Complexity:
            - Time: `O(n^2)`.
            - Space: `O(1)`.
    - Sort & linear check.
        - Complexity:
            - Time: `O(n log n)`.
            - Space: `O(1)`.

</details>

<details><summary>Full solution</summary>

![](./interviewQuestion01_solution01.png)

![](./interviewQuestion01_solution02.png)

</details>

<details><summary>Additional notes</summary>

- ASCII vs Unicode
    - ASCII (Extended)
        - Regular
            - 2^7 characters. (128).
            - English.
        - Extended
            - 2^8 characters. (256).
            - Languages based on the latin alphabet.
        - Text can be stored as ASCII (Extended). In Bytes.
    - Unicode
        - 2^21 characters.
        - For all world-wide languages.
        - Abstract representation of text.
        - The unicode needs to be encoded to be stored.
            - UTF-8 and UTF-16 are variable length encodings.
            - In UTF-8, a character may occupy a minimum of 8 bits.
            - In UTF-16, a character length starts with 16 bits.
            - UTF-32 is a fixed length encoding of 32 bits.

</details>

---

### Question 2

#### Question

![](./interviewQuestion02_.png)

#### Hints

<details><summary>Hint #1</summary>

![](./hint001.png)

</details>

<details><summary>Hint #84</summary>

![](./hint084.png)

</details>

<details><summary>Hint #122</summary>

![](./hint122.png)

</details>

<details><summary>Hint #131</summary>

![](./hint131.png)

</details>

#### Solution

<details><summary>Key points</summary>

- N/A

</details>

<details><summary>Full solution</summary>

![](./interviewQuestion02_solution01.png)

![](./interviewQuestion02_solution02.png)

![](./interviewQuestion02_solution03.png)

![](./interviewQuestion02_solution04.png)

![](./interviewQuestion02_solution05.png)

![](./interviewQuestion02_solution06.png)

</details>

<details><summary>Additional notes</summary>

- N/A

</details>

---