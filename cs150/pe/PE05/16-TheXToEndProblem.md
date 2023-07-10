// Given a string, compute recursively a new string where all the lowercase 'x' chars have been moved to the end of the string.

// * endX("xxre") → "rexx"
// * endX("xxhixx") → "hixxxx"
// * endX("xhixhix") → "hihixxx"

```cpp
#include <string>
using std::string;
string endX(const string& str)
{
   return ""; // replace this with your code
}
```

// https://codecheck.io/files/2303022312mp4bni0v6pev4kg0xke2b91

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|endX|"xxre"|"rexx"|"rexx"|
|pass|endX|"xxhixx"|"hixxxx"|"hixxxx"|
|pass|endX|"xhixhix"|"hihixxx"|"hihixxx"|