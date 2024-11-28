# Basic C++/Python For DSA

This is a comprehensive cheat sheet for basic Data Structures and Algorithms (DSA) concepts, including examples in C++ and Python. The cheat sheet includes various topics such as User Input/Output, Data Types, Control Flow, Arrays, Functions, and more.

---

## 1. User Input / Output

### C++:
```cpp
#include <iostream>
using namespace std;

int main() {
    // Input
    int a;
    cin >> a;  // Takes input from the user

    // Output
    cout << "You entered: " << a << endl;  // Prints the value of a

    return 0;
}
```

### Python:
```python
# Input
a = int(input("Enter a number: "))  # Takes input from the user and converts it to an integer

# Output
print("You entered:", a)  # Prints the value of a
```

---

## 2. Data Types

### C++:
```cpp
#include <iostream>
using namespace std;

int main() {
    // Integer
    int a = 5;
    // Float
    float b = 5.5;
    // Double
    double c = 10.12345;
    // Char
    char d = 'A';
    // Boolean
    bool e = true;

    cout << "Integer: " << a << endl;
    cout << "Float: " << b << endl;
    cout << "Double: " << c << endl;
    cout << "Char: " << d << endl;
    cout << "Boolean: " << e << endl;

    return 0;
}
```

### Python:
```python
# Integer
a = 5
# Float
b = 5.5
# String
s = "Hello, World!"
# Boolean
is_active = True

print("Integer:", a)
print("Float:", b)
print("String:", s)
print("Boolean:", is_active)
```

---

## 3. If Else Statements

### C++:
```cpp
#include <iostream>
using namespace std;

int main() {
    int a;
    cin >> a;

    if (a > 0) {
        cout << "Positive" << endl;
    } else if (a == 0) {
        cout << "Zero" << endl;
    } else {
        cout << "Negative" << endl;
    }

    return 0;
}
```

### Python:
```python
a = int(input("Enter a number: "))

if a > 0:
    print("Positive")
elif a == 0:
    print("Zero")
else:
    print("Negative")
```

---

## 4. Switch Statement

### C++:
```cpp
#include <iostream>
using namespace std;

int main() {
    int choice;
    cin >> choice;

    switch(choice) {
        case 1:
            cout << "Option 1" << endl;
            break;
        case 2:
            cout << "Option 2" << endl;
            break;
        default:
            cout << "Invalid choice" << endl;
    }

    return 0;
}
```

### Python:
```python
choice = int(input("Enter your choice (1 or 2): "))

# Mimicking Switch with if-elif-else
if choice == 1:
    print("Option 1")
elif choice == 2:
    print("Option 2")
else:
    print("Invalid choice")
```

---

## 5. Arrays and Strings

### C++ Arrays Example:
```cpp
#include <iostream>
using namespace std;

int main() {
    int arr[5] = {1, 2, 3, 4, 5};

    for (int i = 0; i < 5; i++) {
        cout << arr[i] << " ";  // Prints the array elements
    }

    cout << endl;
    return 0;
}
```

### Python Lists Example:
```python
arr = [1, 2, 3, 4, 5]

for item in arr:
    print(item, end=" ")  # Prints the array elements

print()
```

### C++ String Example:
```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string s = "Hello, World!";
    cout << "String: " << s << endl;

    // Accessing a character from the string
    cout << "First character: " << s[0] << endl;

    return 0;
}
```

### Python String Example:
```python
s = "Hello, World!"
print("String:", s)

# Accessing a character from the string
print("First character:", s[0])
```

---

## 6. For Loops

### C++ For Loop:
```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 0; i < 5; i++) {
        cout << "i = " << i << endl;  // Prints values of i from 0 to 4
    }

    return 0;
}
```

### Python For Loop:
```python
for i in range(5):
    print("i =", i)  # Prints values of i from 0 to 4
```

---

## 7. While Loops

### C++ While Loop:
```cpp
#include <iostream>
using namespace std;

int main() {
    int i = 0;
    while (i < 5) {
        cout << "i = " << i << endl;  // Prints values of i from 0 to 4
        i++;
    }

    return 0;
}
```

### Python While Loop:
```python
i = 0
while i < 5:
    print("i =", i)  # Prints values of i from 0 to 4
    i += 1
```

---

## 8. Functions (Pass by Reference and Value)

### C++ Pass by Value:
```cpp
#include <iostream>
using namespace std;

void byValue(int x) {
    x = 10;  // Only changes the local copy of x
    cout << "Inside byValue: " << x << endl;
}

int main() {
    int a = 5;
    byValue(a);
    cout << "Outside byValue: " << a << endl;  // a remains 5
    return 0;
}
```

### C++ Pass by Reference:
```cpp
#include <iostream>
using namespace std;

void byReference(int &x) {
    x = 10;  // Changes the original variable
    cout << "Inside byReference: " << x << endl;
}

int main() {
    int a = 5;
    byReference(a);
    cout << "Outside byReference: " << a << endl;  // a is now 10
    return 0;
}
```

### Python Pass by Value (Immutable Type):
```python
def by_value(x):
    x = 10  # Changes only the local copy of x
    print("Inside by_value:", x)

a = 5
by_value(a)
print("Outside by_value:", a)  # a remains 5
```

### Python Pass by Reference (Mutable Type):
```python
def modify_list(lst):
    lst.append(4)  # Modifies the original list

my_list = [1, 2, 3]
modify_list(my_list)
print("Modified list:", my_list)  # my_list is now [1, 2, 3, 4]
```