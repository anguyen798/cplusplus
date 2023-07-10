// Given a string, compute recursively a new string where all the adjacent chars are now separated by a "\*".

// * allStar("hello") → "h\*e\*l\*l\*o"
// * allStar("abc") → "a\*b\*c"
// * allStar("ab") → "a\*b"

```cpp
#include <string>
using std::string;
string allStar(const string& str)
{
   return ""; // replace this with your code
}
```

// https://codecheck.io/files/2303022322ebbm9nq136v4vb5h40yrq6he9

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|allStar|"hello"|"h\*e\*l\*l\*o"|"h\*e\*l\*l\*o"|
|pass|allStar|"abc"|"a\*b\*c"|"a\*b\*c"|
|pass|allStar|"ab"|"a\*b"|"a\*b"|