# Programming Questions

## 1. Write a Program to Check Whether Number is Even or Odd 🔢

**C++:**
```cpp
#include <iostream>
int main() {
    int num;
    std::cout << "Enter an integer: ";
    std::cin >> num;
    if (num % 2 == 0)
        std::cout << num << " is even.";
    else
        std::cout << num << " is odd.";
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
        int num = scanner.nextInt();
        if (num % 2 == 0) {
            System.out.println(num + " is even.");
        } else {
            System.out.println(num + " is odd.");
        }
    }
}
```

**Python:**
```python
num = int(input("Enter an integer: "))
if num % 2 == 0:
    print(num, "is even.")
else:
    print(num, "is odd.")
```

**JavaScript:**
```javascript
let num = parseInt(prompt("Enter an integer:"));
if (num % 2 === 0) {
    console.log(num + " is even.");
} else {
    console.log(num + " is odd.");
}
```

## 2. Write a Program to Check Whether a Character is Vowel or Consonant. 🔤

**C++:**
```cpp
#include <iostream>
int main() {
    char c;
    bool isVowel;
    std::cout << "Enter a character: ";
    std::cin >> c;
    isVowel = (c == 'a' || c == 'e' || c == 'i' || c == 'o' || c == 'u' || 
               c == 'A' || c == 'E' || c == 'I' || c == 'O' || c == 'U');
    if (isVowel)
        std::cout << c << " is a vowel.";
    else
        std::cout << c << " is a consonant.";
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
        if (c == 'a' || c == 'e' || c == 'i' || c == 'o' || c == 'u' || 
            c == 'A' || c == 'E' || c == 'I' || c == 'O' || c == 'U') {
            System.out.println(c + " is a vowel.");
        } else {
            System.out.println(c + " is a consonant.");
        }
    }
}
```

**Python:**
```python
c = input("Enter a character: ").lower()
if c in 'aeiou':
    print(c, "is a vowel.")
else:
    print(c, "is a consonant.")
```

**JavaScript:**
```javascript
let c = prompt("Enter a character:").toLowerCase();
if (c === 'a' || c === 'e' || c === 'i' || c === 'o' || c === 'u') {
    console.log(c + " is a vowel.");
} else {
    console.log(c + " is a consonant.");
}
```

## 3. Write a Program which accepts coefficients of a quadratic equation from the user and displays the roots (both real and complex roots depending upon the discriminant). ➗

**C++:**
```cpp
#include <iostream>
#include <cmath>
int main() {
    float a, b, c, discriminant, root1, root2, realPart, imaginaryPart;
    std::cout << "Enter coefficients a, b and c: ";
    std::cin >> a >> b >> c;
    discriminant = b*b - 4*a*c;
    if (discriminant > 0) {
        root1 = (-b + sqrt(discriminant)) / (2*a);
        root2 = (-b - sqrt(discriminant)) / (2*a);
        std::cout << "Roots are real and different." << std::endl;
        std::cout << "Root 1 = " << root1 << std::endl;
        std::cout << "Root 2 = " << root2 << std::endl;
    } else if (discriminant == 0) {
        root1 = -b / (2*a);
        std::cout << "Roots are real and same." << std::endl;
        std::cout << "Root 1 = Root 2 = " << root1 << std::endl;
    } else {
        realPart = -b / (2*a);
        imaginaryPart = sqrt(-discriminant) / (2*a);
        std::cout << "Roots are complex and different." << std::endl;
        std::cout << "Root 1 = " << realPart << "+" << imaginaryPart << "i" << std::endl;
        std::cout << "Root 2 = " << realPart << "-" << imaginaryPart << "i" << std::endl;
    }
    return 0;
}
```

**Java:**
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter coefficients a, b and c: ");
        double a = scanner.nextDouble();
        double b = scanner.nextDouble();
        double c = scanner.nextDouble();
        double discriminant = b * b - 4 * a * c;
        if (discriminant > 0) {
            double root1 = (-b + Math.sqrt(discriminant)) / (2 * a);
            double root2 = (-b - Math.sqrt(discriminant)) / (2 * a);
            System.out.println("Roots are real and different.");
            System.out.println("Root 1 = " + root1);
            System.out.println("Root 2 = " + root2);
        } else if (discriminant == 0) {
            double root = -b / (2 * a);
            System.out.println("Roots are real and same.");
            System.out.println("Root 1 = Root 2 = " + root);
        } else {
            double realPart = -b / (2 * a);
            double imaginaryPart = Math.sqrt(-discriminant) / (2 * a);
            System.out.println("Roots are complex and different.");
            System.out.println("Root 1 = " + realPart + " + " + imaginaryPart + "i");
            System.out.println("Root 2 = " + realPart + " - " + imaginaryPart + "i");
        }
    }
}
```

**Python:**
```python
import cmath

a = float(input("Enter coefficient a: "))
b = float(input("Enter coefficient b: "))
c = float(input("Enter coefficient c: "))

discriminant = (b**2) - (4*a*c)

if discriminant > 0:
    root1 = (-b + cmath.sqrt(discriminant)) / (2 * a)
    root2 = (-b - cmath.sqrt(discriminant)) / (2 * a)
    print("Roots are real and different.")
    print("Root 1 =", root1)
    print("Root 2 =", root2)
elif discriminant == 0:
    root = -b / (2 * a)
    print("Roots are real and same.")
    print("Root 1 = Root 2 =", root)
else:
    root1 = (-b / (2 * a)) + (cmath.sqrt(discriminant) / (2 * a))
    root2 = (-b / (2 * a)) - (cmath.sqrt(discriminant) / (2 * a))
    print("Roots are complex and different.")
    print("Root 1 =", root1)
    print("Root 2 =", root2)
```

**JavaScript:**
```javascript
let a = parseFloat(prompt("Enter coefficient a:"));
let b = parseFloat(prompt("Enter coefficient b:"));
let c = parseFloat(prompt("Enter coefficient c:"));
let discriminant = b * b - 4 * a * c;

if (discriminant > 0) {
    let root1 = (-b + Math.sqrt(discriminant)) / (2 * a);
    let root2 = (-b - Math.sqrt(discriminant)) / (2 * a);
    console.log("Roots are real and different.");
    console.log("Root 1 = " + root1);
    console.log("Root 2 = " + root2);
} else if (discriminant == 0) {
    let root = -b / (2 * a);
    console.log("Roots are real and same.");
    console.log("Root 1 = Root 2 = " + root);
} else {
    let realPart = (-b / (2 * a)).toFixed(2);
    let imaginaryPart = (Math.sqrt(-discriminant) / (2 * a)).toFixed(2);
    console.log("Roots are complex and different.");
    console.log("Root 1 = " + realPart + " + " + imaginaryPart + "i");
    console.log("Root 2 = " + real

Part + " - " + imaginaryPart + "i");
}
```

## 4. Write a Program to Check whether a year entered by user is Leap Year or not 📅

**C++:**
```cpp
#include <iostream>
int main() {
    int year;
    std::cout << "Enter a year: ";
    std::cin >> year;
    if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0))
        std::cout << year << " is a leap year.";
    else
        std::cout << year << " is not a leap year.";
    return 0;
}
```

**Java:**
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a year: ");
        int year = scanner.nextInt();
        if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0)) {
            System.out.println(year + " is a leap year.");
        } else {
            System.out.println(year + " is not a leap year.");
        }
    }
}
```

**Python:**
```python
year = int(input("Enter a year: "))
if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
    print(year, "is a leap year.")
else:
    print(year, "is not a leap year.")
```

**JavaScript:**
```javascript
let year = parseInt(prompt("Enter a year:"));
if ((year % 4 === 0 && year % 100 !== 0) || (year % 400 === 0)) {
    console.log(year + " is a leap year.");
} else {
    console.log(year + " is not a leap year.");
}
```
