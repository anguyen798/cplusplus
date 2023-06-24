```cpp
#include <iostream>
#include <string>
using namespace std;

void title() {
    const string LAST_NAME = "Last";
    const string FIRST_NAME = "First";
    const string ASSIGNMENT = "Mod Max Five Problem";

    cout << LAST_NAME << ", "<< FIRST_NAME << ": ";
    cout << ASSIGNMENT << endl;
    cout << "\n";
    cout << string (50, '-');
    cout << "\n";
}

int modMaxFive(int a, int b) {
    if (a == b)
        return 0;
    else if (a % 5 == b % 5)
        return a < b ? a : b;
    else
        return a > b ? a : b;
}

int main() {
    title();

    int a, b;
    cout << "Enter two integers:" << endl;
    cin >> a >> b;

    int result = modMaxFive(a, b);
    cout << "The result is: " << result << endl;

    return 0;
}

```