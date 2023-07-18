// Write a function negativeSum that accepts an input stream and an output stream as arguments, and returns a true/false value. The input stream contains a series of integers. Your function should determine whether the running sum, starting from the first number is ever negative. For example, if the input consists of the following:

// 38 4 19 -27 -15 -3 4 19 38
// The first number is 38 (not negative), the sum of the next (38 + 4), the sum of the next (38 + 4 + 19), and so on up to the sum of all of the numbers. None of these sums is negative, so the function would produce the following output and return false.
// no negative sum

// If the file instead contains the following numbers, the function finds that a negative sum of -8 is reached after adding 6 numbers together (14 + 7 + -10 + 9 + -18 + -10):
// 14 7 -10 9 -18 -10 17 42 98
// It should output the following, indicating that a negative sum can be reached, and return true.
// -8 after 6 steps

```cpp
#include <iostream>
#include <fstream>
#include <sstream>
#include <iomanip>
#include <string>
using namespace std;
// Below here

bool negativeSum(istream & in, ostream & out) {
   int number, sum {0}, steps {0};
   while (in >> number)
   {
      sum += number;
      steps++;
      if (sum < 0) {
         out << sum << " after " << steps << " steps" << endl;
         return true;
      }
   }
   out << "no negative sum" << endl;
   return false;
}


// Above here
int main()
{
    istringstream in("38 4 19 -27 -15 -3 4 19 38");
    bool result = negativeSum(in, cout);
    in.clear();
    in.str("14 7 -10 9 -18 -10 17 42 98");
    result = negativeSum(in, cout);
}

```

/*
```text
Running negativeSum.cpp

no negative sum
-8 after 6 steps

pass

Score

1/1
```
\*/

https://codecheck.io/files/23041117062z1mdyha751mk98lsllogl97g