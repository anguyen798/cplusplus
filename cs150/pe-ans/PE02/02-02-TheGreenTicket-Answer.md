```cpp
#include <iostream>
#include <string>
using namespace std;

void title() {
    const string LAST_NAME = "Last";
    const string FIRST_NAME = "First";
    const string ASSIGNMENT = "Green Ticket Problem";

    cout << LAST_NAME << ", "<< FIRST_NAME << ": ";
    cout << ASSIGNMENT << endl;
    cout << "\n";
    cout << string (50, '-');
    cout << "\n";
}

int greenTicket(int a, int b, int c) {
    if (a == b && b == c)
        return 20;
    else if (a == b || b == c || a == c)
        return 10;
    else
        return 0;
}

int main() {
    title();

    int a, b, c;
    cout << "Enter three integers for the green lottery ticket:" << endl;
    cin >> a >> b >> c;

    int result = greenTicket(a, b, c);
    cout << "The result is: " << result << endl;

    return 0;
}

```