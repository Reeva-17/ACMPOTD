## Approach
Since soldiers are in a circle, each soldier has a neighbour on the right:Compare a[i] with a[i+1]
For the last soldier, compare a[n-1] with a[0]
Keep the pair with the minimum absolute difference

## Code
```cpp
#include <iostream>
#include <vector>
#include <cmath>
using namespace std;

int main() {
    int n;
    cin >> n;

    vector<int> a(n);
    for (int i = 0; i < n; i++)
        cin >> a[i];

    int minDiff = 1000000;
    int ans1 = 0, ans2 = 1;

    for (int i = 0; i < n; i++) {
        int j = (i + 1) % n;   // next soldier, circle-wise
        int diff = abs(a[i] - a[j]);

        if (diff < minDiff) {
            minDiff = diff;
            ans1 = i;
            ans2 = j;
        }
    }

    cout << ans1 + 1 << " " << ans2 + 1;

    return 0;
}
```
Complexity:

Time: O(n)

Space: O(n) because of the array.


<img width="1807" height="409" alt="image" src="https://github.com/user-attachments/assets/ef61d593-1bd4-458f-b7c8-095400c10e03" />
