# Star Pattern Challenges ⭐️🌟

## 1. Solid Rectangular Star Pattern ⭐

### Question

Write a program to print a solid rectangular star pattern with given rows and columns.

### C++

```cpp
#include <iostream>
using namespace std;

int main() {
    int rows = 3;
    int cols = 5;

    for (int i = 0; i < rows; ++i) {
        for (int j = 0; j < cols; ++j) {
            cout << "* ";
        }
        cout << endl;
    }

    return 0;
}
```

### Java

```java
public class SolidRectangularStar {

    public static void main(String[] args) {
        int rows = 3;
        int cols = 5;

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```

### Python

```python
# Solid Rectangular Star Pattern
rows = 3
cols = 5

for i in range(rows):
    print("* " * cols)
```

### JavaScript

```javascript
// Solid Rectangular Star Pattern
function solidRectangularStar() {
    let rows = 3;
    let cols = 5;

    for (let i = 0; i < rows; i++) {
        console.log('* '.repeat(cols));
    }
}

solidRectangularStar();
```

---

## 2. Hollow Rectangular Star Pattern 🌟

### Question

Write a program to print a hollow rectangular star pattern with given rows and columns.

### C++

```cpp
#include <iostream>
using namespace std;

int main() {
    int rows = 3;
    int cols = 5;

    for (int i = 0; i < rows; ++i) {
        for (int j = 0; j < cols; ++j) {
            if (i == 0 || i == rows - 1 || j == 0 || j == cols - 1) {
                cout << "* ";
            } else {
                cout << "  ";
            }
        }
        cout << endl;
    }

    return 0;
}
```

### Java

```java
public class HollowRectangularStar {

    public static void main(String[] args) {
        int rows = 3;
        int cols = 5;

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                if (i == 0 || i == rows - 1 || j == 0 || j == cols - 1) {
                    System.out.print("* ");
                } else {
                    System.out.print("  ");
                }
            }
            System.out.println();
        }
    }
}
```

### Python

```python
# Hollow Rectangular Star Pattern
rows = 3
cols = 5

for i in range(rows):
    for j in range(cols):
        if i == 0 or i == rows - 1 or j == 0 or j == cols - 1:
            print("* ", end="")
        else:
            print("  ", end="")
    print()
```

### JavaScript

```javascript
// Hollow Rectangular Star Pattern
function hollowRectangularStar() {
    let rows = 3;
    let cols = 5;

    for (let i = 0; i < rows; i++) {
        let line = '';
        for (let j = 0; j < cols; j++) {
            if (i === 0 || i === rows - 1 || j === 0 || j === cols - 1) {
                line += '* ';
            } else {
                line += '  ';
            }
        }
        console.log(line);
    }
}

hollowRectangularStar();
```

---

## 3. Half Pyramid Star Pattern 🏔️

### Question

Write a program to print a half-pyramid star pattern with the given number of rows.

### C++

```cpp
#include <iostream>
using namespace std;

int main() {
    int rows = 5;

    for (int i = 1; i <= rows; ++i) {
        for (int j = 1; j <= i; ++j) {
            cout << "* ";
        }
        cout << endl;
    }

    return 0;
}
```

### Java

```java
public class HalfPyramidStar {

    public static void main(String[] args) {
        int rows = 5;

        for (int i = 1; i <= rows; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```

### Python

```python
# Half Pyramid Star Pattern
rows = 5

for i in range(1, rows + 1):
    print("* " * i)
```

### JavaScript

```javascript
// Half Pyramid Star Pattern
function halfPyramidStar() {
    let rows = 5;

    for (let i = 1; i <= rows; i++) {
        console.log('* '.repeat(i));
    }
}

halfPyramidStar();
```

---

## 4. Inverted Half Pyramid Star Pattern 🔻

### Question

Write a program to print an inverted half-pyramid star pattern with the given number of rows.

### C++

```cpp
#include <iostream>
using namespace std;

int main() {
    int rows = 6;

    for (int i = rows; i >= 1; --i) {
        for (int j = 1; j <= i; ++j) {
            cout << "* ";
        }
        cout << endl;
    }

    return 0;
}
```

### Java

```java
public class InvertedHalfPyramidStar {

    public static void main(String[] args) {
        int rows = 6;

        for (int i = rows; i >= 1; i--) {
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```

### Python

```python
# Inverted Half Pyramid Star Pattern
rows = 6

for i in range(rows, 0, -1):
    print("* " * i)
```

### JavaScript

```javascript
// Inverted Half Pyramid Star Pattern
function invertedHalfPyramidStar() {
    let rows = 6;

    for (let i = rows; i >= 1; i--) {
        console.log('* '.repeat(i));
    }
}

invertedHalfPyramidStar();
```

---

## 5. Full Pyramid Star Pattern 🎋

### Question

Write a program to print a full pyramid star pattern with the given number of rows.

### C++

```cpp
#include <iostream>
using namespace std;

int main() {
    int rows = 5;

    for (int i = 1; i <= rows; ++i) {
        for (int j = rows; j > i; --j) {
            cout << "  ";
        }
        for (int k = 1; k <= (2 * i - 1); ++k) {
            cout << "* ";
        }
        cout << endl;
    }

    return 0;
}
```

### Java

```java
public class FullPyramidStar {

    public static void main(String[] args) {
        int rows = 5;

        for (int i = 1; i <= rows; i++) {
            for (int j = rows; j > i; j--) {
                System.out.print("  ");
            }
            for (int k = 1; k <= (2 * i - 1); k++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```

### Python

```python
# Full Pyramid Star Pattern
rows = 5

for i in range(1, rows + 1):
    print(' ' * (rows - i) + '* ' * (2 * i - 1))
```

### JavaScript

```javascript
// Full Pyramid Star Pattern
function fullPyramidStar() {
    let rows = 5;

    for (let i = 1; i <= rows; i++) {
        let spaces = ' '.repeat(rows - i);
        let stars = '* '.repeat(2 * i - 1);
        console.log(spaces + stars);
    }
}

fullPyramidStar();
```

---

## 6. Inverted Full Pyramid Star Pattern ⛺

### Question

Write a program to print an inverted full pyramid star pattern with the given number of rows.

### C++

```cpp
#include <iostream>
using namespace std;

int main() {
    int rows = 6;

    for (int i = rows; i >= 1; --i) {
        for (int j = rows; j > i; --j) {
            cout << "  ";
        }
        for (int k = 1; k <= (2 * i - 1); ++k) {
            cout << "* ";
        }
        cout << endl;
    }

    return 0;
}
```

### Java

```java
public class InvertedFullPyramidStar {

    public static void main(String[] args) {


        int rows = 6;

        for (int i = rows; i >= 1; i--) {
            for (int j = rows; j > i; j--) {
                System.out.print("  ");
            }
            for (int k = 1; k <= (2 * i - 1); k++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```

### Python

```python
# Inverted Full Pyramid Star Pattern
rows = 6

for i in range(rows, 0, -1):
    print(' ' * (rows - i) + '* ' * (2 * i - 1))
```

### JavaScript

```javascript
// Inverted Full Pyramid Star Pattern
function invertedFullPyramidStar() {
    let rows = 6;

    for (let i = rows; i >= 1; i--) {
        let spaces = ' '.repeat(rows - i);
        let stars = '* '.repeat(2 * i - 1);
        console.log(spaces + stars);
    }
}

invertedFullPyramidStar();
```


Here’s a GitHub markdown file with the requested questions, including C++, Java, Python, and JavaScript code for each pattern. I’ve added emojis to make the content engaging and illustrative. 🌟📚

---

## 7. Hollow Full Pyramid Star 🌟

### Question

Write a program to print a hollow full pyramid star pattern with the given number of rows.

### C++

```cpp
#include <iostream>
using namespace std;

int main() {
    int rows = 5;

    for (int i = 1; i <= rows; ++i) {
        for (int j = rows; j > i; --j) {
            cout << " ";
        }
        for (int k = 1; k <= (2 * i - 1); ++k) {
            if (k == 1 || k == (2 * i - 1) || i == rows) {
                cout << "*";
            } else {
                cout << " ";
            }
        }
        cout << endl;
    }

    return 0;
}
```

### Java

```java
public class HollowFullPyramidStar {

    public static void main(String[] args) {
        int rows = 5;

        for (int i = 1; i <= rows; i++) {
            for (int j = rows; j > i; j--) {
                System.out.print(" ");
            }
            for (int k = 1; k <= (2 * i - 1); k++) {
                if (k == 1 || k == (2 * i - 1) || i == rows) {
                    System.out.print("*");
                } else {
                    System.out.print(" ");
                }
            }
            System.out.println();
        }
    }
}
```

### Python

```python
# Hollow Full Pyramid Star Pattern
rows = 5

for i in range(1, rows + 1):
    print(' ' * (rows - i), end='')
    for j in range(1, 2 * i):
        if j == 1 or j == 2 * i - 1 or i == rows:
            print("*", end='')
        else:
            print(" ", end='')
    print()
```

### JavaScript

```javascript
// Hollow Full Pyramid Star Pattern
function hollowFullPyramidStar() {
    let rows = 5;

    for (let i = 1; i <= rows; i++) {
        let line = ' '.repeat(rows - i);
        for (let j = 1; j <= (2 * i - 1); j++) {
            if (j === 1 || j === (2 * i - 1) || i === rows) {
                line += '*';
            } else {
                line += ' ';
            }
        }
        console.log(line);
    }
}

hollowFullPyramidStar();
```

---

## 8. Half Pyramid Using Numbers 1️⃣

### Question

Write a program to print a half-pyramid pattern using numbers with the given number of rows.

### C++

```cpp
#include <iostream>
using namespace std;

int main() {
    int rows = 5;

    for (int i = 1; i <= rows; ++i) {
        for (int j = 1; j <= i; ++j) {
            cout << j << " ";
        }
        cout << endl;
    }

    return 0;
}
```

### Java

```java
public class HalfPyramidUsingNumbers {

    public static void main(String[] args) {
        int rows = 5;

        for (int i = 1; i <= rows; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print(j + " ");
            }
            System.out.println();
        }
    }
}
```

### Python

```python
# Half Pyramid Using Numbers
rows = 5

for i in range(1, rows + 1):
    print(" ".join(str(j) for j in range(1, i + 1)))
```

### JavaScript

```javascript
// Half Pyramid Using Numbers
function halfPyramidUsingNumbers() {
    let rows = 5;

    for (let i = 1; i <= rows; i++) {
        let line = '';
        for (let j = 1; j <= i; j++) {
            line += j + ' ';
        }
        console.log(line);
    }
}

halfPyramidUsingNumbers();
```

---

## 9. Pascal Triangle 📐

### Question

Write a program to print Pascal's Triangle with the given number of rows.

### C++

```cpp
#include <iostream>
using namespace std;

int factorial(int n) {
    if (n == 0 || n == 1) return 1;
    return n * factorial(n - 1);
}

int main() {
    int rows = 5;

    for (int i = 0; i < rows; ++i) {
        for (int j = 0; j <= i; ++j) {
            cout << factorial(i) / (factorial(j) * factorial(i - j)) << " ";
        }
        cout << endl;
    }

    return 0;
}
```

### Java

```java
public class PascalTriangle {

    public static void main(String[] args) {
        int rows = 5;

        for (int i = 0; i < rows; i++) {
            int C = 1;
            for (int j = 0; j <= i; j++) {
                System.out.print(C + " ");
                C = C * (i - j) / (j + 1);
            }
            System.out.println();
        }
    }
}
```

### Python

```python
# Pascal Triangle
from math import factorial

rows = 5

for i in range(rows):
    for j in range(i + 1):
        print(factorial(i) // (factorial(j) * factorial(i - j)), end=' ')
    print()
```

### JavaScript

```javascript
// Pascal Triangle
function pascalTriangle() {
    let rows = 5;

    for (let i = 0; i < rows; i++) {
        let C = 1;
        let line = '';
        for (let j = 0; j <= i; j++) {
            line += C + ' ';
            C = C * (i - j) / (j + 1);
        }
        console.log(line);
    }
}

pascalTriangle();
```

