# Programming Challenges 📚💻

## 1. Write a Program to Find the Frequency of a Given Character in a String 🔠

### C++

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string str;
    char ch;
    int count = 0;

    cout << "Enter a string: ";
    getline(cin, str);

    cout << "Enter the character to find its frequency: ";
    cin >> ch;

    for (char c : str) {
        if (c == ch) {
            count++;
        }
    }

    cout << "Frequency of '" << ch << "' is: " << count << endl;

    return 0;
}
```

### Java

```java
import java.util.Scanner;

public class CharacterFrequency {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter a string: ");
        String str = scanner.nextLine();

        System.out.print("Enter the character to find its frequency: ");
        char ch = scanner.next().charAt(0);

        int count = 0;
        for (char c : str.toCharArray()) {
            if (c == ch) {
                count++;
            }
        }

        System.out.println("Frequency of '" + ch + "' is: " + count);
    }
}
```

### Python

```python
# Program to find the frequency of a character in a string
str_input = input("Enter a string: ")
char = input("Enter the character to find its frequency: ")

count = str_input.count(char)

print(f"Frequency of '{char}' is: {count}")
```

### JavaScript

```javascript
// Function to find the frequency of a given character in a string
function findCharacterFrequency() {
    let str = prompt("Enter a string:");
    let char = prompt("Enter the character to find its frequency:");

    let count = 0;
    for (let c of str) {
        if (c === char) {
            count++;
        }
    }

    console.log(`Frequency of '${char}' is: ${count}`);
}

findCharacterFrequency();
```

---

## 2. Write a Program to Find the Number of Vowels, Consonants, Digits, and White Spaces in a String 🅰️🔡🔢

### C++

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string str;
    int vowels = 0, consonants = 0, digits = 0, spaces = 0;

    cout << "Enter a string: ";
    getline(cin, str);

    for (char c : str) {
        if (c == ' ') {
            spaces++;
        } else if (isdigit(c)) {
            digits++;
        } else if (isalpha(c)) {
            char lower = tolower(c);
            if (lower == 'a' || lower == 'e' || lower == 'i' || lower == 'o' || lower == 'u') {
                vowels++;
            } else {
                consonants++;
            }
        }
    }

    cout << "Number of vowels: " << vowels << endl;
    cout << "Number of consonants: " << consonants << endl;
    cout << "Number of digits: " << digits << endl;
    cout << "Number of white spaces: " << spaces << endl;

    return 0;
}
```

### Java

```java
import java.util.Scanner;

public class StringAnalysis {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter a string: ");
        String str = scanner.nextLine();

        int vowels = 0, consonants = 0, digits = 0, spaces = 0;

        for (char c : str.toCharArray()) {
            if (c == ' ') {
                spaces++;
            } else if (Character.isDigit(c)) {
                digits++;
            } else if (Character.isLetter(c)) {
                char lower = Character.toLowerCase(c);
                if (lower == 'a' || lower == 'e' || lower == 'i' || lower == 'o' || lower == 'u') {
                    vowels++;
                } else {
                    consonants++;
                }
            }
        }

        System.out.println("Number of vowels: " + vowels);
        System.out.println("Number of consonants: " + consonants);
        System.out.println("Number of digits: " + digits);
        System.out.println("Number of white spaces: " + spaces);
    }
}
```

### Python

```python
# Program to find vowels, consonants, digits, and white spaces in a string
str_input = input("Enter a string: ")

vowels = consonants = digits = spaces = 0

for char in str_input:
    if char.isspace():
        spaces += 1
    elif char.isdigit():
        digits += 1
    elif char.isalpha():
        if char.lower() in 'aeiou':
            vowels += 1
        else:
            consonants += 1

print(f"Number of vowels: {vowels}")
print(f"Number of consonants: {consonants}")
print(f"Number of digits: {digits}")
print(f"Number of white spaces: {spaces}")
```

### JavaScript

```javascript
// Function to find the number of vowels, consonants, digits, and white spaces in a string
function analyzeString() {
    let str = prompt("Enter a string:");
    let vowels = 0, consonants = 0, digits = 0, spaces = 0;

    for (let c of str) {
        if (c === ' ') {
            spaces++;
        } else if (/\d/.test(c)) {
            digits++;
        } else if (/[a-zA-Z]/.test(c)) {
            if ('aeiou'.includes(c.toLowerCase())) {
                vowels++;
            } else {
                consonants++;
            }
        }
    }

    console.log(`Number of vowels: ${vowels}`);
    console.log(`Number of consonants: ${consonants}`);
    console.log(`Number of digits: ${digits}`);
    console.log(`Number of white spaces: ${spaces}`);
}

analyzeString();
```

---

## 3. Write a Program to Remove All Characters in a String Except Alphabets. Example: Enter a String: `p2'r"o@gram84iz./` Output String: `programiz` ✂️🔤

### C++

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string str, result;
    cout << "Enter a string: ";
    getline(cin, str);

    for (char c : str) {
        if (isalpha(c)) {
            result += c;
        }
    }

    cout << "Output String: " << result << endl;

    return 0;
}
```

### Java

```java
import java.util.Scanner;

public class RemoveNonAlphabets {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter a string: ");
        String str = scanner.nextLine();

        StringBuilder result = new StringBuilder();

        for (char c : str.toCharArray()) {
            if (Character.isLetter(c)) {
                result.append(c);
            }
        }

        System.out.println("Output String: " + result.toString());
    }
}
```

### Python

```python
# Program to remove all characters except alphabets
str_input = input("Enter a string: ")

result = ''.join(char for char in str_input if char.isalpha())

print(f"Output String: {result}")
```

### JavaScript

```javascript
// Function to remove all characters except alphabets
function removeNonAlphabets() {
    let str = prompt("Enter a string:");
    let result = str.replace(/[^a-zA-Z]/g, '');

    console.log(`Output String: ${result}`);
}

removeNonAlphabets();
```

---

## 4. Write a Program to Find the Length of a String Entered by User 📏

### C++

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string str;
    cout << "Enter a string: ";
    getline(cin, str);

    cout << "Length of the string is: " << str.length() << endl;

    return 0;
}
```

### Java

```java
import java.util.Scanner;

public class StringLength {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter a string: ");
        String str = scanner.nextLine();

        System.out.println("Length of the string is: " + str.length());
    }
}
```

### Python

```python
# Program to find the length of a string
str_input = input("Enter a string: ")

print(f"Length of the string is: {len(str_input)}")
```

### JavaScript

```javascript
// Function to find the length of a string
function findStringLength() {
    let str = prompt("Enter a string:");
    let length = str.length;

    console.log(`Length of the string is: ${length}`);
}

findStringLength();
```

---

## 5. Write a Program to Concatenate (Join) Two Strings Entered by User 🤝📝

### C++

```cpp
#include <iostream>
#include <string>
using namespace std;

int main()

 {
    string str1, str2;

    cout << "Enter the first string: ";
    getline(cin, str1);

    cout << "Enter the second string: ";
    getline(cin, str2);

    string result = str1 + str2;

    cout << "Concatenated String: " << result << endl;

    return 0;
}
```

### Java

```java
import java.util.Scanner;

public class StringConcatenation {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the first string: ");
        String str1 = scanner.nextLine();

        System.out.print("Enter the second string: ");
        String str2 = scanner.nextLine();

        String result = str1 + str2;

        System.out.println("Concatenated String: " + result);
    }
}
```

### Python

```python
# Program to concatenate two strings
str1 = input("Enter the first string: ")
str2 = input("Enter the second string: ")

result = str1 + str2

print(f"Concatenated String: {result}")
```

### JavaScript

```javascript
// Function to concatenate two strings
function concatenateStrings() {
    let str1 = prompt("Enter the first string:");
    let str2 = prompt("Enter the second string:");

    let result = str1 + str2;

    console.log(`Concatenated String: ${result}`);
}

concatenateStrings();
```



## 6. Write a Program to Change Every Letter in a Given String with the Letter Following It in the Alphabet (e.g., a becomes b, p becomes q, z becomes a) 🔄🔠

### C++

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string str;
    cout << "Enter a string: ";
    getline(cin, str);

    for (char &c : str) {
        if (isalpha(c)) {
            if (c == 'z') c = 'a';
            else if (c == 'Z') c = 'A';
            else c++;
        }
    }

    cout << "Modified string: " << str << endl;

    return 0;
}
```

### Java

```java
import java.util.Scanner;

public class ShiftLetters {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter a string: ");
        String str = scanner.nextLine();

        StringBuilder result = new StringBuilder();

        for (char c : str.toCharArray()) {
            if (Character.isLetter(c)) {
                if (c == 'z') result.append('a');
                else if (c == 'Z') result.append('A');
                else result.append((char) (c + 1));
            } else {
                result.append(c);
            }
        }

        System.out.println("Modified string: " + result.toString());
    }
}
```

### Python

```python
# Program to shift letters to the next in the alphabet
str_input = input("Enter a string: ")

result = ''.join(chr(ord(c) + 1) if c.isalpha() and c.lower() != 'z' else 'a' if c == 'z' else c for c in str_input)

print(f"Modified string: {result}")
```

### JavaScript

```javascript
// Function to shift letters to the next in the alphabet
function shiftLetters() {
    let str = prompt("Enter a string:");
    let result = '';

    for (let c of str) {
        if (/[a-zA-Z]/.test(c)) {
            if (c === 'z') {
                result += 'a';
            } else if (c === 'Z') {
                result += 'A';
            } else {
                result += String.fromCharCode(c.charCodeAt(0) + 1);
            }
        } else {
            result += c;
        }
    }

    console.log("Modified string: " + result);
}

shiftLetters();
```

---

## 7. Write a Program to Check if a Given String is a Palindrome or Not 🪞🔄

### C++

```cpp
#include <iostream>
#include <string>
using namespace std;

bool isPalindrome(const string& str) {
    int left = 0;
    int right = str.length() - 1;

    while (left < right) {
        if (str[left] != str[right]) return false;
        left++;
        right--;
    }
    return true;
}

int main() {
    string str;
    cout << "Enter a string: ";
    getline(cin, str);

    if (isPalindrome(str)) {
        cout << "The string is a palindrome." << endl;
    } else {
        cout << "The string is not a palindrome." << endl;
    }

    return 0;
}
```

### Java

```java
import java.util.Scanner;

public class PalindromeCheck {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter a string: ");
        String str = scanner.nextLine();

        String reversed = new StringBuilder(str).reverse().toString();

        if (str.equals(reversed)) {
            System.out.println("The string is a palindrome.");
        } else {
            System.out.println("The string is not a palindrome.");
        }
    }
}
```

### Python

```python
# Program to check if a string is a palindrome
str_input = input("Enter a string: ")

if str_input == str_input[::-1]:
    print("The string is a palindrome.")
else:
    print("The string is not a palindrome.")
```

### JavaScript

```javascript
// Function to check if a string is a palindrome
function checkPalindrome() {
    let str = prompt("Enter a string:");
    let reversed = str.split('').reverse().join('');

    if (str === reversed) {
        console.log("The string is a palindrome.");
    } else {
        console.log("The string is not a palindrome.");
    }
}

checkPalindrome();
```

---

## 8. Write a Program to Count All the Words in a Given String. Words Must be Separated by Only One Space. 🗣️🧮

### C++

```cpp
#include <iostream>
#include <sstream>
#include <string>
using namespace std;

int main() {
    string str;
    cout << "Enter a string: ";
    getline(cin, str);

    stringstream ss(str);
    string word;
    int count = 0;

    while (ss >> word) {
        count++;
    }

    cout << "Number of words -> " << count << endl;

    return 0;
}
```

### Java

```java
import java.util.Scanner;

public class WordCount {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter a string: ");
        String str = scanner.nextLine();

        String[] words = str.split(" ");
        System.out.println("Number of words -> " + words.length);
    }
}
```

### Python

```python
# Program to count words in a string
str_input = input("Enter a string: ")

word_count = len(str_input.split())

print(f"Number of words -> {word_count}")
```

### JavaScript

```javascript
// Function to count words in a string
function countWords() {
    let str = prompt("Enter a string:");
    let wordCount = str.trim().split(/\s+/).length;

    console.log(`Number of words -> ${wordCount}`);
}

countWords();
```

---

## 9. Write a Program to Capitalize the First Letter of Each Word of a Given String. Words Must be Separated by Only One Space. ✨🔤

### C++

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string str;
    cout << "Enter a string: ";
    getline(cin, str);

    bool capitalize = true;

    for (char &c : str) {
        if (isalpha(c)) {
            if (capitalize) {
                c = toupper(c);
                capitalize = false;
            }
        } else {
            capitalize = true;
        }
    }

    cout << "Modified string: " << str << endl;

    return 0;
}
```

### Java

```java
import java.util.Scanner;

public class CapitalizeWords {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter a string: ");
        String str = scanner.nextLine();

        String[] words = str.split(" ");
        StringBuilder result = new StringBuilder();

        for (String word : words) {
            if (!word.isEmpty()) {
                result.append(Character.toUpperCase(word.charAt(0)))
                      .append(word.substring(1))
                      .append(" ");
            }
        }

        System.out.println("Modified string: " + result.toString().trim());
    }
}
```

### Python

```python
# Program to capitalize the first letter of each word in a string
str_input = input("Enter a string: ")

result = ' '.join(word.capitalize() for word in str_input.split())

print(f"Modified string: {result}")
```

### JavaScript

```javascript
// Function to capitalize the first letter of each word in a string
function capitalizeWords() {
    let str = prompt("Enter a string:");
    let result = str.split(' ').map(word => word.charAt(0).toUpperCase() + word.slice(1)).join(' ');

    console.log("Modified string: " + result);
}

capitalizeWords();
```

---

## 10. Write a Program to Find the Largest Word in a Given String 🌟🔠

### C++

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string str;
    cout << "Enter a string: ";
    getline(cin, str);

    string largestWord, currentWord;
    istringstream iss(str);

    while (iss >> currentWord) {
        if (currentWord.length() > largestWord.length()) {
            largestWord = currentWord;
        }
    }

    cout << "Largest word: " << largestWord << endl;

    return 0;
}
```

### Java

```java
import java.util.Scanner;

public class LargestWord {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter a string: ");
        String str = scanner.nextLine();

        String[] words = str.split(" ");
        String largestWord = "";

        for (String word : words) {
            if (word.length() > largestWord.length()) {
                largestWord = word;
            }
        }

        System.out.println("Largest word: " + largestWord);
    }
}
```

### Python

```python
# Program to find the largest word in

 a string
str_input = input("Enter a string: ")

words = str_input.split()
largest_word = max(words, key=len)

print(f"Largest word: {largest_word}")
```

### JavaScript

```javascript
// Function to find the largest word in a string
function findLargestWord() {
    let str = prompt("Enter a string:");
    let words = str.split(' ');
    let largestWord = words.reduce((max, word) => word.length > max.length ? word : max, "");

    console.log("Largest word: " + largestWord);
}

findLargestWord();
```
