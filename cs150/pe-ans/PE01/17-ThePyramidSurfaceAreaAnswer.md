// Write a program to calculate the total surface area (A) of a square pyramid
as shown here. Here is the formula:
// $$A = a(A + \sqrt{a^{2} + 4h^{2}})$$
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
    const string assignment = "Pyramid Surface Area";

    cout << LAST_NAME << ", " << FIRST_NAME << ": " << assignment << endl;
    cout << string(50, '-') << endl;
    cout << endl;

    double a, h;

    cout << "Enter the length of the base side (a): ";
    cin >> a;
    cout << "Enter the height of the pyramid (h): ";
    cin >> h;

    double surfaceArea = a * (a + sqrt(a * a + 4 * h * h));

    cout << "Surface Area: [" << surfaceArea << "]" << endl;

////////////////// PUT ONLY YOUR CODE ABOVE //////////////////////
    return 0;
}    
```

// https://replit.com