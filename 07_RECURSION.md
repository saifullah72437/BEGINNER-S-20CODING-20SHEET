# Programming Challenges and Solutions 💻🚀

## 1. Write a Program to Find Sum of N Natural Numbers (Entered by Users) Using Recursion 📈🌟

### C++

```cpp
#include <iostream>
using namespace std;

int sumOfNaturalNumbers(int n) {
    if (n <= 1) return n;
    return n + sumOfNaturalNumbers(n - 1);
}

int main() {
    int n;
    cout << "Enter a positive integer: ";
    cin >> n;
    cout << "Sum of first " << n << " natural numbers is: " << sumOfNaturalNumbers(n) << endl;
    return 0;
}
```

### Java

```java
import java.util.Scanner;

public class SumOfNaturalNumbers {

    static int sumOfNaturalNumbers(int n) {
        if (n <= 1) return n;
        return n + sumOfNaturalNumbers(n - 1);
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a positive integer: ");
        int n = scanner.nextInt();
        System.out.println("Sum of first " + n + " natural numbers is: " + sumOfNaturalNumbers(n));
    }
}
```

### Python

```python
# Function to find the sum of N natural numbers using recursion
def sum_of_natural_numbers(n):
    if n <= 1:
        return n
    return n + sum_of_natural_numbers(n - 1)

# Main function
n = int(input("Enter a positive integer: "))
print(f"Sum of first {n} natural numbers is: {sum_of_natural_numbers(n)}")
```

### JavaScript

```javascript
// Function to find the sum of N natural numbers using recursion
function sumOfNaturalNumbers(n) {
    if (n <= 1) return n;
    return n + sumOfNaturalNumbers(n - 1);
}

// Main
let n = parseInt(prompt("Enter a positive integer:"), 10);
console.log(`Sum of first ${n} natural numbers is: ${sumOfNaturalNumbers(n)}`);
```

---

## 2. Write a Program to Calculate Factorial of a Number Using Recursion 🎯✨

### C++

```cpp
#include <iostream>
using namespace std;

int factorial(int n) {
    if (n <= 1) return 1;
    return n * factorial(n - 1);
}

int main() {
    int n;
    cout << "Enter a non-negative integer: ";
    cin >> n;
    cout << "Factorial of " << n << " is: " << factorial(n) << endl;
    return 0;
}
```

### Java

```java
import java.util.Scanner;

public class Factorial {

    static int factorial(int n) {
        if (n <= 1) return 1;
        return n * factorial(n - 1);
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a non-negative integer: ");
        int n = scanner.nextInt();
        System.out.println("Factorial of " + n + " is: " + factorial(n));
    }
}
```

### Python

```python
# Function to calculate factorial of a number using recursion
def factorial(n):
    if n <= 1:
        return 1
    return n * factorial(n - 1)

# Main function
n = int(input("Enter a non-negative integer: "))
print(f"Factorial of {n} is: {factorial(n)}")
```

### JavaScript

```javascript
// Function to calculate factorial of a number using recursion
function factorial(n) {
    if (n <= 1) return 1;
    return n * factorial(n - 1);
}

// Main
let n = parseInt(prompt("Enter a non-negative integer:"), 10);
console.log(`Factorial of ${n} is: ${factorial(n)}`);
```

---

## 3. Write a Program to Find G.C.D of Two Numbers Entered by User Using Recursion 📏🔄

### C++

```cpp
#include <iostream>
using namespace std;

int gcd(int a, int b) {
    if (b == 0) return a;
    return gcd(b, a % b);
}

int main() {
    int a, b;
    cout << "Enter two integers: ";
    cin >> a >> b;
    cout << "G.C.D of " << a << " and " << b << " is: " << gcd(a, b) << endl;
    return 0;
}
```

### Java

```java
import java.util.Scanner;

public class GCD {

    static int gcd(int a, int b) {
        if (b == 0) return a;
        return gcd(b, a % b);
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter two integers: ");
        int a = scanner.nextInt();
        int b = scanner.nextInt();
        System.out.println("G.C.D of " + a + " and " + b + " is: " + gcd(a, b));
    }
}
```

### Python

```python
# Function to find GCD of two numbers using recursion
def gcd(a, b):
    if b == 0:
        return a
    return gcd(b, a % b)

# Main function
a = int(input("Enter the first number: "))
b = int(input("Enter the second number: "))
print(f"G.C.D of {a} and {b} is: {gcd(a, b)}")
```

### JavaScript

```javascript
// Function to find GCD of two numbers using recursion
function gcd(a, b) {
    if (b === 0) return a;
    return gcd(b, a % b);
}

// Main
let a = parseInt(prompt("Enter the first number:"), 10);
let b = parseInt(prompt("Enter the second number:"), 10);
console.log(`G.C.D of ${a} and ${b} is: ${gcd(a, b)}`);
```

---

## 4. Write a Program that Calculates the Power of a Number Using Recursion Where Base and Exponent are Entered by the User 🚀🔢

### C++

```cpp
#include <iostream>
using namespace std;

int power(int base, int exponent) {
    if (exponent == 0) return 1;
    return base * power(base, exponent - 1);
}

int main() {
    int base, exponent;
    cout << "Enter base and exponent: ";
    cin >> base >> exponent;
    cout << base << " raised to the power of " << exponent << " is: " << power(base, exponent) << endl;
    return 0;
}
```

### Java

```java
import java.util.Scanner;

public class Power {

    static int power(int base, int exponent) {
        if (exponent == 0) return 1;
        return base * power(base, exponent - 1);
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter base and exponent: ");
        int base = scanner.nextInt();
        int exponent = scanner.nextInt();
        System.out.println(base + " raised to the power of " + exponent + " is: " + power(base, exponent));
    }
}
```

### Python

```python
# Function to calculate the power of a number using recursion
def power(base, exponent):
    if exponent == 0:
        return 1
    return base * power(base, exponent - 1)

# Main function
base = int(input("Enter base: "))
exponent = int(input("Enter exponent: "))
print(f"{base} raised to the power of {exponent} is: {power(base, exponent)}")
```

### JavaScript

```javascript
// Function to calculate the power of a number using recursion
function power(base, exponent) {
    if (exponent === 0) return 1;
    return base * power(base, exponent - 1);
}

// Main
let base = parseInt(prompt("Enter base:"), 10);
let exponent = parseInt(prompt("Enter exponent:"), 10);
console.log(`${base} raised to the power of ${exponent} is: ${power(base, exponent)}`);
```
