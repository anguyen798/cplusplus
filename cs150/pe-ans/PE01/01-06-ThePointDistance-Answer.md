
```cpp
#include <iostream>
#include <cmath>
#include <string>

int main() {
    using namespace std;

    const double pi = acos(-1.0);
    const string STUDENT = "anguyen798";
    const string assignment = "Distance Calculator";

    cout << STUDENT << ": ";
    cout << assignment << endl;
    cout << "\"\\\"\\\"\\\"\\\"\\\"\\\"\\\"\\\"\\\"\\\"\\\"\\\"\\\"\\\"" << endl;
    cout << endl;

    double x1, y1, x2, y2;

    cout << "Enter the coordinates of the first point (x1, y1): ";
    cin >> x1 >> y1;

    cout << "Enter the coordinates of the second point (x2, y2): ";
    cin >> x2 >> y2;

    double distance = sqrt(pow(x2 - x1, 2) + pow(y2 - y1, 2));

    cout << "Distance: [" << distance << "]" << endl;

    return 0;
}

```