// Given a string and a non-empty substring sub, compute recursively if at least n copies of sub appear in the string somewhere, possibly with overlapping. N will be non-negative.

// * strCopies("catcowcat", "cat", 2) → true
// * strCopies("catcowcat", "cow", 2) → false
// * strCopies("catcowcat", "cow", 1) → true

```cpp
#include <string>
using std::string;
bool strCopies(const string& str, const string& sub, int n)
{
   return false; // replace this with your code
}
```

// https://codecheck.io/files/23030222169incbam0sd6cd1724qtp3kd37

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|strCopies|"catcowcat", "cat", 2|true|true|
|pass|strCopies|"catcowcat", "cow", 2|false|false|
|pass|strCopies|"catcowcat", "cow", 1|true|true|