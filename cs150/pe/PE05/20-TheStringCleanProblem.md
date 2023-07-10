// Given a string, return recursively a "cleaned" string where adjacent chars that are the same have been reduced to a single char. So "yyzzza" yields "yza".

// * stringClean("yyzzza") → "yza"
// * stringClean("abbbcdd") → "abcd"
// * stringClean("Hello") → "Helo"

```cpp
#include <string>
using std::string;
string stringClean(const string& str)
{
   return ""; // replace this with your code
}
```

// https://codecheck.io/files/230302225587s2mghg7hwvn5606zgimtxvd

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|stringClean|"yyzzza"|"yza"|"yza"|
|pass|stringClean|"abbbcdd"|"abcd"|"abcd"|
|pass|stringClean|"Hello"|"Helo"|"Helo"|