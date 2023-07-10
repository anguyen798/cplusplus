// Given a string, compute recursively (no loops) a new string where all the lowercase 'x' chars have been changed to 'y' chars.

// * changeXY("codex") → "codey"
// * changeXY("xxhixx") → "yyhiyy"
// * changeXY("xhixhix") → "yhiyhiy"

```cpp
#include <string>
using std::string;
string changeXY(const string& str)
{
   return ""; // replace this with your code
}
```

// https://codecheck.io/files/23030223347ikqoqk2e63qk8avk758nfjny

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|changeXY|"codex"|"codey"|"codey"|
|pass|changeXY|"xxhixx"|"yyhiyy"|"yyhiyy"|
|pass|changeXY|"xhixhix"|"yhiyhiy"|"yhiyhiy"|