// Write a function named matchIndex that accepts an input stream and an output stream as parameters. The input stream represents an input file. Your function should compare each neighboring pair of lines (the first and second lines, then the third and fourth lines, and so on) looking for places where the character at a given 0-based index from the two lines is the same. For example, in the strings "hello" and "belt", the characters at indexes 1 ('e') and 2 ('l') match. Your code should be case-sensitive; for example, "J" does not match "j".
// For each pair of lines, your function should print output showing the character indexes that match, separated by spaces in the format shown below. If no characters match, print "none" instead as shown below.
// For example, suppose the input file contains the following text. (Line numbers and character indexes are shown around the input and matching characters are shown in bold, but these markings do not appear in the actual file.)

/*
```text
// 0123456789012345678901234567890123456789
// 1    The quick brown fox
// 2    Those achy down socks
// 3    Wheels on the school bus go round
// 4    The wipers go swish swish swish
// 5    His name is Robert Paulson
// 6    So long 'n thanks for all the fish
// 7    Humpty Dumpty sat on a wall
// 8    And then he also had a great fall
// 9    booyakasha
// 10  Bruno Ali G Borat
```
\*/

// When passed the above file, your function would produce the following output:
/*
```text
// lines 1 and 2: 0 1 7 12 13 14 15 17
// lines 3 and 4: 1 2 13 14 23
// lines 5 and 6: none
// lines 7 and 8: 4 14 20 21 22
// lines 9 and 10: none
```
\*/

// Notice that lines are not generally the same length. You may assume that the file contains an even number of lines.

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

void matchIndex(istream & in, ostream & out)
{
   string line1, line2;
   int lineCount {0};
   while (getline(in, line1) && getline(in, line2))
   {
      lineCount += 2;
      bool hasMatch {false};
      out << "lines " << lineCount - 1 << " and " << lineCount << ": ";
      for (size_t i = 0; i < min(line1.size(), line2.size()); ++i)
      {
         if (line1.at(i) == line2.at(i)) {
            hasMatch = true;
            out << i << " ";
         }
      }
      if (!hasMatch) { out << "none"; }
      out << '\n';
   }
}

// Above here
int main()
{
    istringstream in(
        "The quick brown fox\n"
        "Those achy down socks\n"
        "Wheels on the school bus go round\n"
        "The wipers go swish swish swish\n"
        "His name is Robert Paulson\n"
        "So long 'n thanks for all the fish\n"
        "Humpty Dumpty sat on a wall\n"
        "And then he also had a great fall\n"
        "booyakasha\n"
        "Bruno Ali G Borat\n"
    );
    matchIndex(in, cout);
}

```

/*
```text
Running matchIndex.cpp

lines 1 and 2: 0 1 7 12 13 14 15 17 
lines 3 and 4: 1 2 13 14 23 
lines 5 and 6: none
lines 7 and 8: 4 14 20 21 22 
lines 9 and 10: none

pass

Score

1/1
```
\*/

// https://codecheck.io/files/2304111930br7q2d8jrqkls78mixsx7yrl4