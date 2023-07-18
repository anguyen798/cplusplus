// Write a function tokenStats that takes an input stream and an output stream as arguments. Report the number of lines in the file, the longest line, the number of tokens on each line, and the length of the longest token on each line. Assume at least one line of input and that each line has at least one token.

// For example, if an input stream contains the following text:
/*
```text
// "Beware the Jabberwock, my son,
// the jaws that bite, the claws that catch,
// Beware the JubJub bird and shun
// the frumious bandersnatch."
```
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

void tokenStats(..., ...)
{
  . . .
}

// Above here
int main()
{
    istringstream in(
        "\"Beware the Jabberwock, my son,\n"
        "the jaws that bite, the claws that catch,\n"
        "Beware the JubJub bird and shun\n"
        "the frumious bandersnatch.\""
    );
    tokenStats(in, cout);
}
```

/*
```text
Running tokenStats.cpp

Line 1 has 5 tokens (longest = 11)
Line 2 has 8 tokens (longest = 6)
Line 3 has 6 tokens (longest = 6)
Line 4 has 3 tokens (longest = 14)
Longest line: the jaws that bite, the claws that catch,

pass

Score

1/1
```
\*/

// https://codecheck.io/files/230410202966x8awuevuymlsx5dazfzfvfe