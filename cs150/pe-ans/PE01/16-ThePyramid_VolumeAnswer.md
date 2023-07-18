// Write a program to calculate the volume (V) of a square pyramid as shown
here. Here is the formula:
// $$V = \frac{1}{3} a^{2} h$$
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
    const string assignment = "Pyramid Volume";

    cout << LAST_NAME << ", " << FIRST_NAME << ": " << assignment << endl;
    cout << string(50, '-') << endl;
    cout << endl;

    double a, h;

    cout << "Enter the length of the base side (a): ";
    cin >> a;
    cout << "Enter the height of the pyramid (h): ";
    cin >> h;

    double volume = (1.0 / 3.0) * a * a * h;

    cout << "Volume: [" << volume << "]" << endl;

////////////////// PUT ONLY YOUR CODE ABOVE //////////////////////
    return 0;
}    
```

// https://replit.com