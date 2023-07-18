// Write a program to calculate the volume of a right-circular code, like the
one pictured here. To calculate the volume (V) of a cone, given a radius
(R) and a height (H), the formula is:
// $$V = \frac{1}{3} \pi R^{2} H$$
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

    cout << "Enter the radius of the cone: ";
    cin >> radius;
    cout << "Enter the height of the cone: ";
    cin >> height;
    double volume = (1.0 / 3.0) * pi * pow(radius, 2) * height;
    
    cout << endl;

    cout << "Cone Volume [" << volume << "]" << endl;

////////////////// PUT ONLY YOUR CODE ABOVE //////////////////////
    return 0;
}
```

// https://codecheck.io/files/23052320003bb8iumm52y7hwr2zptfc5kh5