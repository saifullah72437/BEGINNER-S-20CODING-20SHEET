# Programming Questions

## 1. Write a Program to print "Hello, World!" 🌍

**C++:**
```cpp
#include <iostream>
int main() {
    std::cout << "Hello, World!";
    return 0;
}
```

**Java:**
```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

**Python:**
```python
print("Hello, World!")
```

**JavaScript:**
```javascript
console.log("Hello, World!");
```

## 2. Write a Program to Print Integer Number Entered by User 🧑‍💻

**C++:**
```cpp
#include <iostream>
int main() {
    int number;
    std::cout << "Enter an integer: ";
    std::cin >> number;
    std::cout << "You entered: " << number;
    return 0;
}
```

**Java:**
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter an integer: ");
        int number = scanner.nextInt();
        System.out.println("You entered: " + number);
    }
}
```

**Python:**
```python
number = int(input("Enter an integer: "))
print("You entered:", number)
```

**JavaScript:**
```javascript
let number = prompt("Enter an integer:");
console.log("You entered: " + number);
```

## 3. Write a Program to Add Two Integer Numbers Entered by User ➕➕

**C++:**
```cpp
#include <iostream>
int main() {
    int num1, num2, sum;
    std::cout << "Enter two integers: ";
    std::cin >> num1 >> num2;
    sum = num1 + num2;
    std::cout << "Sum: " << sum;
    return 0;
}
```

**Java:**
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter first integer: ");
        int num1 = scanner.nextInt();
        System.out.print("Enter second integer: ");
        int num2 = scanner.nextInt();
        int sum = num1 + num2;
        System.out.println("Sum: " + sum);
    }
}
```

**Python:**
```python
num1 = int(input("Enter first integer: "))
num2 = int(input("Enter second integer: "))
sum = num1 + num2
print("Sum:", sum)
```

**JavaScript:**
```javascript
let num1 = parseInt(prompt("Enter first integer:"));
let num2 = parseInt(prompt("Enter second integer:"));
let sum = num1 + num2;
console.log("Sum: " + sum);
```

## 4. Write a program where the user is asked to enter two integers (divisor and dividend) and the quotient and the remainder of their division is computed. (Both divisor and dividend should be integers.) ➗

**C++:**
```cpp
#include <iostream>
int main() {
    int divisor, dividend, quotient, remainder;
    std::cout << "Enter dividend: ";
    std::cin >> dividend;
    std::cout << "Enter divisor: ";
    std::cin >> divisor;
    quotient = dividend / divisor;
    remainder = dividend % divisor;
    std::cout << "Quotient: " << quotient << "\nRemainder: " << remainder;
    return 0;
}
```

**Java:**
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter dividend: ");
        int dividend = scanner.nextInt();
        System.out.print("Enter divisor: ");
        int divisor = scanner.nextInt();
        int quotient = dividend / divisor;
        int remainder = dividend % divisor;
        System.out.println("Quotient: " + quotient);
        System.out.println("Remainder: " + remainder);
    }
}
```

**Python:**
```python
dividend = int(input("Enter dividend: "))
divisor = int(input("Enter divisor: "))
quotient = dividend // divisor
remainder = dividend % divisor
print("Quotient:", quotient)
print("Remainder:", remainder)
```

**JavaScript:**
```javascript
let dividend = parseInt(prompt("Enter dividend:"));
let divisor = parseInt(prompt("Enter divisor:"));
let quotient = Math.floor(dividend / divisor);
let remainder = dividend % divisor;
console.log("Quotient: " + quotient);
console.log("Remainder: " + remainder);
```

## 5. Write a Program to Find Size of int, float, double and char in your computer 🖥️

**C++:**
```cpp
#include <iostream>
int main() {
    std::cout << "Size of int: " << sizeof(int) << " bytes\n";
    std::cout << "Size of float: " << sizeof(float) << " bytes\n";
    std::cout << "Size of double: " << sizeof(double) << " bytes\n";
    std::cout << "Size of char: " << sizeof(char) << " byte\n";
    return 0;
}
```

**Java:**
```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Size of int: " + Integer.BYTES + " bytes");
        System.out.println("Size of float: " + Float.BYTES + " bytes");
        System.out.println("Size of double: " + Double.BYTES + " bytes");
        System.out.println("Size of char: " + Character.BYTES + " byte");
    }
}
```

**Python:**
```python
import sys
print("Size of int:", sys.getsizeof(int()), "bytes")
print("Size of float:", sys.getsizeof(float()), "bytes")
print("Size of double:", sys.getsizeof(float()), "bytes")
print("Size of char:", sys.getsizeof(chr(0)), "bytes")
```

**JavaScript:**
```javascript
console.log("Size of int:", 4, "bytes");
console.log("Size of float:", 4, "bytes");
console.log("Size of double:", 8, "bytes");
console.log("Size of char:", 2, "bytes");
```

## 6. Write a Program to Swap Two Numbers 🔄

**C++:**
```cpp
#include <iostream>
int main() {
    int a, b, temp;
    std::cout << "Enter first number: ";
    std::cin >> a;
    std::cout << "Enter second number: ";
    std::cin >> b;
    temp = a;
    a = b;
    b = temp;
    std::cout << "After swapping: \n";
    std::cout << "First number: " << a << "\nSecond number: " << b;
    return 0;
}
```

**Java:**
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter first number: ");
        int a = scanner.nextInt();
        System.out.print("Enter second number: ");
        int b = scanner.nextInt();
        int temp = a;
        a = b;
        b = temp;
        System.out.println("After swapping: ");
        System.out.println("First number: " + a);
        System.out.println("Second number: " + b);
    }
}
```

**Python:**
```python
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
a, b = b, a
print("After swapping:")
print("First number:", a)
print("Second number:", b)
```

**JavaScript:**
```javascript
let a = parseInt(prompt("Enter first number:"));
let b = parseInt(prompt("Enter second number:"));
[a, b] = [b, a];
console.log("After swapping:");
console.log("First number: " + a);
console.log("Second number: " + b);
```

## 7. Write a Program to Find ASCII Value of a Character 🔤

**C++:**
```cpp
#include <iostream>
int main() {
    char c;
    std::cout << "Enter a character: ";
    std::cin >> c;
    std::cout << "ASCII value of " << c << " is " << int(c);
    return 0;
}
```

**Java:**
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a character: ");
        char c = scanner.next().charAt(0);
        int ascii = (int) c;
        System.out.println("ASCII value of " + c + " is " + ascii);
    }
}
```

**Python:**
```python
c = input("Enter a character: ")
print("ASCII value of", c, "is", ord(c))
```

**JavaScript:**
```javascript
let c = prompt("Enter a character:");
console.log("ASCII value of " + c + " is " + c.charCodeAt(0));
```

## 8. Write a Program to Multiply two decimal Numbers entered by

 User ✖️

**C++:**
```cpp
#include <iostream>
int main() {
    float num1, num2, product;
    std::cout << "Enter two numbers: ";
    std::cin >> num1 >> num2;
    product = num1 * num2;
    std::cout << "Product: " << product;
    return 0;
}
```

**Java:**
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter first number: ");
        float num1 = scanner.nextFloat();
        System.out.print("Enter second number: ");
        float num2 = scanner.nextFloat();
        float product = num1 * num2;
        System.out.println("Product: " + product);
    }
}
```

**Python:**
```python
num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))
product = num1 * num2
print("Product:", product)
```

**JavaScript:**
```javascript
let num1 = parseFloat(prompt("Enter first number:"));
let num2 = parseFloat(prompt("Enter second number:"));
let product = num1 * num2;
console.log("Product: " + product);
```

