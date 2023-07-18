// Write a function countWords that accepts an input stream and an output stream as arguments. The function outputs the total number of lines and words found in the input as well as the average number of words per line. For example, consider the following input:

/*
```text
// You must show: your Student ID card
// to 1) a TA or 2) the instructor
// before
// leaving the room.
```
\*/

// For the purposes of this problem, we will use whitespace to separate words. That means that some words might include punctuation, as in "show:" and "1)". (This is the same definition that the input stream uses for tokens.) For the input above, your function should produce the following output:

/*
```text
// Total lines = 6
// Total words = 19
// Average words per line = 3.167
```
\*/

// The format of your output must exactly match that shown above, including rounding the words per line to 3 decimal places. Notice that some input lines can be blank. Do not worry about rounding the average words per line. You may assume that the input stream contains at least 1 line of input.

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

void countWords(..., ...)
{
  . . .
}

// Above here
int main()
{
    istringstream in("You must show: your Student ID card\n"
                    "\n"
                    "to 1) a TA or 2) the instructor \n"
                    "before\n"
                    "\n"
                    "leaving the room. \n"
    );
    countWords(in, cout);
}

```

/*
```text
Running countWords.cpp

Total lines = 6
Total words = 19
Average words per line = 3.167

pass

Score

1/1
```
\*/

// https://codecheck.io/files/2304111835d70nzukmgd00j1pbmhckyua1o