// Given a string and a non-empty substring sub, compute recursively the number of times that sub appears in the string, without the sub strings overlapping.

// * strCount("catcowcat", "cat") → 2
// * strCount("catcowcat", "cow") → 1
// * strCount("catcowcat", "dog") → 0

```cpp
#include <string>
using std::string;
int strCount(const string& str, const string& sub)
{
   return 0; // replace this with your code
}
```

// https://codecheck.io/files/2303022223cnfut8un1giatlbfh2xt2gby0

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|strCount|"catcowcat", "cat"|2|2|
|pass|strCount|"catcowcat", "cow"|1|1|
|pass|strCount|"catcowcat", "dog"|0|0|