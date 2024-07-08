# Programming Challenges and Solutions 💻🚀

## 1. Write a Program that Adds Two Matrices Using Multi-dimensional Arrays Where the Number of Rows `r` and Columns `c` is Entered by User (Value of `r` and `c` < 100) ➕🧮

### C++

```cpp
#include <iostream>
using namespace std;

int main() {
    int r, c;

    cout << "Enter the number of rows and columns (r and c): ";
    cin >> r >> c;

    if (r >= 100 || c >= 100) {
        cout << "The value of r and c should be less than 100." << endl;
        return 1;
    }

    int matrix1[r][c], matrix2[r][c], sum[r][c];

    cout << "Enter elements of first matrix:" << endl;
    for (int i = 0; i < r; ++i) {
        for (int j = 0; j < c; ++j) {
            cin >> matrix1[i][j];
        }
    }

    cout << "Enter elements of second matrix:" << endl;
    for (int i = 0; i < r; ++i) {
        for (int j = 0; j < c; ++j) {
            cin >> matrix2[i][j];
        }
    }

    // Adding the matrices
    for (int i = 0; i < r; ++i) {
        for (int j = 0; j < c; ++j) {
            sum[i][j] = matrix1[i][j] + matrix2[i][j];
        }
    }

    cout << "Sum of the matrices is:" << endl;
    for (int i = 0; i < r; ++i) {
        for (int j = 0; j < c; ++j) {
            cout << sum[i][j] << " ";
        }
        cout << endl;
    }

    return 0;
}
```

### Java

```java
import java.util.Scanner;

public class MatrixAddition {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the number of rows and columns (r and c): ");
        int r = scanner.nextInt();
        int c = scanner.nextInt();

        if (r >= 100 || c >= 100) {
            System.out.println("The value of r and c should be less than 100.");
            return;
        }

        int[][] matrix1 = new int[r][c];
        int[][] matrix2 = new int[r][c];
        int[][] sum = new int[r][c];

        System.out.println("Enter elements of first matrix:");
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                matrix1[i][j] = scanner.nextInt();
            }
        }

        System.out.println("Enter elements of second matrix:");
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                matrix2[i][j] = scanner.nextInt();
            }
        }

        // Adding the matrices
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                sum[i][j] = matrix1[i][j] + matrix2[i][j];
            }
        }

        System.out.println("Sum of the matrices is:");
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                System.out.print(sum[i][j] + " ");
            }
            System.out.println();
        }
    }
}
```

### Python

```python
# Program to add two matrices
r, c = map(int, input("Enter the number of rows and columns (r and c): ").split())

if r >= 100 or c >= 100:
    print("The value of r and c should be less than 100.")
    exit()

matrix1 = []
matrix2 = []
sum_matrix = []

print("Enter elements of first matrix:")
for i in range(r):
    row = list(map(int, input().split()))
    matrix1.append(row)

print("Enter elements of second matrix:")
for i in range(r):
    row = list(map(int, input().split()))
    matrix2.append(row)

# Adding the matrices
for i in range(r):
    sum_row = []
    for j in range(c):
        sum_row.append(matrix1[i][j] + matrix2[i][j])
    sum_matrix.append(sum_row)

print("Sum of the matrices is:")
for row in sum_matrix:
    print(" ".join(map(str, row)))
```

### JavaScript

```javascript
// Function to add two matrices
function addMatrices() {
    let r = parseInt(prompt("Enter the number of rows (r):"));
    let c = parseInt(prompt("Enter the number of columns (c):"));

    if (r >= 100 || c >= 100) {
        console.log("The value of r and c should be less than 100.");
        return;
    }

    let matrix1 = [];
    let matrix2 = [];
    let sum = [];

    console.log("Enter elements of first matrix:");
    for (let i = 0; i < r; i++) {
        matrix1[i] = [];
        for (let j = 0; j < c; j++) {
            matrix1[i][j] = parseInt(prompt(`Enter element [${i}][${j}] of first matrix:`));
        }
    }

    console.log("Enter elements of second matrix:");
    for (let i = 0; i < r; i++) {
        matrix2[i] = [];
        for (let j = 0; j < c; j++) {
            matrix2[i][j] = parseInt(prompt(`Enter element [${i}][${j}] of second matrix:`));
        }
    }

    // Adding the matrices
    for (let i = 0; i < r; i++) {
        sum[i] = [];
        for (let j = 0; j < c; j++) {
            sum[i][j] = matrix1[i][j] + matrix2[i][j];
        }
    }

    console.log("Sum of the matrices is:");
    for (let i = 0; i < r; i++) {
        console.log(sum[i].join(" "));
    }
}

addMatrices();
```

---

## 2. Write a Program that Takes Two Matrices of Order `r1*c1` and `r2*c2` Respectively. Then, the Program Multiplies These Two Matrices (If Possible) and Displays It on the Screen. 🧮🔄

### C++

```cpp
#include <iostream>
using namespace std;

int main() {
    int r1, c1, r2, c2;

    cout << "Enter the number of rows and columns for first matrix (r1 c1): ";
    cin >> r1 >> c1;

    cout << "Enter the number of rows and columns for second matrix (r2 c2): ";
    cin >> r2 >> c2;

    if (c1 != r2) {
        cout << "Matrix multiplication is not possible." << endl;
        return 1;
    }

    int matrix1[r1][c1], matrix2[r2][c2], result[r1][c2] = {0};

    cout << "Enter elements of first matrix:" << endl;
    for (int i = 0; i < r1; ++i) {
        for (int j = 0; j < c1; ++j) {
            cin >> matrix1[i][j];
        }
    }

    cout << "Enter elements of second matrix:" << endl;
    for (int i = 0; i < r2; ++i) {
        for (int j = 0; j < c2; ++j) {
            cin >> matrix2[i][j];
        }
    }

    // Multiplying the matrices
    for (int i = 0; i < r1; ++i) {
        for (int j = 0; j < c2; ++j) {
            for (int k = 0; k < c1; ++k) {
                result[i][j] += matrix1[i][k] * matrix2[k][j];
            }
        }
    }

    cout << "Product of the matrices is:" << endl;
    for (int i = 0; i < r1; ++i) {
        for (int j = 0; j < c2; ++j) {
            cout << result[i][j] << " ";
        }
        cout << endl;
    }

    return 0;
}
```

### Java

```java
import java.util.Scanner;

public class MatrixMultiplication {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the number of rows and columns for first matrix (r1 c1): ");
        int r1 = scanner.nextInt();
        int c1 = scanner.nextInt();

        System.out.print("Enter the number of rows and columns for second matrix (r2 c

2): ");
        int r2 = scanner.nextInt();
        int c2 = scanner.nextInt();

        if (c1 != r2) {
            System.out.println("Matrix multiplication is not possible.");
            return;
        }

        int[][] matrix1 = new int[r1][c1];
        int[][] matrix2 = new int[r2][c2];
        int[][] result = new int[r1][c2];

        System.out.println("Enter elements of first matrix:");
        for (int i = 0; i < r1; i++) {
            for (int j = 0; j < c1; j++) {
                matrix1[i][j] = scanner.nextInt();
            }
        }

        System.out.println("Enter elements of second matrix:");
        for (int i = 0; i < r2; i++) {
            for (int j = 0; j < c2; j++) {
                matrix2[i][j] = scanner.nextInt();
            }
        }

        // Multiplying the matrices
        for (int i = 0; i < r1; i++) {
            for (int j = 0; j < c2; j++) {
                for (int k = 0; k < c1; k++) {
                    result[i][j] += matrix1[i][k] * matrix2[k][j];
                }
            }
        }

        System.out.println("Product of the matrices is:");
        for (int i = 0; i < r1; i++) {
            for (int j = 0; j < c2; j++) {
                System.out.print(result[i][j] + " ");
            }
            System.out.println();
        }
    }
}
```

### Python

```python
# Program to multiply two matrices
r1, c1 = map(int, input("Enter the number of rows and columns for first matrix (r1 c1): ").split())
r2, c2 = map(int, input("Enter the number of rows and columns for second matrix (r2 c2): ").split())

if c1 != r2:
    print("Matrix multiplication is not possible.")
    exit()

matrix1 = []
matrix2 = []
result = [[0 for _ in range(c2)] for _ in range(r1)]

print("Enter elements of first matrix:")
for i in range(r1):
    row = list(map(int, input().split()))
    matrix1.append(row)

print("Enter elements of second matrix:")
for i in range(r2):
    row = list(map(int, input().split()))
    matrix2.append(row)

# Multiplying the matrices
for i in range(r1):
    for j in range(c2):
        for k in range(c1):
            result[i][j] += matrix1[i][k] * matrix2[k][j]

print("Product of the matrices is:")
for row in result:
    print(" ".join(map(str, row)))
```

### JavaScript

```javascript
// Function to multiply two matrices
function multiplyMatrices() {
    let r1 = parseInt(prompt("Enter the number of rows for first matrix (r1):"));
    let c1 = parseInt(prompt("Enter the number of columns for first matrix (c1):"));
    let r2 = parseInt(prompt("Enter the number of rows for second matrix (r2):"));
    let c2 = parseInt(prompt("Enter the number of columns for second matrix (c2):"));

    if (c1 !== r2) {
        console.log("Matrix multiplication is not possible.");
        return;
    }

    let matrix1 = [];
    let matrix2 = [];
    let result = Array.from({ length: r1 }, () => Array(c2).fill(0));

    console.log("Enter elements of first matrix:");
    for (let i = 0; i < r1; i++) {
        matrix1[i] = [];
        for (let j = 0; j < c1; j++) {
            matrix1[i][j] = parseInt(prompt(`Enter element [${i}][${j}] of first matrix:`));
        }
    }

    console.log("Enter elements of second matrix:");
    for (let i = 0; i < r2; i++) {
        matrix2[i] = [];
        for (let j = 0; j < c2; j++) {
            matrix2[i][j] = parseInt(prompt(`Enter element [${i}][${j}] of second matrix:`));
        }
    }

    // Multiplying the matrices
    for (let i = 0; i < r1; i++) {
        for (let j = 0; j < c2; j++) {
            for (let k = 0; k < c1; k++) {
                result[i][j] += matrix1[i][k] * matrix2[k][j];
            }
        }
    }

    console.log("Product of the matrices is:");
    for (let i = 0; i < r1; i++) {
        console.log(result[i].join(" "));
    }
}

multiplyMatrices();
```

---

## 3. Write a Program that Takes a Matrix of Order `r*c` from the User and Computes the Transpose of the Matrix. 🔄🧩

### C++

```cpp
#include <iostream>
using namespace std;

int main() {
    int r, c;

    cout << "Enter the number of rows and columns (r and c): ";
    cin >> r >> c;

    int matrix[r][c], transpose[c][r];

    cout << "Enter elements of the matrix:" << endl;
    for (int i = 0; i < r; ++i) {
        for (int j = 0; j < c; ++j) {
            cin >> matrix[i][j];
        }
    }

    // Computing the transpose
    for (int i = 0; i < r; ++i) {
        for (int j = 0; j < c; ++j) {
            transpose[j][i] = matrix[i][j];
        }
    }

    cout << "Transpose of the matrix is:" << endl;
    for (int i = 0; i < c; ++i) {
        for (int j = 0; j < r; ++j) {
            cout << transpose[i][j] << " ";
        }
        cout << endl;
    }

    return 0;
}
```

### Java

```java
import java.util.Scanner;

public class MatrixTranspose {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the number of rows and columns (r and c): ");
        int r = scanner.nextInt();
        int c = scanner.nextInt();

        int[][] matrix = new int[r][c];
        int[][] transpose = new int[c][r];

        System.out.println("Enter elements of the matrix:");
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                matrix[i][j] = scanner.nextInt();
            }
        }

        // Computing the transpose
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                transpose[j][i] = matrix[i][j];
            }
        }

        System.out.println("Transpose of the matrix is:");
        for (int i = 0; i < c; i++) {
            for (int j = 0; j < r; j++) {
                System.out.print(transpose[i][j] + " ");
            }
            System.out.println();
        }
    }
}
```

### Python

```python
# Program to find the transpose of a matrix
r, c = map(int, input("Enter the number of rows and columns (r and c): ").split())

matrix = []
print("Enter elements of the matrix:")
for _ in range(r):
    row = list(map(int, input().split()))
    matrix.append(row)

# Computing the transpose
transpose = [[matrix[j][i] for j in range(r)] for i in range(c)]

print("Transpose of the matrix is:")
for row in transpose:
    print(" ".join(map(str, row)))
```

### JavaScript

```javascript
// Function to compute the transpose of a matrix
function transposeMatrix() {
    let r = parseInt(prompt("Enter the number of rows (r):"));
    let c = parseInt(prompt("Enter the number of columns (c):"));

    let matrix = [];
    let transpose = Array.from({ length: c }, () => Array(r).fill(0));

    console.log("Enter elements of the matrix:");
    for (let i = 0; i < r; i++) {
        matrix[i] = [];
        for (let j = 0; j < c; j++) {
            matrix[i][j] = parseInt(prompt(`Enter element [${i}][${j}] of the matrix:`));
        }
    }

    // Computing the transpose
    for (let i = 0; i < r; i++) {
        for (let j = 0; j < c; j++) {
            transpose[j][i] = matrix[i][j];
        }
    }

    console.log("Transpose of the matrix is:");
    for (let i = 0; i < c; i++) {
        console.log(transpose[i].join(" "));
    }
}

transposeMatrix();
```

---

## 4. Write a Program that Takes Three Integers from the User and Swaps Them in Cyclic Order Using Pointers. Example:

 Enter Value of a, b, and c Respectively: 1 2 3 Value After Swapping Numbers in Cycle: a=3, b=1, c=2 🔄🔄🔄

### C++

```cpp
#include <iostream>
using namespace std;

void swapInCycle(int* a, int* b, int* c) {
    int temp = *a;
    *a = *c;
    *c = *b;
    *b = temp;
}

int main() {
    int a, b, c;

    cout << "Enter value of a, b and c respectively: ";
    cin >> a >> b >> c;

    swapInCycle(&a, &b, &c);

    cout << "Value after swapping numbers in cycle:" << endl;
    cout << "a=" << a << endl;
    cout << "b=" << b << endl;
    cout << "c=" << c << endl;

    return 0;
}
```

### Java

```java
import java.util.Scanner;

public class SwapInCycle {

    public static void swapInCycle(int[] arr) {
        int temp = arr[0];
        arr[0] = arr[2];
        arr[2] = arr[1];
        arr[1] = temp;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int[] arr = new int[3];
        System.out.print("Enter value of a, b and c respectively: ");
        for (int i = 0; i < 3; i++) {
            arr[i] = scanner.nextInt();
        }

        swapInCycle(arr);

        System.out.println("Value after swapping numbers in cycle:");
        System.out.println("a=" + arr[0]);
        System.out.println("b=" + arr[1]);
        System.out.println("c=" + arr[2]);
    }
}
```

### Python

```python
# Program to swap three integers in cyclic order
a, b, c = map(int, input("Enter value of a, b and c respectively: ").split())

# Swapping in cycle
a, b, c = c, a, b

print("Value after swapping numbers in cycle:")
print(f"a={a}")
print(f"b={b}")
print(f"c={c}")
```

### JavaScript

```javascript
// Function to swap three integers in cyclic order
function swapInCycle() {
    let a = parseInt(prompt("Enter value of a:"));
    let b = parseInt(prompt("Enter value of b:"));
    let c = parseInt(prompt("Enter value of c:"));

    [a, b, c] = [c, a, b];

    console.log("Value after swapping numbers in cycle:");
    console.log(`a=${a}`);
    console.log(`b=${b}`);
    console.log(`c=${c}`);
}

swapInCycle();
```
