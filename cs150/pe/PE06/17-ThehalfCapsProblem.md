// Write a function halfCaps that accept an input stream and an output stream as arguments. The input stream contains a sequence of words. Your function should output the same sequence of words with alternating casing (lowercase, uppercase, lowercase, uppercase, etc). The first word, third word, fifth word, and all other "odd" words should be in lowercase letters, whereas the second word, fourth word, sixth word, and all other "even" words should be in uppercase letters.

//For example, suppose the input contains the following words.
// The QUick brown foX jumPED over the Sleepy student

// For the purposes of this problem, we will use whitespace to separate words. You can assume that the sequence of words will not contain any numbers or punctuation and that each word will be separated by one space. For the input above, your function should produce the following output:
// the QUICK brown FOX jumped OVER the SLEEPY student

// Your output should separate each word by a single space. The output may end with a space if you like. Note that the input stream may contain no words or may contain an even or odd number of words.

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

void halfCaps(..., ...)
{
  . . .
}

// Above here
int main()
{
    istringstream in("The QUick brown foX jumPED over the Sleepy student");
    halfCaps(in, cout);
}

```

/*
```text
Running halfCaps.cpp

the QUICK brown FOX jumped OVER the SLEEPY student 

pass

Score

1/1
```
\*/

// https://codecheck.io/files/2304111854conmx9n7zv9l289znhpqhtjo5