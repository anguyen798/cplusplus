// Write a function mostUnique that accepts an input stream and an output stream as arguments.
// The input stream contains integer quiz scores separated by spaces. Each class period is on its own line and contains a different number of students. Your function should return the highest number of unique scores given in a single class period. The function should also output information about the unique scores given in each period, in a format described below.
// On a given line, all occurrences of any particular number value will occur consecutively in the input. For example, if there is a sequence of occurrences of the number 8, there will not be any other occurrences of the number 8 on that same line outside of that sequence.
// Given an input stream that contains the following text:

/*
```text
// 10 10 10 9 9 8 3
// 3 3 8 10 9 7 7 6 6
// 4 1 9 9 10 7 7
// 10 10 10 10
```
\*/

// The function should return 6 and generate the following output:
/*
```text
// Period 1: 4 unique scores
// Period 2: 6 unique scores
// Period 3: 5 unique scores
// Period 4: 1 unique scores
```
\*/

// On the first line, there are 4 unique scores: 10, 9, 8 and 3. The second line contains 6 unique scores: 3, 8, 10, 9, 7 and 6. The third line contains 5 unique scores: 4, 1, 9, 10 and 7. The fourth line only has one unique score: 10. The value returned is 6 because it is the highest number of unique scores given in a class period.
// Assume that the input contains at least one line of data and that each line contains at least one score.

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

int mostUnique(..., ...)
{
  . . .
}

// Above here
int main()
{
    istringstream in("10 10 10  9 9   8    3\n"
                    "3 3 8 10 9 7   7 6 6\n"
                    "4  1 9  9 10  7 7 \n"
                    "10  10   10 10\n"
                    );
    int result = mostUnique(in, cout);
    cout << "result=" << result << endl;
}
```

/*
```text
Running mostUnique.cpp

Period 1: 4 unique scores
Period 2: 6 unique scores
Period 3: 5 unique scores
Period 4: 1 unique scores
result=6

pass

Score

1/1
```
\*/

// https://codecheck.io/files/230411174571cwqe8h8vbwx9045tz5rxhsm