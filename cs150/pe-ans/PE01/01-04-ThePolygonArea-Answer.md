```cpp
#include <iostream>
#include <cmath>
#include <string>

int main() {
    using namespace std;

    const double pi = acos(-1.0);
    const string STUDENT = "anguyen798";
    const string assignment = "Polygon Area Calculator";

    cout << STUDENT << ": ";
    cout << assignment << endl;

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

    return 0;
}

```