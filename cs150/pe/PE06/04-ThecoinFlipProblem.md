// Write a function coinFlip that accepts an input stream and an output stream as arguments. The input represents sets of coin flips that are either heads (H) or tails (T) in either upper or lower case, separated by at least one space. Consider each line to be a separate set of coin flips and output the number of heads and the percentage of heads in that line, rounded to the nearest tenth. If this percentage is more than 50%, you should out a "You win" message.

// For example, consider this input:

/* 
```text
// H T H H T
// T t t T h H
// h
```
\*/

// For the input above, your function should produce the following output:

/*
```text
// 3 heads (60.0%)
// You win!
// 2 heads (33.3%)
// 1 heads (100.0%)
// You win!
```

// The format of your output must exactly match that shown above. You may assume that the input stream contains at least 1 line of input, that each line contains at least one token, and that no tokens other than h, H, t, or T will be in the lines.

\*/

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
void coinFlip(..., ...)
{
  . . .
}
// Above here
int main()
{
    istringstream in("H T H H T\nT t   t T h  H\n   h");
    coinFlip(in, cout);
}
```

/*
```text
Running coinFlip.cpp

3 heads (60.0%)
You win!

2 heads (33.3%)

1 heads (100.0%)
You win!

pass

Score

1/1
```
\*/

// https://codecheck.io/files/23041020218azgw74cg81rmx710f4rhnaln