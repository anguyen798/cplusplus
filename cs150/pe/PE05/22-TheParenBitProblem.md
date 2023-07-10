// Given a string that contains a single pair of parenthesis, compute recursively a new string made of only of the parenthesis and their contents, so "xyz(abc)123" yields "(abc)".

// * parenBit("xyz(abc)123") → "(abc)"
// * parenBit("x(hello)") → "(hello)"
// * parenBit("(xy)1") → "(xy)"

```cpp
#include <string>
using std::string;
string parenBit(const string& str)
{
   return ""; // replace this with your code
}
```

// https://codecheck.io/files/2303022237egyekqtask1iqvz76l92atadm

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|parenBit|"xyz(abc)123"|"(abc)"|"(abc)"|
|pass|parenBit|"x(hello)"|"(hello)"|"(hello)"|
|pass|parenBit|"(xy)1"|"(xy)"|"(xy)"|