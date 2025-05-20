
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

