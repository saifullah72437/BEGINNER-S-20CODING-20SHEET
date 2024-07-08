# Programming Questions and Solutions

## 1. Write a Program to Calculate Sum of first N Natural Numbers (here value of N is Entered by user) 💯

**C++:**
```cpp
#include <iostream>
int main() {
    int N, sum = 0;
    std::cout << "Enter a positive integer: ";
    std::cin >> N;
    for (int i = 1; i <= N; ++i) {
        sum += i;
    }
    std::cout << "Sum of first " << N << " natural numbers is " << sum << std::endl;
    return 0;
}
```

**Java:**
```java
import java.util.Scanner;

public class SumNaturalNumbers {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a positive integer: ");
        int N = scanner.nextInt();
        int sum = 0;
        for (int i = 1; i <= N; ++i) {
            sum += i;
        }
        System.out.println("Sum of first " + N + " natural numbers is " + sum);
    }
}
```

**Python:**
```python
N = int(input("Enter a positive integer: "))
sum = 0
for i in range(1, N + 1):
    sum += i
print("Sum of first", N, "natural numbers is", sum)
```

**JavaScript:**
```javascript
let N = parseInt(prompt("Enter a positive integer:"));
let sum = 0;
for (let i = 1; i <= N; i++) {
    sum += i;
}
console.log("Sum of first " + N + " natural numbers is " + sum);
```

## 2. Write a Program to Find Factorial of a given number N (N is entered by user) 🎲

**C++:**
```cpp
#include <iostream>
int main() {
    int N;
    unsigned long long factorial = 1;
    std::cout << "Enter a positive integer: ";
    std::cin >> N;
    for (int i = 1; i <= N; ++i) {
        factorial *= i;
    }
    std::cout << "Factorial of " << N << " is " << factorial << std::endl;
    return 0;
}
```

**Java:**
```java
import java.util.Scanner;

public class Factorial {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a positive integer: ");
        int N = scanner.nextInt();
        long factorial = 1;
        for (int i = 1; i <= N; ++i) {
            factorial *= i;
        }
        System.out.println("Factorial of " + N + " is " + factorial);
    }
}
```

**Python:**
```python
N = int(input("Enter a positive integer: "))
factorial = 1
for i in range(1, N + 1):
    factorial *= i
print("Factorial of", N, "is", factorial)
```

**JavaScript:**
```javascript
let N = parseInt(prompt("Enter a positive integer:"));
let factorial = 1;
for (let i = 1; i <= N; i++) {
    factorial *= i;
}
console.log("Factorial of " + N + " is " + factorial);
```

## 3. Write a Program to Generate Multiplication Table of a number (entered by the user) using a for loop 📊

**C++:**
```cpp
#include <iostream>
int main() {
    int num;
    std::cout << "Enter an integer: ";
    std::cin >> num;
    for (int i = 1; i <= 10; ++i) {
        std::cout << num << " * " << i << " = " << num * i << std::endl;
    }
    return 0;
}
```

**Java:**
```java
import java.util.Scanner;

public class MultiplicationTable {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter an integer: ");
        int num = scanner.nextInt();
        for (int i = 1; i <= 10; ++i) {
            System.out.println(num + " * " + i + " = " + (num * i));
        }
    }
}
```

**Python:**
```python
num = int(input("Enter an integer: "))
for i in range(1, 11):
    print(num, "*", i, "=", num * i)
```

**JavaScript:**
```javascript
let num = parseInt(prompt("Enter an integer:"));
for (let i = 1; i <= 10; i++) {
    console.log(num + " * " + i + " = " + (num * i));
}
```

## 4. Write a Program to Display Fibonacci Series upto nth term (n is entered by user) 🌀

**C++:**
```cpp
#include <iostream>
int main() {
    int n, t1 = 0, t2 = 1, nextTerm;
    std::cout << "Enter the number of terms: ";
    std::cin >> n;
    std::cout << "Fibonacci Series: ";
    for (int i = 1; i <= n; ++i) {
        std::cout << t1 << ", ";
        nextTerm = t1 + t2;
        t1 = t2;
        t2 = nextTerm;
    }
    return 0;
}
```

**Java:**
```java
import java.util.Scanner;

public class FibonacciSeries {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the number of terms: ");
        int n = scanner.nextInt();
        int t1 = 0, t2 = 1;
        System.out.print("Fibonacci Series: ");
        for (int i = 1; i <= n; ++i) {
            System.out.print(t1 + ", ");
            int nextTerm = t1 + t2;
            t1 = t2;
            t2 = nextTerm;
        }
    }
}
```

**Python:**
```python
n = int(input("Enter the number of terms: "))
t1, t2 = 0, 1
print("Fibonacci Series:", end=" ")
for i in range(n):
    print(t1, end=", ")
    t1, t2 = t2, t1 + t2
```

**JavaScript:**
```javascript
let n = parseInt(prompt("Enter the number of terms:"));
let t1 = 0, t2 = 1, nextTerm;
console.log("Fibonacci Series:");
for (let i = 1; i <= n; i++) {
    console.log(t1 + ", ");
    nextTerm = t1 + t2;
    t1 = t2;
    t2 = nextTerm;
}
```

## 5. Write a Program to Display Fibonacci Series upto certain number n (n is entered by user) 🌀

**C++:**
```cpp
#include <iostream>
int main() {
    int n, t1 = 0, t2 = 1, nextTerm = 0;
    std::cout << "Enter a positive integer: ";
    std::cin >> n;
    std::cout << "Fibonacci Series: ";
    while (nextTerm <= n) {
        std::cout << nextTerm << ", ";
        t1 = t2;
        t2 = nextTerm;
        nextTerm = t1 + t2;
    }
    return 0;
}
```

**Java:**
```java
import java.util.Scanner;

public class FibonacciSeriesUptoN {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a positive integer: ");
        int n = scanner.nextInt();
        int t1 = 0, t2 = 1, nextTerm = 0;
        System.out.print("Fibonacci Series: ");
        while (nextTerm <= n) {
            System.out.print(nextTerm + ", ");
            t1 = t2;
            t2 = nextTerm;
            nextTerm = t1 + t2;
        }
    }
}
```

**Python:**
```python
n = int(input("Enter a positive integer: "))
t1, t2 = 0, 1
nextTerm = 0
print("Fibonacci Series:", end=" ")
while nextTerm <= n:
    print(nextTerm, end=", ")
    t1, t2 = t2, nextTerm
    nextTerm = t1 + t2
```

**JavaScript:**
```javascript
let n = parseInt(prompt("Enter a positive integer:"));
let t1 = 0, t2 = 1, nextTerm = 0;
console.log("Fibonacci Series:");
while (nextTerm <= n) {
    console.log(nextTerm + ", ");
    t1 = t2;
    t2 = nextTerm;
    nextTerm = t1 + t2;
}
```


# Programming Problems and Solutions 🚀

## 6. Write a Program to Find GCD or HCF of two numbers entered by user 🤔

**C++:**
```cpp
#include <iostream>
int main() {
    int a, b;
    std::cout << "Enter two integers: ";
    std::cin >> a >> b;
    while (b != 0) {
        int temp = b;
        b = a % b;
        a = temp;
    }
    std::cout << "GCD is " << a << std::endl;
    return 0;
}
```

**Java:**
```java
import java.util.Scanner;

public class GCD {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter two integers: ");
        int a = scanner.nextInt();
        int b = scanner.nextInt();
        while (b != 0) {
            int temp = b;
            b = a % b;
            a = temp;
        }
        System.out.println("GCD is " + a);
    }
}
```

**Python:**
```python
def gcd(a, b):
    while b != 0:
        a, b = b, a % b
    return a

a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
print("GCD is", gcd(a, b))
```

**JavaScript:**
```javascript
function gcd(a, b) {
    while (b != 0) {
        let temp = b;
        b = a % b;
        a = temp;
    }
    return a;
}

let a = parseInt(prompt("Enter first number:"));
let b = parseInt(prompt("Enter second number:"));
console.log("GCD is " + gcd(a, b));
```

## 7. Write a Program to Find LCM of two numbers entered by user 📏

**C++:**
```cpp
#include <iostream>
int gcd(int a, int b) {
    while (b != 0) {
        int temp = b;
        b = a % b;
        a = temp;
    }
    return a;
}

int lcm(int a, int b) {
    return (a * b) / gcd(a, b);
}

int main() {
    int a, b;
    std::cout << "Enter two integers: ";
    std::cin >> a >> b;
    std::cout << "LCM is " << lcm(a, b) << std::endl;
    return 0;
}
```

**Java:**
```java
import java.util.Scanner;

public class LCM {
    public static int gcd(int a, int b) {
        while (b != 0) {
            int temp = b;
            b = a % b;
            a = temp;
        }
        return a;
    }

    public static int lcm(int a, int b) {
        return (a * b) / gcd(a, b);
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter two integers: ");
        int a = scanner.nextInt();
        int b = scanner.nextInt();
        System.out.println("LCM is " + lcm(a, b));
    }
}
```

**Python:**
```python
def gcd(a, b):
    while b != 0:
        a, b = b, a % b
    return a

def lcm(a, b):
    return (a * b) // gcd(a, b)

a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
print("LCM is", lcm(a, b))
```

**JavaScript:**
```javascript
function gcd(a, b) {
    while (b != 0) {
        let temp = b;
        b = a % b;
        a = temp;
    }
    return a;
}

function lcm(a, b) {
    return (a * b) / gcd(a, b);
}

let a = parseInt(prompt("Enter first number:"));
let b = parseInt(prompt("Enter second number:"));
console.log("LCM is " + lcm(a, b));
```

## 8. Write a Program to Reverse a given Number N by user 🔄

**C++:**
```cpp
#include <iostream>
int main() {
    int n, reversed = 0;
    std::cout << "Enter an integer: ";
    std::cin >> n;
    while (n != 0) {
        int digit = n % 10;
        reversed = reversed * 10 + digit;
        n /= 10;
    }
    std::cout << "Reversed number is " << reversed << std::endl;
    return 0;
}
```

**Java:**
```java
import java.util.Scanner;

public class ReverseNumber {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter an integer: ");
        int n = scanner.nextInt();
        int reversed = 0;
        while (n != 0) {
            int digit = n % 10;
            reversed = reversed * 10 + digit;
            n /= 10;
        }
        System.out.println("Reversed number is " + reversed);
    }
}
```

**Python:**
```python
n = int(input("Enter an integer: "))
reversed_num = 0
while n != 0:
    digit = n % 10
    reversed_num = reversed_num * 10 + digit
    n //= 10
print("Reversed number is", reversed_num)
```

**JavaScript:**
```javascript
let n = parseInt(prompt("Enter an integer:"));
let reversed = 0;
while (n != 0) {
    let digit = n % 10;
    reversed = reversed * 10 + digit;
    n = Math.floor(n / 10);
}
console.log("Reversed number is " + reversed);
```

## 9. Write a Program to display sum of all digits of a given Number N by user ➕

**C++:**
```cpp
#include <iostream>
int main() {
    int n, sum = 0;
    std::cout << "Enter an integer: ";
    std::cin >> n;
    while (n != 0) {
        sum += n % 10;
        n /= 10;
    }
    std::cout << "Sum of digits is " << sum << std::endl;
    return 0;
}
```

**Java:**
```java
import java.util.Scanner;

public class SumOfDigits {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter an integer: ");
        int n = scanner.nextInt();
        int sum = 0;
        while (n != 0) {
            sum += n % 10;
            n /= 10;
        }
        System.out.println("Sum of digits is " + sum);
    }
}
```

**Python:**
```python
n = int(input("Enter an integer: "))
sum_of_digits = 0
while n != 0:
    sum_of_digits += n % 10
    n //= 10
print("Sum of digits is", sum_of_digits)
```

**JavaScript:**
```javascript
let n = parseInt(prompt("Enter an integer:"));
let sum = 0;
while (n != 0) {
    sum += n % 10;
    n = Math.floor(n / 10);
}
console.log("Sum of digits is " + sum);
```

## 10. Write a Program to Calculate Power of a Number using inbuilt pow() function by taking two inputs from users as Base and exponent respectively 🌟

**C++:**
```cpp
#include <iostream>
#include <cmath>
int main() {
    double base, exponent;
    std::cout << "Enter base and exponent: ";
    std::cin >> base >> exponent;
    double result = pow(base, exponent);
    std::cout << base << "^" << exponent << " = " << result << std::endl;
    return 0;
}
```

**Java:**
```java
import java.util.Scanner;

public class PowerUsingPow {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter base and exponent: ");
        double base = scanner.nextDouble();
        double exponent = scanner.nextDouble();
        double result = Math.pow(base, exponent);
        System.out.println(base + "^" + exponent + " = " + result);
    }
}
```

**Python:**
```python
base = float(input("Enter base: "))
exponent = float(input("Enter exponent: "))
result = pow(base, exponent)
print(f"{base}^{exponent} = {result}")
```

**JavaScript:**
```javascript
let base = parseFloat(prompt("Enter base:"));
let exponent = parseFloat(prompt("Enter exponent:"));
let result = Math.pow(base, exponent);
console.log(`${base}^${exponent} = ${result}`);
```


Here’s how you can structure your GitHub Markdown file with the questions, code solutions in C++, Java, Python, and JavaScript, and relevant emojis:


## 11. Write a Program to Calculate Power of a Number without using inbuilt pow() function by taking two inputs from users as Base and exponent respectively 🔢✨

**C++:**
```cpp
#include <iostream>
#include <cmath>

int main() {
    double base, exponent, result = 1;
    std::cout << "Enter base and exponent: ";
    std::cin >> base >> exponent;
    
    for (int i = 0; i < exponent; ++i) {
        result *= base;
    }
    
    std::cout << base << "^" << exponent << " = " << result << std::endl;
    return 0;
}
```

**Java:**
```java
import java.util.Scanner;

public class PowerWithoutPow {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter base and exponent: ");
        double base = scanner.nextDouble();
        int exponent = scanner.nextInt();
        double result = 1;
        
        for (int i = 0; i < exponent; i++) {
            result *= base;
        }
        
        System.out.println(base + "^" + exponent + " = " + result);
    }
}
```

**Python:**
```python
base = float(input("Enter base: "))
exponent = int(input("Enter exponent: "))
result = 1

for _ in range(exponent):
    result *= base

print(f"{base}^{exponent} = {result}")
```

**JavaScript:**
```javascript
let base = parseFloat(prompt("Enter base:"));
let exponent = parseInt(prompt("Enter exponent:"));
let result = 1;

for (let i = 0; i < exponent; i++) {
    result *= base;
}

console.log(`${base}^${exponent} = ${result}`);
```

## 12. Write a Program to Check Whether a Number N entered by user is Palindrome or Not 🔄📏

**C++:**
```cpp
#include <iostream>
int main() {
    int n, reversed = 0, original, remainder;
    std::cout << "Enter an integer: ";
    std::cin >> n;
    original = n;
    
    while (n != 0) {
        remainder = n % 10;
        reversed = reversed * 10 + remainder;
        n /= 10;
    }
    
    if (original == reversed)
        std::cout << original << " is a Palindrome." << std::endl;
    else
        std::cout << original << " is not a Palindrome." << std::endl;
    
    return 0;
}
```

**Java:**
```java
import java.util.Scanner;

public class Palindrome {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter an integer: ");
        int n = scanner.nextInt();
        int reversed = 0, original = n, remainder;
        
        while (n != 0) {
            remainder = n % 10;
            reversed = reversed * 10 + remainder;
            n /= 10;
        }
        
        if (original == reversed)
            System.out.println(original + " is a Palindrome.");
        else
            System.out.println(original + " is not a Palindrome.");
    }
}
```

**Python:**
```python
n = int(input("Enter an integer: "))
original = n
reversed_num = 0

while n != 0:
    remainder = n % 10
    reversed_num = reversed_num * 10 + remainder
    n //= 10

if original == reversed_num:
    print(f"{original} is a Palindrome.")
else:
    print(f"{original} is not a Palindrome.")
```

**JavaScript:**
```javascript
let n = parseInt(prompt("Enter an integer:"));
let original = n;
let reversed = 0;

while (n != 0) {
    let remainder = n % 10;
    reversed = reversed * 10 + remainder;
    n = Math.floor(n / 10);
}

if (original === reversed) {
    console.log(original + " is a Palindrome.");
} else {
    console.log(original + " is not a Palindrome.");
}
```

## 13. Write a Program to Check Whether a Number is Prime or Not 🌟🔢

**C++:**
```cpp
#include <iostream>
bool isPrime(int n) {
    if (n <= 1) return false;
    for (int i = 2; i <= n / 2; ++i) {
        if (n % i == 0) return false;
    }
    return true;
}

int main() {
    int n;
    std::cout << "Enter a number: ";
    std::cin >> n;
    if (isPrime(n))
        std::cout << n << " is a Prime number." << std::endl;
    else
        std::cout << n << " is not a Prime number." << std::endl;
    return 0;
}
```

**Java:**
```java
import java.util.Scanner;

public class PrimeNumber {
    public static boolean isPrime(int n) {
        if (n <= 1) return false;
        for (int i = 2; i <= n / 2; i++) {
            if (n % i == 0) return false;
        }
        return true;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int n = scanner.nextInt();
        if (isPrime(n))
            System.out.println(n + " is a Prime number.");
        else
            System.out.println(n + " is not a Prime number.");
    }
}
```

**Python:**
```python
def is_prime(n):
    if n <= 1:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

n = int(input("Enter a number: "))
if is_prime(n):
    print(f"{n} is a Prime number.")
else:
    print(f"{n} is not a Prime number.")
```

**JavaScript:**
```javascript
function isPrime(n) {
    if (n <= 1) return false;
    for (let i = 2; i <= n / 2; i++) {
        if (n % i === 0) return false;
    }
    return true;
}

let n = parseInt(prompt("Enter a number:"));
if (isPrime(n)) {
    console.log(n + " is a Prime number.");
} else {
    console.log(n + " is not a Prime number.");
}
```

## 14. Write a Program to Display Prime Numbers Between Two Intervals (entered by user) 📈🔢

**C++:**
```cpp
#include <iostream>
bool isPrime(int n) {
    if (n <= 1) return false;
    for (int i = 2; i <= n / 2; ++i) {
        if (n % i == 0) return false;
    }
    return true;
}

int main() {
    int lower, upper;
    std::cout << "Enter two numbers (intervals): ";
    std::cin >> lower >> upper;
    std::cout << "Prime numbers between " << lower << " and " << upper << " are:" << std::endl;
    for (int i = lower; i <= upper; ++i) {
        if (isPrime(i)) {
            std::cout << i << " ";
        }
    }
    std::cout << std::endl;
    return 0;
}
```

**Java:**
```java
import java.util.Scanner;

public class PrimeNumbersBetweenIntervals {
    public static boolean isPrime(int n) {
        if (n <= 1) return false;
        for (int i = 2; i <= n / 2; i++) {
            if (n % i == 0) return false;
        }
        return true;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter two numbers (intervals): ");
        int lower = scanner.nextInt();
        int upper = scanner.nextInt();
        System.out.println("Prime numbers between " + lower + " and " + upper + " are:");
        for (int i = lower; i <= upper; i++) {
            if (isPrime(i)) {
                System.out.print(i + " ");
            }
        }
    }
}
```

**Python:**
```python
def is_prime(n):
    if n <= 1:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

lower = int(input("Enter the lower bound: "))
upper = int(input("Enter the upper bound: "))
print(f"Prime numbers between {lower} and {upper} are:")
for num in range(lower, upper + 1):
    if is_prime(num):
        print(num, end=' ')
print()
```

**JavaScript:**
```javascript
function isPrime(n) {
    if (n <= 1) return false;
    for (let i = 2; i

 <= n / 2; i++) {
        if (n % i === 0) return false;
    }
    return true;
}

let lower = parseInt(prompt("Enter the lower bound:"));
let upper = parseInt(prompt("Enter the upper bound:"));
console.log(`Prime numbers between ${lower} and ${upper} are:`);
for (let i = lower; i <= upper; i++) {
    if (isPrime(i)) {
        console.log(i);
    }
}
```

## 15. Write a Program to Check Whether a Number Entered by the User is an Armstrong Number or Not 🌟🔢

**C++:**
```cpp
#include <iostream>
#include <cmath>

int main() {
    int n, original, sum = 0, digits = 0;
    std::cout << "Enter a number: ";
    std::cin >> n;
    original = n;
    
    // Count the number of digits
    while (original != 0) {
        original /= 10;
        ++digits;
    }
    
    original = n;
    
    // Calculate the sum of the power of digits
    while (original != 0) {
        int remainder = original % 10;
        sum += std::pow(remainder, digits);
        original /= 10;
    }
    
    if (sum == n)
        std::cout << n << " is an Armstrong number." << std::endl;
    else
        std::cout << n << " is not an Armstrong number." << std::endl;
    
    return 0;
}
```

**Java:**
```java
import java.util.Scanner;

public class ArmstrongNumber {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int n = scanner.nextInt();
        int original = n, sum = 0, digits = 0;
        
        // Count the number of digits
        while (original != 0) {
            original /= 10;
            digits++;
        }
        
        original = n;
        
        // Calculate the sum of the power of digits
        while (original != 0) {
            int remainder = original % 10;
            sum += Math.pow(remainder, digits);
            original /= 10;
        }
        
        if (sum == n)
            System.out.println(n + " is an Armstrong number.");
        else
            System.out.println(n + " is not an Armstrong number.");
    }
}
```

**Python:**
```python
n = int(input("Enter a number: "))
original = n
sum = 0
digits = len(str(n))

while n != 0:
    remainder = n % 10
    sum += remainder ** digits
    n //= 10

if sum == original:
    print(f"{original} is an Armstrong number.")
else:
    print(f"{original} is not an Armstrong number.")
```

**JavaScript:**
```javascript
let n = parseInt(prompt("Enter a number:"));
let original = n;
let sum = 0;
const digits = (n + '').length;

while (n !== 0) {
    let remainder = n % 10;
    sum += Math.pow(remainder, digits);
    n = Math.floor(n / 10);
}

if (sum === original) {
    console.log(original + " is an Armstrong number.");
} else {
    console.log(original + " is not an Armstrong number.");
}
```

## 16. Write a Program to Display All Factors of a Number Entered by User 🔍🔢

**C++:**
```cpp
#include <iostream>
int main() {
    int n;
    std::cout << "Enter a number: ";
    std::cin >> n;
    std::cout << "Factors of " << n << " are:" << std::endl;
    for (int i = 1; i <= n; ++i) {
        if (n % i == 0) {
            std::cout << i << " ";
        }
    }
    std::cout << std::endl;
    return 0;
}
```

**Java:**
```java
import java.util.Scanner;

public class Factors {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int n = scanner.nextInt();
        System.out.println("Factors of " + n + " are:");
        for (int i = 1; i <= n; i++) {
            if (n % i == 0) {
                System.out.print(i + " ");
            }
        }
    }
}
```

**Python:**
```python
n = int(input("Enter a number: "))
print(f"Factors of {n} are:")
for i in range(1, n + 1):
    if n % i == 0:
        print(i, end=' ')
print()
```

**JavaScript:**
```javascript
let n = parseInt(prompt("Enter a number:"));
console.log(`Factors of ${n} are:`);
for (let i = 1; i <= n; i++) {
    if (n % i === 0) {
        console.log(i);
    }
}
```
