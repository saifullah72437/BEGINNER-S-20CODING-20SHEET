# Programming Challenges and Solutions 💻🚀

## 1. Write a Program that Takes N Elements (Max. Value of N is 100 and N is a Float Number Specified by User) from User, Stores Data in an Array, and Calculates the Average of Those Numbers 📊🌟

### C++

```cpp
#include <iostream>
using namespace std;

int main() {
    int N;
    float sum = 0.0, average;

    cout << "Enter the number of elements (max 100): ";
    cin >> N;

    if (N > 100) {
        cout << "N should not exceed 100." << endl;
        return 1;
    }

    float numbers[N];
    cout << "Enter " << N << " numbers:" << endl;
    for (int i = 0; i < N; ++i) {
        cin >> numbers[i];
        sum += numbers[i];
    }

    average = sum / N;
    cout << "Average of the entered numbers is: " << average << endl;

    return 0;
}
```

### Java

```java
import java.util.Scanner;

public class AverageOfNumbers {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the number of elements (max 100): ");
        int N = scanner.nextInt();
        
        if (N > 100) {
            System.out.println("N should not exceed 100.");
            return;
        }

        float[] numbers = new float[N];
        float sum = 0.0f;
        System.out.println("Enter " + N + " numbers:");
        for (int i = 0; i < N; ++i) {
            numbers[i] = scanner.nextFloat();
            sum += numbers[i];
        }

        float average = sum / N;
        System.out.println("Average of the entered numbers is: " + average);
    }
}
```

### Python

```python
# Program to calculate the average of N numbers
N = int(input("Enter the number of elements (max 100): "))

if N > 100:
    print("N should not exceed 100.")
    exit()

numbers = []
print(f"Enter {N} numbers:")
for _ in range(N):
    num = float(input())
    numbers.append(num)

average = sum(numbers) / N
print(f"Average of the entered numbers is: {average}")
```

### JavaScript

```javascript
// Function to calculate the average of N numbers
function calculateAverage() {
    let N = parseInt(prompt("Enter the number of elements (max 100):"), 10);
    
    if (N > 100) {
        console.log("N should not exceed 100.");
        return;
    }

    let numbers = [];
    let sum = 0;
    console.log(`Enter ${N} numbers:`);
    for (let i = 0; i < N; i++) {
        numbers[i] = parseFloat(prompt(`Enter number ${i + 1}:`));
        sum += numbers[i];
    }

    let average = sum / N;
    console.log(`Average of the entered numbers is: ${average}`);
}

calculateAverage();
```

---

## 2. Write a Program that Takes N Elements from User and Displays the Largest Element of an Array 📈🌟

### C++

```cpp
#include <iostream>
using namespace std;

int main() {
    int N;

    cout << "Enter the number of elements: ";
    cin >> N;

    float numbers[N];
    cout << "Enter " << N << " numbers:" << endl;
    for (int i = 0; i < N; ++i) {
        cin >> numbers[i];
    }

    float largest = numbers[0];
    for (int i = 1; i < N; ++i) {
        if (numbers[i] > largest) {
            largest = numbers[i];
        }
    }

    cout << "The largest element is: " << largest << endl;

    return 0;
}
```

### Java

```java
import java.util.Scanner;

public class LargestElement {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the number of elements: ");
        int N = scanner.nextInt();

        float[] numbers = new float[N];
        System.out.println("Enter " + N + " numbers:");
        for (int i = 0; i < N; ++i) {
            numbers[i] = scanner.nextFloat();
        }

        float largest = numbers[0];
        for (int i = 1; i < N; ++i) {
            if (numbers[i] > largest) {
                largest = numbers[i];
            }
        }

        System.out.println("The largest element is: " + largest);
    }
}
```

### Python

```python
# Program to find the largest element in an array
N = int(input("Enter the number of elements: "))

numbers = []
print(f"Enter {N} numbers:")
for _ in range(N):
    num = float(input())
    numbers.append(num)

largest = max(numbers)
print(f"The largest element is: {largest}")
```

### JavaScript

```javascript
// Function to find the largest element in an array
function findLargestElement() {
    let N = parseInt(prompt("Enter the number of elements:"), 10);
    let numbers = [];
    console.log(`Enter ${N} numbers:`);
    for (let i = 0; i < N; i++) {
        numbers[i] = parseFloat(prompt(`Enter number ${i + 1}:`));
    }

    let largest = numbers[0];
    for (let i = 1; i < N; i++) {
        if (numbers[i] > largest) {
            largest = numbers[i];
        }
    }

    console.log(`The largest element is: ${largest}`);
}

findLargestElement();
```

---

## 3. Write a Program that Calculates the Standard Deviation of 10 Data Using Arrays 📏🔢

### C++

```cpp
#include <iostream>
#include <cmath>
using namespace std;

int main() {
    const int N = 10;
    float numbers[N];
    float sum = 0.0, mean, variance = 0.0, standardDeviation;

    cout << "Enter " << N << " numbers:" << endl;
    for (int i = 0; i < N; ++i) {
        cin >> numbers[i];
        sum += numbers[i];
    }

    mean = sum / N;

    for (int i = 0; i < N; ++i) {
        variance += pow(numbers[i] - mean, 2);
    }

    variance /= N;
    standardDeviation = sqrt(variance);

    cout << "Standard Deviation is: " << standardDeviation << endl;

    return 0;
}
```

### Java

```java
import java.util.Scanner;

public class StandardDeviation {

    public static void main(String[] args) {
        final int N = 10;
        Scanner scanner = new Scanner(System.in);
        float[] numbers = new float[N];
        float sum = 0.0f, mean, variance = 0.0f, standardDeviation;

        System.out.println("Enter " + N + " numbers:");
        for (int i = 0; i < N; ++i) {
            numbers[i] = scanner.nextFloat();
            sum += numbers[i];
        }

        mean = sum / N;

        for (int i = 0; i < N; ++i) {
            variance += Math.pow(numbers[i] - mean, 2);
        }

        variance /= N;
        standardDeviation = (float) Math.sqrt(variance);

        System.out.println("Standard Deviation is: " + standardDeviation);
    }
}
```

### Python

```python
import math

# Program to calculate the standard deviation of 10 data points
N = 10
numbers = []
print(f"Enter {N} numbers:")
for _ in range(N):
    num = float(input())
    numbers.append(num)

mean = sum(numbers) / N
variance = sum((x - mean) ** 2 for x in numbers) / N
standard_deviation = math.sqrt(variance)

print(f"Standard Deviation is: {standard_deviation}")
```

### JavaScript

```javascript
// Function to calculate the standard deviation of 10 data points
function calculateStandardDeviation() {
    const N = 10;
    let numbers = [];
    let sum = 0;

    console.log(`Enter ${N} numbers:`);
    for (let i = 0; i < N; i++) {
        numbers[i] = parseFloat(prompt(`Enter number ${i + 1}:`));
        sum += numbers[i];
    }

    let mean = sum / N;
    let variance = 0;

    for (let i = 0; i < N; i++) {
        variance += Math.pow(numbers[i] - mean, 2);
    }

    variance /= N;
    let standardDeviation = Math.sqrt(variance);

    console.log(`Standard Deviation is: ${standardDeviation}`);
}

calculateStandardDeviation();
```

---

## 4. Write a Program that Takes the Array of Five Elements and the Elements of That Array Are Accessed Using Pointer 📑🔗

### C++

```cpp
#include <iostream>
using namespace std;

int main() {
    const int SIZE = 5;
    int

 numbers[SIZE];

    cout << "Enter " << SIZE << " numbers:" << endl;
    for (int i = 0; i < SIZE; ++i) {
        cin >> numbers[i];
    }

    int* ptr = numbers;

    cout << "Elements of the array accessed using pointer:" << endl;
    for (int i = 0; i < SIZE; ++i) {
        cout << *(ptr + i) << endl;
    }

    return 0;
}
```

### Java

```java
public class ArrayPointer {

    public static void main(String[] args) {
        final int SIZE = 5;
        int[] numbers = new int[SIZE];

        java.util.Scanner scanner = new java.util.Scanner(System.in);
        System.out.println("Enter " + SIZE + " numbers:");
        for (int i = 0; i < SIZE; ++i) {
            numbers[i] = scanner.nextInt();
        }

        System.out.println("Elements of the array:");
        for (int i = 0; i < SIZE; ++i) {
            System.out.println(numbers[i]);
        }
    }
}
```

### Python

```python
# Program to access array elements
SIZE = 5
numbers = []
print(f"Enter {SIZE} numbers:")
for _ in range(SIZE):
    num = int(input())
    numbers.append(num)

print("Elements of the array:")
for num in numbers:
    print(num)
```

### JavaScript

```javascript
// Function to access array elements
function accessArrayElements() {
    const SIZE = 5;
    let numbers = [];

    console.log(`Enter ${SIZE} numbers:`);
    for (let i = 0; i < SIZE; i++) {
        numbers[i] = parseInt(prompt(`Enter number ${i + 1}:`), 10);
    }

    console.log("Elements of the array:");
    for (let i = 0; i < SIZE; i++) {
        console.log(numbers[i]);
    }
}

accessArrayElements();
```
