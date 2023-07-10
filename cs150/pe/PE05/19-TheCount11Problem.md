// Given a string, compute recursively (no loops) the number of "11" substrings in the string. The "11" substrings should not overlap.

// * count11("11abc11") → 2
// * count11("abc11x11x11") → 3
// * count11("111") → 1

```cpp
#include <string>
using std::string;
int count11(const string& str)
{
   return 0; // replace this with your code
}
```

// https://codecheck.io/files/2303022259y48v91mg1n3ifkcl787765kq

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|count11|"11abc11"|2|2|
|pass|count11|"abc11x11x11"|3|3|
|pass|count11|"111"|1|1|