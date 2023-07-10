// Given a non-negative int n, compute recursively (no loops) the count of the occurrences of 8 as a digit, except that an 8 with another 8 immediately to its left counts double, so 8818 yields 4.

// Note that mod (%) by 10 yields the rightmost digit (126 % 10 is 6), while divide (/) by 10 removes the rightmost digit (126 / 10 is 12).

// * count8(8) → 1
// * count8(818) → 2
// * count8(8818) → 4

```cpp
#include <string>
using std::string;
int count8(int n)
{
   return 0; // replace this with your code
}
```

// https://codecheck.io/files/230303240019ezt4sqwhjmkvfgnk1u13ry6

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|count8|8|1|1|
|pass|count8|818|2|2|
|pass|count8|8818|4|4|