// Given a string and a non-empty substring sub, compute recursively the largest substring which starts and ends with sub and return its length.

// * strDist("catcowcat", "cat") → 9
// * strDist("catcowcat", "cow") → 3
// * strDist("cccatcowcatxx", "cat") → 9

```cpp
#include <string>
using std::string;
int strDist(const string& str, const string& sub)
{
   return 0; // replace this with your code
}
```

// https://codecheck.io/files/23030221557sc2cak7f5zze7dot4zbwix54

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|strDist|"catcowcat", "cat"|9|9|
|pass|strDist|"catcowcat", "cow"|3|3|
|pass|strDist|"cccatcowcatxx", "cat"|9|9|