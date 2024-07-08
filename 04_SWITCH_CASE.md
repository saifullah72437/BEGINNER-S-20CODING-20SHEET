# Programming Challenges and Solutions 💻🚀

## 1. Write a Program to Make a Simple Calculator to Add, Subtract, Multiply or Divide Using Switch Case 📊➗

The program should take an arithmetic operator (`+`, `-`, `*`, `/`) and two operands from a user and perform the operation on those two operands depending on the operator entered by the user.

### C++

```cpp
#include <iostream>
using namespace std;

int main() {
    char op;
    double num1, num2, result;

    cout << "Enter an operator (+, -, *, /): ";
    cin >> op;
    cout << "Enter two operands: ";
    cin >> num1 >> num2;

    switch(op) {
        case '+':
            result = num1 + num2;
            cout << num1 << " + " << num2 << " = " << result << endl;
            break;
        case '-':
            result = num1 - num2;
            cout << num1 << " - " << num2 << " = " << result << endl;
            break;
        case '*':
            result = num1 * num2;
            cout << num1 << " * " << num2 << " = " << result << endl;
            break;
        case '/':
            if (num2 != 0) {
                result = num1 / num2;
                cout << num1 << " / " << num2 << " = " << result << endl;
            } else {
                cout << "Division by zero is not allowed." << endl;
            }
            break;
        default:
            cout << "Invalid operator!" << endl;
            break;
    }

    return 0;
}
```

### Java

```java
import java.util.Scanner;

public class SimpleCalculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter an operator (+, -, *, /): ");
        char op = scanner.next().charAt(0);
        System.out.print("Enter two operands: ");
        double num1 = scanner.nextDouble();
        double num2 = scanner.nextDouble();
        double result;

        switch (op) {
            case '+':
                result = num1 + num2;
                System.out.println(num1 + " + " + num2 + " = " + result);
                break;
            case '-':
                result = num1 - num2;
                System.out.println(num1 + " - " + num2 + " = " + result);
                break;
            case '*':
                result = num1 * num2;
                System.out.println(num1 + " * " + num2 + " = " + result);
                break;
            case '/':
                if (num2 != 0) {
                    result = num1 / num2;
                    System.out.println(num1 + " / " + num2 + " = " + result);
                } else {
                    System.out.println("Division by zero is not allowed.");
                }
                break;
            default:
                System.out.println("Invalid operator!");
                break;
        }
    }
}
```

### Python

```python
# Simple Calculator
def simple_calculator():
    op = input("Enter an operator (+, -, *, /): ")
    num1 = float(input("Enter first operand: "))
    num2 = float(input("Enter second operand: "))

    if op == '+':
        result = num1 + num2
        print(f"{num1} + {num2} = {result}")
    elif op == '-':
        result = num1 - num2
        print(f"{num1} - {num2} = {result}")
    elif op == '*':
        result = num1 * num2
        print(f"{num1} * {num2} = {result}")
    elif op == '/':
        if num2 != 0:
            result = num1 / num2
            print(f"{num1} / {num2} = {result}")
        else:
            print("Division by zero is not allowed.")
    else:
        print("Invalid operator!")

simple_calculator()
```

### JavaScript

```javascript
// Simple Calculator
function simpleCalculator() {
    let op = prompt("Enter an operator (+, -, *, /):");
    let num1 = parseFloat(prompt("Enter first operand:"));
    let num2 = parseFloat(prompt("Enter second operand:"));
    let result;

    switch (op) {
        case '+':
            result = num1 + num2;
            console.log(`${num1} + ${num2} = ${result}`);
            break;
        case '-':
            result = num1 - num2;
            console.log(`${num1} - ${num2} = ${result}`);
            break;
        case '*':
            result = num1 * num2;
            console.log(`${num1} * ${num2} = ${result}`);
            break;
        case '/':
            if (num2 !== 0) {
                result = num1 / num2;
                console.log(`${num1} / ${num2} = ${result}`);
            } else {
                console.log("Division by zero is not allowed.");
            }
            break;
        default:
            console.log("Invalid operator!");
            break;
    }
}

simpleCalculator();
```
