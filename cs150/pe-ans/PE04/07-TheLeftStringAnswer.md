// Write a function strToLeet() that accepts an input-output string parameter and converts the string to (or from) "leet speak" (aka 1337 speak), an internet dialect where various letters are replaced by other letters/numbers. Return the original string.

// | Original character | 'Leet' character |
// | o                            | 0                       |
// | l  (lowercase L)      | 1                       |
// | e                            | 3                       |
// | a                            | 4                       |
// | t                             | 7                       |
// | s (end of word)      | z                       |

// Here are some examples:
// string str = "four score and";
// cout << strToLeet(str) << endl; // four score and (unchanged)
// cout << str << endl; // f0ur sc0r3 4nd (changed)

```cpp
string strToLeet(string &str) {
    string original {str};
    for (int i {0}, len {str.size()}; i < len; ++i) {
        char c = str.at(i);
        switch (c)
        {
            case 'o':
                str.at(i) = '0';
                break;
            case 'l':
                str.at(i) = '1';
                break;
            case 'e':
                str.at(i) = '3';
                break;
            case 'a':
                str.at(i) = '4';
                break;
            case 't':
                str.at(i) = '7';
                break;
            case 's':
                if (i + 1 == str.size() || str.at(i + 1) == ' ') {
                    str.at(i) = 'Z';
                }
                break;
        }
    }
    return original;
}
```

// https://codecheck.io/files/2303031916c2vc01koo0b0hscyop99jji0g