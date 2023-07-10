// Given a string, compute recursively a new string where identical chars that are adjacent in the original string are separated from each other by a "\*".

// * pairStar("hello") → "hel\*lo"
// * pairStar("xxyy") → "x\*xy\*y"
// * pairStar("aaaa") → "a\*a\*a\*a"

```cpp
#include <string>
using std::string;
string pairStar(const string& str)
{
   return ""; // replace this with your code
}
```

// https://codecheck.io/files/23030223185pjkpn88ibjwhi55rmkg3h9lm

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|pairStar|"hello"|"hel\*lo"|"hel\*lo"|
|pass|pairStar|"xxyy"|"x\*xy\*y"|"x\*xy\*y"|
|pass|pairStar|"aaaa"|"a\*a\*a\*a"|"a\*a\*a\*a"|