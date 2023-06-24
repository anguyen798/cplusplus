```cpp
#include <iostream>
#include <string>
using namespace std;

void title() {
    const string LAST_NAME = "Last";
    const string FIRST_NAME = "First";
    const string ASSIGNMENT = "The No Doubles Problem";

    cout << LAST_NAME << ", "<< FIRST_NAME << ": ";
    cout << ASSIGNMENT << endl;
    cout << "\n";
    cout << string (50, '-');
    cout << "\n";
}

int noDoubles(int die1, int die2, bool has_doubles) {
    if (has_doubles && die1 == die2) {
        die1 = die1 % 6 + 1; // increment die1, wrap to 1 if it was 6
    }
    return die1 + die2;
}

int main() {
    title();

    int die1, die2;
    bool has_doubles;
    cout << "Enter two dice rolls (1-6) and a boolean for doubles (0 or 1):" << endl;
    cin >> die1 >> die2 >> has_doubles;

    int result = noDoubles(die1, die2, has_doubles);
    cout << "The result is: " << result << endl;

    return 0;
}

```