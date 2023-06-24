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

    double windChill = 0.0817 * (3.71 * sqrt(v) + 5.81 - 0.25 * v) * (t - 91.4) + 91.4;

    cout << "Wind Chill: [" << windChill << "]" << endl;

    return 0;
}

```