// Write a program to calculate the distance between two points (x1,
y1) and (x2, y2) and displays the distance. The formula for
calculating the distance between two points is:
// $$D = \sqrt{(x_{2}-x_{1})^{2} + (y_{2}-y_{1})^{2}}$$
```cpp
#include <iostream>
#include <cmath>
#include <iomanip>
#include <string>
using namespace std;

int main()
{
////////////////// PUT ONLY YOUR CODE BELOW //////////////////////
    // Add your code here

    const double pi = acos(-1.0);
    const string FIRST_NAME = "First";
    const string LAST_NAME = "Last";
    const string assignment = "Distance Calculator";

    cout << LAST_NAME << ", " << FIRST_NAME << ": " << assignment << endl;
    cout << "\"\\\"\\\"\\\"\\\"\\\"\\\"\\\"\\\"\\\"\\\"\\\"\\\"\\\"\\\"" << endl;
    cout << endl;

    double x1, y1, x2, y2;

    cout << "Enter the coordinates of the first point (x1, y1): ";
    cin >> x1 >> y1;

    cout << "Enter the coordinates of the second point (x2, y2): ";
    cin >> x2 >> y2;

    double distance = sqrt(pow(x2 - x1, 2) + pow(y2 - y1, 2));

    cout << "Distance: [" << distance << "]" << endl;

////////////////// PUT ONLY YOUR CODE ABOVE //////////////////////
    return 0;
}

```

// https://codecheck.io/files/2305232059cm5elfidllcj5p4pio5ho84l0