// Write a function wordStats that accepts an input stream and an output stream as arguments. The input stream contains a sequence of words. Report the total number of words (as an integer) and the average word length (as an un-rounded real number). You may assume that the input stream isn't empty. For example, suppose the input stream contains the following:

// To be or not to be, that is the question.

// We will use whitespace to separate words. That means that some words include punctuation, as in "be,". (This is the same definition that the input stream uses for tokens.) For the input above, your function should produce exactly the following output:

// Total words = 10
// Average length = 3.2

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

void wordStats(..., ...)
{
  . . .
}

// Above here
int main()
{
    istringstream in("To be or not to be, that is the question.");
    wordStats(in, cout);
}
```

/*
```text
Running wordStats.cpp

Total words = 10
Average length = 3.2

pass

Score

1/1
```
\*/

// https://codecheck.io/files/23041117515sj5jmc1q38uh3sbec66o4jaf