```cpp
#include <iostream>
#include <cmath>
#include <iomanip>
#include <string>
using namespace std;


int main() {
////////////////// PUT ONLY YOUR CODE BELOW //////////////////////
    double radius, height;
    const double pi = acos(-1.0);
    const string FIRST_NAME = "First";
    const string LAST_NAME = "Last";
    const string ASSIGNMENT = "Cone Volume Calculator";

    cout << LAST_NAME << ", " << FIRST_NAME << ": " << assignment << endl;
	\\ Sequences before: \"/\"/\"/\"/\"/\"/\"/\"/\"/\"/\"/\"/\"/\ 
    cout << "\\\"/\\\"/\\\"/\\\"/\\\"/\\\"/\\\"/\\\"/\\\"/\\\"/\\\"/\\\"/\\\"/\\" << endl;
    cout << endl;

    cout << "Enter the radius of the cylinder: ";
    cin >> radius;
    cout << "Enter the height of the cylinder: ";
    cin >> height;
    double topArea = pi * pow(radius, 2);
    double lateralArea = 2 * pi * radius * height;
    double totalArea = 2 * topArea + lateralArea;
    
    cout << endl;

    cout << "Surface Area: [" << totalArea << "]" << endl;

    return 0;
}

```