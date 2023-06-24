```cpp
#include <iostream>
#include <string>
#include <cctype>
using namespace std;

void title() {
    const string LAST_NAME = "Last";
    const string FIRST_NAME = "First";
    const string ASSIGNMENT = "The Fizz Buzz Too Problem";

    cout << LAST_NAME << ", "<< FIRST_NAME << ": ";
    cout << ASSIGNMENT << endl;
    cout << "\n";
    cout << string (50, '-');
    cout << "\n";
}

string fizzBuzzToo(string str) {
    bool startWithF = tolower(str[0]) == 'f';
    bool endWithB = tolower(str[str.length()-1]) == 'b';

    if (startWithF && endWithB)
        return "FizzBuzz";
    else if (startWithF)
        return "Fizz";
    else if (endWithB)
        return "Buzz";
    else
        return str + "!";
}

int main() {
    title();

    string str;
    cout << "Enter a string:" << endl;
    cin >> str;

    string result = fizzBuzzToo(str);
    cout << "The result is: \"" << result << "\"" << endl;

    return 0;
}

```