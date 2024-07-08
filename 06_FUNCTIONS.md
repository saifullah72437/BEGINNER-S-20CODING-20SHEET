
# Programming Challenges and Solutions 💻🚀

## 1. Write a Program to Display Prime Numbers Between Two Intervals (entered by the user) Using Functions 🔢✨

### C++

```cpp
#include <iostream>
using namespace std;

bool isPrime(int num) {
    if (num <= 1) return false;
    for (int i = 2; i <= num / 2; ++i) {
        if (num % i == 0) return false;
    }
    return true;
}

void displayPrimes(int start, int end) {
    for (int i = start; i <= end; ++i) {
        if (isPrime(i)) {
            cout << i << " ";
        }
    }
    cout << endl;
}

int main() {
    int start, end;
    cout << "Enter the start and end of the interval: ";
    cin >> start >> end;
    cout << "Prime numbers between " << start << " and " << end << " are: ";
    displayPrimes(start, end);
    return 0;
}
```

### Java

```java
import java.util.Scanner;

public class PrimeNumbersInInterval {

    static boolean isPrime(int num) {
        if (num <= 1) return false;
        for (int i = 2; i <= num / 2; ++i) {
            if (num % i == 0) return false;
        }
        return true;
    }

    static void displayPrimes(int start, int end) {
        for (int i = start; i <= end; ++i) {
            if (isPrime(i)) {
                System.out.print(i + " ");
            }
        }
        System.out.println();
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the start and end of the interval: ");
        int start = scanner.nextInt();
        int end = scanner.nextInt();
        System.out.print("Prime numbers between " + start + " and " + end + " are: ");
        displayPrimes(start, end);
    }
}
```

### Python

```python
# Function to check if a number is prime
def is_prime(num):
    if num <= 1:
        return False
    for i in range(2, num // 2 + 1):
        if num % i == 0:
            return False
    return True

# Function to display prime numbers in a given interval
def display_primes(start, end):
    primes = [num for num in range(start, end + 1) if is_prime(num)]
    print(f"Prime numbers between {start} and {end} are: {primes}")

# Main function
start = int(input("Enter the start of the interval: "))
end = int(input("Enter the end of the interval: "))
display_primes(start, end)
```

### JavaScript

```javascript
// Function to check if a number is prime
function isPrime(num) {
    if (num <= 1) return false;
    for (let i = 2; i <= num / 2; ++i) {
        if (num % i === 0) return false;
    }
    return true;
}

// Function to display prime numbers in a given interval
function displayPrimes(start, end) {
    let primes = [];
    for (let i = start; i <= end; ++i) {
        if (isPrime(i)) {
            primes.push(i);
        }
    }
    console.log(`Prime numbers between ${start} and ${end} are: ${primes.join(' ')}`);
}

// Main
let start = parseInt(prompt("Enter the start of the interval:"));
let end = parseInt(prompt("Enter the end of the interval:"));
displayPrimes(start, end);
```

---

## 2. Write a Program to Check if an Integer (Entered by the User) Can Be Expressed as the Sum of Two Prime Numbers, If Yes, Print All Possible Combinations with the Use of Functions 🔄🔢

### C++

```cpp
#include <iostream>
using namespace std;

bool isPrime(int num) {
    if (num <= 1) return false;
    for (int i = 2; i <= num / 2; ++i) {
        if (num % i == 0) return false;
    }
    return true;
}

void findSumOfPrimes(int num) {
    for (int i = 2; i <= num / 2; ++i) {
        if (isPrime(i) && isPrime(num - i)) {
            cout << num << " = " << i << " + " << (num - i) << endl;
        }
    }
}

int main() {
    int num;
    cout << "Enter a positive integer: ";
    cin >> num;
    findSumOfPrimes(num);
    return 0;
}
```

### Java

```java
import java.util.Scanner;

public class SumOfTwoPrimes {

    static boolean isPrime(int num) {
        if (num <= 1) return false;
        for (int i = 2; i <= num / 2; ++i) {
            if (num % i == 0) return false;
        }
        return true;
    }

    static void findSumOfPrimes(int num) {
        for (int i = 2; i <= num / 2; ++i) {
            if (isPrime(i) && isPrime(num - i)) {
                System.out.println(num + " = " + i + " + " + (num - i));
            }
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a positive integer: ");
        int num = scanner.nextInt();
        findSumOfPrimes(num);
    }
}
```

### Python

```python
# Function to check if a number is prime
def is_prime(num):
    if num <= 1:
        return False
    for i in range(2, num // 2 + 1):
        if num % i == 0:
            return False
    return True

# Function to find if a number can be expressed as the sum of two primes
def find_sum_of_primes(num):
    for i in range(2, num // 2 + 1):
        if is_prime(i) and is_prime(num - i):
            print(f"{num} = {i} + {num - i}")

# Main function
num = int(input("Enter a positive integer: "))
find_sum_of_primes(num)
```

### JavaScript

```javascript
// Function to check if a number is prime
function isPrime(num) {
    if (num <= 1) return false;
    for (let i = 2; i <= num / 2; ++i) {
        if (num % i === 0) return false;
    }
    return true;
}

// Function to find if a number can be expressed as the sum of two primes
function findSumOfPrimes(num) {
    for (let i = 2; i <= num / 2; ++i) {
        if (isPrime(i) && isPrime(num - i)) {
            console.log(`${num} = ${i} + ${num - i}`);
        }
    }
}

// Main
let num = parseInt(prompt("Enter a positive integer:"));
findSumOfPrimes(num);
```

---

## 3. Write a Program to Convert Binary Number to Decimal Manually by Creating User-Defined Functions 🔢➡️🌟

### C++

```cpp
#include <iostream>
#include <cmath>
using namespace std;

int binaryToDecimal(int binary) {
    int decimal = 0, base = 1;
    while (binary > 0) {
        int lastDigit = binary % 10;
        decimal += lastDigit * base;
        base *= 2;
        binary /= 10;
    }
    return decimal;
}

int main() {
    int binary;
    cout << "Enter a binary number: ";
    cin >> binary;
    cout << "Decimal equivalent is: " << binaryToDecimal(binary) << endl;
    return 0;
}
```

### Java

```java
import java.util.Scanner;

public class BinaryToDecimal {

    static int binaryToDecimal(int binary) {
        int decimal = 0, base = 1;
        while (binary > 0) {
            int lastDigit = binary % 10;
            decimal += lastDigit * base;
            base *= 2;
            binary /= 10;
        }
        return decimal;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a binary number: ");
        int binary = scanner.nextInt();
        System.out.println("Decimal equivalent is: " + binaryToDecimal(binary));
    }
}
```

### Python

```python
# Function to convert binary number to decimal
def binary_to_decimal(binary):
    decimal = 0
    base = 1
    while binary > 0:
        last_digit = binary % 10
        decimal += last_digit * base
        base *= 2
        binary //= 10
    return decimal

# Main function
binary = int(input("Enter a binary number: "))
print("Decimal equivalent is:", binary_to_decimal(binary))
```

### JavaScript

```javascript
// Function to convert binary number

 to decimal
function binaryToDecimal(binary) {
    let decimal = 0, base = 1;
    while (binary > 0) {
        let lastDigit = binary % 10;
        decimal += lastDigit * base;
        base *= 2;
        binary = Math.floor(binary / 10);
    }
    return decimal;
}

// Main
let binary = parseInt(prompt("Enter a binary number:"), 10);
console.log("Decimal equivalent is:", binaryToDecimal(binary));
```

---

## 4. Write a Program to Convert Decimal to Binary Number Manually by Creating User-Defined Functions 🔢⬅️🌟

### C++

```cpp
#include <iostream>
using namespace std;

void decimalToBinary(int decimal) {
    int binary[32];
    int index = 0;
    while (decimal > 0) {
        binary[index++] = decimal % 2;
        decimal /= 2;
    }
    cout << "Binary equivalent is: ";
    for (int i = index - 1; i >= 0; --i) {
        cout << binary[i];
    }
    cout << endl;
}

int main() {
    int decimal;
    cout << "Enter a decimal number: ";
    cin >> decimal;
    decimalToBinary(decimal);
    return 0;
}
```

### Java

```java
import java.util.Scanner;

public class DecimalToBinary {

    static void decimalToBinary(int decimal) {
        StringBuilder binary = new StringBuilder();
        while (decimal > 0) {
            binary.insert(0, decimal % 2);
            decimal /= 2;
        }
        System.out.println("Binary equivalent is: " + binary);
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a decimal number: ");
        int decimal = scanner.nextInt();
        decimalToBinary(decimal);
    }
}
```

### Python

```python
# Function to convert decimal number to binary
def decimal_to_binary(decimal):
    binary = ''
    while decimal > 0:
        binary = str(decimal % 2) + binary
        decimal //= 2
    return binary

# Main function
decimal = int(input("Enter a decimal number: "))
print("Binary equivalent is:", decimal_to_binary(decimal))
```

### JavaScript

```javascript
// Function to convert decimal number to binary
function decimalToBinary(decimal) {
    let binary = '';
    while (decimal > 0) {
        binary = (decimal % 2) + binary;
        decimal = Math.floor(decimal / 2);
    }
    return binary;
}

// Main
let decimal = parseInt(prompt("Enter a decimal number:"), 10);
console.log("Binary equivalent is:", decimalToBinary(decimal));
```
