// Write a program to calculate the surface area of a cylinder; you'll need
the area of the top, plus the area of the bottom, plus the area around the
cylinder (the lateral surface area). The formula for calculating the total
surface area of a cylinder (A) with radius (R) and height (H) is:
// $$A = 2 \pi R^{2} + 2 \pi R H$$
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

////////////////// PUT ONLY YOUR CODE ABOVE //////////////////////
    return 0;
}    
```

// https://codecheck.io/files/2305232037ejfro25re3p6xj4dbajps26da