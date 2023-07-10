// We'll say that a "pair" in a string is two instances of a char separated by a char. So "AxA" the A's make a pair. Pair's can overlap, so "AxAxA" contains 3 pairs -- 2 for A and 1 for x.

// Recursively compute the number of pairs in the given string.

// countPairs("axa") → 1
// countPairs("axax") → 2
// countPairs("axbx") → 1"

```cpp
#include <string>
using std::string;
int countPairs(const string& str)
{
   return 0; // replace this with your code
}
```

// https://codecheck.io/files/2303022308at4et36go59ohdbllmk8qcirb

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|countPairs|"axa"|1|1|
|pass|countPairs|"axax"|2|2|
|pass|countPairs|"axbx"|1|1|