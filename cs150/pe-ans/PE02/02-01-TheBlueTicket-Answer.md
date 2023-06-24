```cpp
#include <iostream>
#include <string>

using namespace std;

void title()
{
    const string LAST_NAME = "Last";
    const string FIRST_NAME = "First";
    const string ASSIGNMENT = "Blue Ticket Problem";

    cout << LAST_NAME << ", " << FIRST_NAME << ": ";
    cout << ASSIGNMENT << endl;
    cout << "\n";
    cout << string(50, '-') << endl;
    cout << "\n";
}

int blueTicket(int a, int b, int c)
{
    int ab = a + b;
    int bc = b + c;
    int ac = a + c;

    if (ab == 10 || bc == 10 || ac == 10)
        return 10;
    else if (ab - bc == 10 || ab - ac == 10)
        return 5;
    else
        return 0;
}

int main()
{
    title();

    int a, b, c;
    cout << "Enter values for a, b, and c: ";
    cin >> a >> b >> c;

    int result = blueTicket(a, b, c);
    cout << "Result: " << result << endl;

    return 0;
}

```