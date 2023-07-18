// Write a function percentPlus that accepts an input stream and an output stream as arguments. The input stream represents student records; each student record takes up two lines of input. The first line has the student's name and the second line has a series of plus and minus characters. Below is a sample input:

/*
```text
// Kane, Erica
// --+-+
// Chandler, Adam
// ++-+
// Martin, Jake
// +++++++
// Dillon, Amanda
// ++-++-+-
```

\*/

// The number of plus/minus characters will vary, but you may assume that at least one such character appears and that no other characters appear on the second line of each pair. For each student you should produce a line of output with the student's name followed by a colon followed by the percent of plus characters.

// The above input should produce the following output:

/*
```text
// Kane, Erica: 40.0% plus
// Chandler, Adam: 75.0% plus
// Martin, Jake: 100.0% plus
// Dillon, Amanda: 62.5% plus
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

void percentPlus(..., ...)
{
  . . .
}

// Above here
int main()
{
    istringstream in(
        "Kane, Erica\n"
        "--+-+\n"
        "Chandler, Adam\n"
        "++-+\n"
        "Martin, Jake\n"
        "+++++++\n"
        "Dillon, Amanda\n"
        "++-++-+-\n"
    );
    percentPlus(in, cout);
}
```

/*
```text
Running percentPlus.cpp

Kane, Erica: 40.0% plus
Chandler, Adam: 75.0% plus
Martin, Jake: 100.0% plus
Dillon, Amanda: 62.5% plus

pass

Score

1/1
```

\*/

// https://codecheck.io/files/23041113363ayvoi1wjuu5tt00soguvd9o4