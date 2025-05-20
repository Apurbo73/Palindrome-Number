#﻿## Palindrome Number:

This C++ program checks whether a number is a palindrome without using any functions. A palindrome number reads the same forward and backward (e.g., 121 or 1331). The program first takes an integer input from the user and stores a copy of it in the variable `originalNum`. It then reverses the number by extracting each digit using the modulus operator (`%`) and appending it to `reversedNum` after shifting its digits left by multiplying by 10. This is done inside a `while` loop that continues until the number becomes zero. After reversing the number, the program compares the reversed number with the original. If they are equal, it prints that the number is a palindrome; otherwise, it prints that it is not. The logic is simple and uses basic arithmetic operations and control structures without the use of custom functions...




### ✅ What is a Palindrome Number?

A palindrome number is a number that reads the same **forward and backward**.
Examples: `121`, `1331`, `12321`

---

### 🔷 C++ Program to Check Palindrome Number

```cpp
#include <iostream>
using namespace std;

int main() {
    int num, reversed = 0, remainder, original;
    
    cout << "Enter an integer: ";
    cin >> num;

    original = num; // Store the original number

    // Reverse the number
    while (num != 0) {
        remainder = num % 10;
        reversed = reversed * 10 + remainder;
        num /= 10;
    }

    // Check if the original and reversed numbers are the same
    if (original == reversed) {
        cout << original << " is a palindrome number." << endl;
    } else {
        cout << original << " is not a palindrome number." << endl;
    }

    return 0;
}
```

---

### 🔎 Sample Output

```
Enter an integer: 12321
12321 is a palindrome number.
```

```
Enter an integer: 12345
12345 is not a palindrome number.
```

---

Let me know if you want a version that checks **palindrome strings**, works with **negative numbers**, or uses **recursion**!
