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

Output:

Enter a: 1
Enter b: -3
Enter c: 2
Two distinct real roots: 2.0 and 1.0

Result: The program successfully calculates the roots of a quadratic equation.
