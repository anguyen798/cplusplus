```cpp
#include <iostream>
#include <string>
using namespace std;

void title() {
    const string LAST_NAME = "Last";
    const string FIRST_NAME = "First";
    const string ASSIGNMENT = "Red Ticket Problem";

    cout << LAST_NAME << ", "<< FIRST_NAME << ": ";
    cout << ASSIGNMENT << endl;
    cout << "\n";
    cout << string (50, '-');
    cout << "\n";
}

int redTicket(int a, int b, int c) {
    if (a == 2 && b == 2 && c == 2)
        return 10;
    else if (a == b && b == c)
        return 5;
    else if (a != b && a != c)
        return 1;
    else
        return 0;
}

int main() {
    title();

    int a, b, c;
    cout << "Enter three integers (0, 1, or 2) for the red lottery ticket:" << endl;
    cin >> a >> b >> c;

    int result = redTicket(a, b, c);
    cout << "The result is: " << result << endl;

    return 0;
}

```