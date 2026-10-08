## Approach
Reverse the string s and compare it with t. If the reversed s is equal to t, print YES; otherwise, print NO.

## Code
```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    string s, t;
    cin >> s >> t;

    reverse(s.begin(), s.end());

    if (s == t)
        cout << "YES";
    else
        cout << "NO";

    return 0;
}
```
Complexity:

Time Complexity: O(n)

Space Complexity: O(n)

<img width="1788" height="481" alt="image" src="https://github.com/user-attachments/assets/c039d50f-c900-4897-9f9b-002fc186f571" />
