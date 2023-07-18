// Write a function printStrings that takes an input stream and an output stream as arguments.
// The input stream contains a sequence of integer/string pairs and that prints to the output stream one line of output for each pair with the given string repeated the given number of times. For example if the input contains the following data:

// 6 fun. 3 hello 10 <> 2 25 4 wow!

// your function should produce the following output:

/*
```text
// fun.fun.fun.fun.fun.fun.
// hellohellohello
// <><><><><><><><><><>
// 2525
// wow!wow!wow!wow!
```
\*/

// Notice that there is one line of output for each integer/string pair. The first line has 6 occurrences of "fun.", the second line has 3 occurrences of "hello", the third line has 10 occurrences of "<>", the fourth line has 2 occurrences of "25" the fifth line has 4 occurrences of "wow!". Notice that there are no extra spaces included in the output. You are to exactly reproduce the format of this sample output. You may assume that the input values always come in pairs with an integer followed by a String (which itself could be numeric, such as "25" above). If the input stream is empty (no integer/string pairs), your function should produce no output.

```cpp
#include <iostream>
#include <fstream>
#include <sstream>
#include <iomanip>
#include <string>
#include <vector>
#include <cmath>
#include <cctype>
using namespace std;
// Below here

void printStrings(..., ...)
{
  . . .
}

// Above here
int main()
{
    istringstream in("6 fun. 3 hello  10   <> 2      25   4 wow!");
    printStrings(in, cout);
}

```

/*
```text
Running printStrings.cpp

fun.fun.fun.fun.fun.fun.
hellohellohello
<><><><><><><><><><>
2525
wow!wow!wow!wow!

pass

Score

1/1
```
\*/

// https://codecheck.io/files/230411172489tlr8tzrfgfyj4my77tf2xl2