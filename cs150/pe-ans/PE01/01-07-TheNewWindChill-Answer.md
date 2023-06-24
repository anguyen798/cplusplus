```cpp
#include <iostream>
#include <cmath>
#include <string>

int main() {
    using namespace std;

    const double pi = acos(-1.0);
    const string STUDENT = "anguyen798";
    const string assignment = "Wind Chill Calculator";

    cout << STUDENT << ": ";
    cout << assignment << endl;
    cout << "///\"/\"///\"/\"///\"/\"///\"/\"//\\//\"" << endl;
    cout << endl;

    double v, t;

    cout << "Enter the wind speed (in miles per hour): ";
    cin >> v;

    cout << "Enter the temperature (in Fahrenheit): ";
    cin >> t;

    double windChill = 35.74 + 0.6215 * t - 35.75 * pow(v, 0.16) + 0.4275 * t * pow(v, 0.16);

    cout << "Wind Chill: [" << windChill << "]" << endl;

    return 0;
}

```