// Write a function runningSum that accepts an input stream and an output stream as parameters. The input stream represents an input file holding a sequence of real numbers. The function outputs the running sum of the numbers followed by the maximum running sum. In other words, the nth number that you report should be the sum of the first n numbers in the input stream and the maximum that you report should be the largest such value that you report. For example if the input stream contains the following data:
// 3.25 4.5 -8.25 7.25 3.5 4.25 -6.5 5.25

// your function should produce the following output:
// running sum = 3.25 7.75 -0.5 6.75 10.25 14.5 8.0 13.25
// max sum = 14.5

// The first number reported is the same as the first number in the input stream (3.25). The second number reported is the sum of the first two numbers in the input stream (3.25 + 4.5). The third number reported is the sum of the first three numbers in the input stream (3.25 + 4.5 + -8.25). And so on. The maximum of these values is 14.5, which is reported on the second line of output. You may assume that there is at least one number to read.

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

void runningSum(istream& in, ostream& out)
{
   double num, sum {0}, maxSum {0};

   out << "running sum = ";
   while (in >> num)
   {
      sum += num;
      out << sum << ' ';
      if (sum > maxSum) { maxSum = sum; }
   }
   out << "\nmax sum = " << maxSum << '\n';
}

// Above here
int main()
{
    istringstream in("3.25 4.5 -8.25 7.25 3.5 4.25 -6.5 5.25");
    runningSum(in, cout);
}
```

/*
```text
Running runningSum.cpp

running sum = 3.25 7.75 -0.5 6.75 10.25 14.5 8 13.25 
max sum = 14.5

pass

Score

1/1
```
\*/

// https://codecheck.io/files/23041119146qdqh8g2t9d6dikzp5d2p3irq