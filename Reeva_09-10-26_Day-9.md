## Approach
Start with sum = 0 and i = 1. Keep adding i to sum and increase i by 1. If sum becomes equal to n, print YES. If it exceeds n, print NO

## Code
```cpp
#include <bits/stdc++.h>
using namespace std;
 
int main() {
    int n, sum = 0;
 
    cin >> n;
 
    for (int i = 1; sum < n; i++) {
        sum += i;
    }
 
    if (sum == n)
        cout << "YES";
    else
        cout << "NO";
 
    return 0;
}
```
Complexity:

Time Complexity: O(√n)

Space Complexity: O(1)

<img width="1788" height="522" alt="image" src="https://github.com/user-attachments/assets/c60d7cde-354c-4709-a862-70272ce77040" />
