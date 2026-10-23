# Programming Using Python - Practical Record

## Student Details
| Field | Details |
| :--- | :--- |
| Name | Sanjana |
| Course | B.Sc. (Hons.) Computer Science |
| Semester | I (First Semester) |
| Roll Number | 27560053 |
| Subject Code | DSC-01 |
| Subject | Programming Using Python |
| College | Ramanujan College, University of Delhi |
| University | University of Delhi |
| Year | 2025-26 |

## About This Repository
This repository contains all 15 practical programs of Python as per DU syllabus. Each program is written in simple and understandable format with proper comments and output screenshots.

## How to Run The Programs
1. Install Python 3 from python.org
2. Save a program as a `.py` file (e.g., `practical01.py`)
3. Open terminal / CMD / Pydroid and run:
```bash
## **python practical01.py**
Practical 01 - Roots of a Quadratic Equation

Aim: Write a Python program to find the roots of a quadratic equation.

**Code:**

```python
import math

a = float(input("Enter a: "))
b = float(input("Enter b: "))
c = float(input("Enter c: "))

if a == 0:
    print("Not a quadratic equation")
else:
    d = b**2 - 4*a*c

    if d > 0:
        r1 = (-b + math.sqrt(d)) / (2*a)
        r2 = (-b - math.sqrt(d)) / (2*a)
        print("Two distinct real roots:", r1, "and", r2)

    elif d == 0:
        print("Equal roots:", -b / (2*a))

    else:
        real = -b / (2*a)
        imag = math.sqrt(-d) / abs(2*a)
        print(f"Complex roots: {real}+{imag}i and {real}-{imag}i")
```
Result: The program successfully calculates the roots of a quadratic equation.
## **Practical 02 - Prime Numbers**

Aim: Write a Python program to check whether a number is prime or not.

**Code:**
```
n = int(input("Enter a number: "))

if n < 2:
    print("Not Prime")
else:
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            print("Not Prime")
            break
    else:
        print("Prime")
```

**Output:**

Enter a number: 7
Prime

Result: The program checks whether a number is prime or not.

---

## **Practical 03 - Star Pyramids**

Aim: Write a Python program to print a star pyramid.

**Code:**

```
n = int(input("Enter number of rows: "))

for i in range(1, n + 1):
    print(" " * (n - i) + "* " * i)
```

Output:

Enter number of rows: 3
  *
 * *
* * *

Result: The program prints a star pyramid pattern.

---

## **Practical 04 - Character Classification**

Aim: Write a Python program to classify a character as a vowel, consonant, digit, or special character.

**Code:**
```
ch = input("Enter a character: ")

if len(ch) != 1:
    print("Enter only one character")
elif ch.isalpha():
    if ch.lower() in "aeiou":
        print("Vowel")
    else:
        print("Consonant")
elif ch.isdigit():
    print("Digit")
else:
    print("Special Character")
```

Output:

Enter a character: A
Vowel

Result: The program classifies the given character.

---

## **Practical 05 - String Operations**

Aim: Write a Python program to perform basic string operations.

**Code:**

```
s = input("Enter a string: ")

print("Length:", len(s))
print("Uppercase:", s.upper())
print("Lowercase:", s.lower())
print("Reverse:", s[::-1])
```

Output:

Enter a string: hello
Length: 5
Uppercase: HELLO
Lowercase: hello
Reverse: olleh

Result: The program performs basic string operations.

---

## **Practical 06 - Swap Prefixes of Two Strings**

Aim: Write a Python program to swap the first characters of two strings.

**Code:**
```
s1 = input("Enter first string: ")
s2 = input("Enter second string: ")

if s1 and s2:
    s1 = s2[0] + s1[1:]
    s2 = s1[0] + s2[1:]
    print("First string:", s1)
    print("Second string:", s2)
else:
    print("Strings cannot be empty")
```

Output:

Enter first string: apple
Enter second string: banana
First string: bpple
Second string: anna

Result: The program swaps the first characters of two strings.

---

## **Practical 07 - Substring Indices**

Aim: Write a Python program to find the starting indices of a substring in a string.

**Code:**
```
s = input("Enter a string: ")
sub = input("Enter substring: ")

indices = []

if sub:
    for i in range(len(s) - len(sub) + 1):
        if s[i:i + len(sub)] == sub:
            indices.append(i)

print("Indices:", indices)
```

Output:

Enter a string: banana
Enter substring: ana
Indices: [1, 3]

Result: The program finds all starting indices of the given substring.

---

## **Practical 08 - Cubes of Even Integers**

Aim: Write a Python program to find the cubes of even integers in a given range.

**Code:**
```
n = int(input("Enter the limit: "))

for i in range(2, n + 1, 2):
    print(i, ":", i ** 3)
```

Output:

Enter the limit: 6
2 : 8
4 : 64
6 : 216

Result: The program calculates and displays the cubes of even integers.

---

## **Practical 09 - File Handling**

Aim: Write a Python program to write and read data from a file.

**Code:**
```
with open("sample.txt", "w") as f:
    f.write("Hello Python")

with open("sample.txt", "r") as f:
    data = f.read()

print("File content:", data)
```

Output:

File content: Hello Python

Result: The program writes data to a file and reads it successfully.

---

## **Practical 10 - Dictionary of Cubes**

Aim: Write a Python program to create a dictionary containing numbers and their cubes.

**Code:**
```
n = int(input("Enter the limit: "))

cubes = {i: i ** 3 for i in range(1, n + 1)}

print(cubes)
```

Output:

Enter the limit: 5
{1: 1, 2: 8, 3: 27, 4: 64, 5: 125}

Result: The program creates a dictionary of numbers and their cubes.

---

## **Practical 11 - Tuple Operations**

Aim: Write a Python program to perform basic tuple operations.

**Code:**
```
t = (10, 20, 30, 20, 40)

print("Tuple:", t)
print("Length:", len(t))
print("Count of 20:", t.count(20))
print("Index of 30:", t.index(30))
```

Output:

Tuple: (10, 20, 30, 20, 40)
Length: 5
Count of 20: 2
Index of 30: 2

Result: The program performs basic tuple operations.

---

## **Practical 12 - Employee Class and Object Counting**

Aim: Write a Python program to create an Employee class and count its objects.

**Code:**
```
class Employee:
    count = 0

    def __init__(self, name):
        self.name = name
        Employee.count += 1


e1 = Employee("Aman")
e2 = Employee("Riya")
e3 = Employee("Neha")

print("Total employees:", Employee.count)
```

Output:

Total employees: 3

Result: The program creates Employee objects and counts them.

---

## **Practical 13 - Class Point2D**

Aim: Write a Python program to create a Point2D class representing a point in two-dimensional space.

**Code:**

```
class Point2D:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def display(self):
        print("Point:", (self.x, self.y))


p = Point2D(3, 4)
p.display()
```

Output:

Point: (3, 4)

Result: The program creates and displays a two-dimensional point.

---

## **Practical 14 - Inheritance: Class Point3D**

Aim: Write a Python program to demonstrate inheritance using Point2D and Point3D classes.

**Code:**
```
class Point2D:
    def __init__(self, x, y):
        self.x = x
        self.y = y


class Point3D(Point2D):
    def __init__(self, x, y, z):
        super().__init__(x, y)
        self.z = z

    def display(self):
        print("Point3D:", (self.x, self.y, self.z))


p = Point3D(2, 3, 4)
p.display()
```

Output:

Point3D: (2, 3, 4)

Result: The program demonstrates inheritance using Point2D and Point3D classes.

---

## **Practical 15 - Exception Handling for a Name**

Aim: Write a Python program to demonstrate exception handling while accepting a name.

**Code:**
```
try:
    name = input("Enter your name: ")

    if not name.strip():
        raise ValueError("Name cannot be empty")

    print("Hello,", name)

except ValueError as e:
    print("Error:", e)
```

Output:

Enter your name: Sanjana
Hello, Sanjana

Result: The program demonstrates exception handling for an empty name.

---

Conclusion

All 15 Python practical programs demonstrate fundamental concepts of Python programming, including conditional statements, loops, strings, collections, file handling, classes, inheritance, and exception handling.
