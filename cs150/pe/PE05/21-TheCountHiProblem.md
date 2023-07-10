// Given a string, compute recursively the number of times lowercase "hi" appears in the string, however do not count "hi" that have an 'x' immediately before them.

// * countHi2("ahixhi") → 1
// * countHi2("ahibhi") → 2
// * countHi2("xhixhi") → 0

```cpp
#include <string>
using std::string;
int countHi2(const string& str)
{
   return 0; // replace this with your code
}
```

// https://codecheck.io/files/23030222432lf5bkby08sd36vk4mxinpttd

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|countHi2|"ahixhi"|1|1|
|pass|countHi2|"ahibhi"|2|2|
|pass|countHi2|"xhixhi"|0|0|