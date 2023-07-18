// Write a function evenStats that accepts an input stream and an output stream as arguments. The input stream represents a series of integers; you may assume that there is at least one integer in the input. Report the total number of numbers, the sum of the numbers, the count of even numbers and the percent of even numbers. For example, if an input stream contains the following text:
// 5 7 2 8 9 10 12 98 7 14 20 22

// Then the function should produce the following output:
// 12 numbers, sum = 214
// 8 evens (66.67%)

```cpp
#include <iostream>
#include <fstream>
#include <sstream>
#include <iomanip>
#include <string>
#include <vector>
#include <cmath>
using namespace std;
// Below here

void evenStats(..., ...)
{
  . . .
}

// Above here
int main()
{
    istringstream in("5 7 2 8 9 10 12 98 7 14 20 22");
    evenStats(in, cout);
}
```

/*
```text
Running evenStats.cpp

12 numbers, sum = 214
8 evens (66.67%)

pass

Score

1/1
```
\*/

// https://codecheck.io/files/2304111357tvx5oe3bz1thu0egolitertf