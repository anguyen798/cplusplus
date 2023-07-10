// Given a string, compute recursively (no loops) a new string where all appearances of "pi" have been replaced by "3.14".

// * changePi("xpix") → "x3.14x"
// * changePi("pipi") → "3.143.14"
// * changePi("pip") → "3.14p"

```cpp
#include <string>
using std::string;
string changePi(const string& str)
{
   return ""; // replace this with your code
}
```


// https://codecheck.io/files/23030223304plcu8b16kwuz354xl69h8hmp

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|changePi|"xpix"|"x3.14x"|"x3.14x"|
|pass|changePi|"pipi"|"3.143.14"|"3.143.14"|
|pass|changePi|"pip"|"3.14p"|"3.14p"|