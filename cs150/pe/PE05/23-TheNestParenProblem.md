// Given a string, return true if it is a nesting of zero or more pairs of parenthesis, like "(())" or "((()))". Suggestion: check the first and last chars, and then recur on what's inside them.

// * nestParen("(())") → true
// * nestParen("((()))") → true
// * nestParen("(((x))") → false

```cpp
#include <string>
using std::string;
bool nestParen(const string& str)
{
   return false; // replace this with your code
}
```

// https://codecheck.io/files/2303022229xgmiui3ki3d1rf0cei6s5ekr

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|nestParen|"(())"|true|true|
|pass|nestParen|"((()))"|true|true|
|pass|nestParen|"(((x))"|false|false|