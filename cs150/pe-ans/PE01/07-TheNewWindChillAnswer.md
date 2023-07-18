// Write a program to calculate the "wind-chill" or "feels-like" temperature (T) given the wind speed (v) in miles per hour and the temperature (t) in Fahrenheit. Your program should use the "new" wind-chill formula adopted in 2001 by the National Weather Service:

// $$T = 35.74 + 0.6215t - 35.75v^{0.16} + 0.4275t v^{0.16}$$
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
    const string assignment = "Wind Chill Calculator";

    cout << LAST_NAME << ", " << FIRST_NAME << ": " << assignment << endl;
    cout << "///\"/\"///\"/\"///\"/\"///\"/\"//\\//\"" << endl;
    cout << endl;

    double v, t;

    cout << "Enter the wind speed (in miles per hour): ";
    cin >> v;

    cout << "Enter the temperature (in Fahrenheit): ";
    cin >> t;

    double windChill = 35.74 + 0.6215 * t - 35.75 * pow(v, 0.16) + 0.4275 * t * pow(v, 0.16);

    cout << "Wind Chill: [" << windChill << "]" << endl;

////////////////// PUT ONLY YOUR CODE ABOVE //////////////////////
    return 0;
}

```

// https://codecheck.io/files/2305232103a5jwevmm2q1wk8pz3dwqjyor2