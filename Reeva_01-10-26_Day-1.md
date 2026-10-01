## Approach

We scan the entire grid and keep track of four boundaries:

- minRow → topmost *
- maxRow → bottommost *
- minCol → leftmost *
- maxCol → rightmost *

Whenever we find a *, we update these four values using min() and max().

After scanning the whole grid, we print all cells from minRow to maxRow and minCol to maxCol.

## Code
```cpp
#include <bits/stdc++.h>

using namespace std;
 
int main() {
 
    int n, m;
    cin >> n >> m;
 
    vector<string> a(n);
 
    for (int i = 0; i < n; i++) {
        cin >> a[i];
    }
 
    int minRow = n;
    int maxRow = -1;
    int minCol = m;
    int maxCol = -1;
 
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < m; j++) {
 
            if (a[i][j] == '*') {
 
                minRow = min(minRow, i);
                maxRow = max(maxRow, i);
 
                minCol = min(minCol, j);
                maxCol = max(maxCol, j);
            }
        }
    }
 
    for (int i = minRow; i <= maxRow; i++) {
 
        for (int j = minCol; j <= maxCol; j++) {
            cout << a[i][j];
        }
 
        cout << '\n';
    }
 
    return 0;

}
```
Complexity:

Time: O(n × m)

Space: O(n × m) for storing the grid.

<img width="1807" height="222" alt="image" src="https://github.com/user-attachments/assets/6a11a18e-a445-4d45-a761-453fc986de3e" />
