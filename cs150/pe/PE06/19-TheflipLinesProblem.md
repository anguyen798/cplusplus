// Write a function named flipLines that accepts an input stream and an output stream as parameters. The input stream represents an input file. Your function writes to the output stream the same file's contents with successive pairs of lines reversed in order.
// For example, if the input file contains the following text:

/*
```text
// Twas brillig and the slithy toves
// did gyre and gimble in the wabe.
// All mimsey were the borogroves,
// and the mome raths outgrabe.
// "Beware the Jabberwock, my son,
// the jaws that bite, the claws that catch,
// Beware the JubJub bird and shun
// the frumious bandersnatch."
```
\*/

// The program should print the first pair of lines in reverse order, then the second pair in reverse order, then the third pair in reverse order, and so on. Therefore your function should produce the following output to the output stream:

/*
```text
// did gyre and gimble in the wabe.
// Twas brillig and the slithy toves
// and the mome raths outgrabe.
// All mimsey were the borogroves,
// "Beware the Jabberwock, my son,
// Beware the JubJub bird and shun
// the jaws that bite, the claws that catch,
// the frumious bandersnatch."
```
\*/

// Notice that a line can be blank, as in the third pair. Also notice that an input file can have an odd number of lines, as in the one above, in which case the last line is printed in its original position. You may not make any assumptions about how many lines are in the input stream.

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

void flipLines(..., ...)
{
  . . .
}

// Above here
int main() {
    istringstream in(
        "Twas brillig and the slithy toves\n"
        "did gyre and gimble in the wabe.\n"
        "All mimsey were the borogroves,\n"
        "and the mome raths outgrabe.\n"
        "\n"
        "\"Beware the Jabberwock, my son,\n"
        "the jaws that bite, the claws that catch,\n"
        "Beware the JubJub bird and shun\n"
        "the frumious bandersnatch.\"\n"
    );
    flipLines(in, cout);
}

```

/*
```text
Running flipLines.cpp

did gyre and gimble in the wabe.
Twas brillig and the slithy toves
and the mome raths outgrabe.
All mimsey were the borogroves,
"Beware the Jabberwock, my son,

Beware the JubJub bird and shun
the jaws that bite, the claws that catch,
the frumious bandersnatch."

pass

Score

1/1
```
\*/

// https://codecheck.io/files/2304111920ecdb1ddjgyn3su6yud1dcpfrg