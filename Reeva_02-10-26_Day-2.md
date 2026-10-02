## Approach

We scan the flag row by row. For each row, we check that all its cells have the same colour and that its colour is different from the previous row. If any condition fails, we print NO; otherwise, we print YES.

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

    for (int i = 0; i < n; i++) {

        // Check if all cells in the row have the same colour
        for (int j = 1; j < m; j++) {
            if (a[i][j] != a[i][0]) {
                cout << "NO";
                return 0;
            }
        }

        // Check if adjacent rows have different colours
        if (i > 0 && a[i][0] == a[i - 1][0]) {
            cout << "NO";
            return 0;
        }
    }

    cout << "YES";

    return 0;
}
```

Complexity:

Time:O(n × m)

Space:O(n × m) for storing the grid.

<img width="1836" height="223" alt="image" src="https://github.com/user-attachments/assets/55ba7d84-dc3f-49cc-8b12-bfb8d06412f5" />
