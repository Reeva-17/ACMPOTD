## Approach
Traverse the string from left to right. If the current character is ., print 0 and move one position ahead. If it is -, check the next character: -. represents 1 and -- represents 2. In both cases, move two positions ahead

## Code
```cpp
#include <bits/stdc++.h>
using namespace std;
 
int main() {
    string s;
    cin >> s;
 
    for (int i = 0; i < s.length(); ) {
        if (s[i] == '.') {
            cout << "0";
            i++;
        }
        else {
            if (s[i + 1] == '.') {
                cout << "1";
            } else {
                cout << "2";
            }
            i += 2;
        }
    }
 
    return 0;
}
```
Complexity:

Time Complexity: O(n)

Space Complexity: O(1)

<img width="1857" height="392" alt="image" src="https://github.com/user-attachments/assets/6b36ff4f-9356-4618-aa0b-33727dae4d0a" />
