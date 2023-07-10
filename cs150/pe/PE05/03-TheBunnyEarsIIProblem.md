// We have bunnies standing in a line, numbered 1, 2, ... The odd bunnies (1, 3, ..) have the normal 2 ears. The even bunnies (2, 4, ..) we'll say have 3 ears, because they each have a raised foot.

// Recursively return the number of "ears" in the bunny line 1, 2, ... n (without loops or multiplication).

// * bunnyEars2(0) → 0
// * bunnyEars2(1) → 2
// * bunnyEars2(2) → 5

```cpp
#include <string>
using std::string;
int bunnyEars2(int n)
{
   return 0; // replace this with your code
}
```

// https://codecheck.io/files/2303032419eqxdxefba0l5mcbztjrcz77n7

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|bunnyEars2|0|0|0|
|pass|bunnyEars2|1|2|2|
|pass|bunnyEars2|2|5|5|