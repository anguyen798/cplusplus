// Write a program to calculate the surface area of a regular polygon, one
where all sides have the same length, like those in the picture to the
right. To calculate the surface area you need the number of sides (n)
and the length of any side (s). The formula you'll use is:
// $$A = \frac{s^{2}n}{4\tan\frac{\pi}{n}}$$

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
    const string assignment = "Polygon Area Calculator";

    cout << LAST_NAME << ", " << FIRST_NAME << ": " << assignment << endl;
    cout << "\"'\"'\"'\"'\"'\"'\"'\"'\"'\"'\"'\"'\"'\"'\"'\"'\"'\"'\"'\"'\"'\"'\"" << endl;
    cout << endl;

    int numSides;
    double sideLength;

    cout << "Enter the number of sides of the polygon: ";
    cin >> numSides;

    cout << "Enter the length of any side of the polygon: ";
    cin >> sideLength;

    double area = (pow(sideLength, 2) * numSides) / (4 * tan(pi / numSides));

    cout << "Polygon Area: [" << area << "]" << endl;

////////////////// PUT ONLY YOUR CODE ABOVE //////////////////////
    return 0;
}

```

// https://codecheck.io/files/23052320492sjmzpf9i5ffq1xqacpkb4egt