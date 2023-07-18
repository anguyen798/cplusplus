// Write a function pizza that accepts an input stream and an output stream as arguments. Imagine that a college dorm room contains several boxes of leftover pizza. A complete pizza has 8 slices. The pizza boxes left in the room each contain either an entire pizza, half a pizza (4 slices), or a single slice. Your function's task is to figure out the fewest boxes needed to store all leftover pizza, if all the partial pizzas were consolidated together as much as possible.

// Read lines from input where each line represents the contents of the pizza boxes in one dorm room. These contents are written as whole, "half", or "slice" in either upper or lower case, separated by at least one space. You should print to output the number of pizza boxes necessary to store all the slices of pizza out of the total. You must use a whole number of boxes. For example, if there are 10 total slices of pizza in a dorm room, 2 pizza boxes are needed: one for the first whole pizza, and one for the final 2 slices. Note that some lines might be blank, meaning that the dorm room contains no pizzas; output for such a case is shown below.

// Consider the following input file representing 5 dorm rooms (note that the fourth is blank):

/*
```text
// slice half slice whole whole half half half
// whole HALF WhoLE half WHOLE WhOlE Slice half sLICe halF
// WHOLE slice WHOLE SLICE whole SLICE whole slice WHOLE half
```
\*/

// For the input above, your function should produce the following output:
/*
```text
// 5 / 8 pizza boxes used
// 7 / 10 pizza boxes used
// 6 / 10 pizza boxes used
// 0 / 0 pizza boxes used
// 1 / 1 pizza boxes used
```
\*/

// The number following the slash is the number of original boxes, the number preceding it are the minimum number of boxes required. For instance on line 1, the dorm room had 8 boxes, but by combining, we can store all the pizza in 5 boxes.

// The format of your output must exactly match that shown above. You may assume that the input stream contains at least 1 line of input, and that no tokens other than whole/half/slice.

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

void pizza(istream & in, ostream & out)
{
   string line;
   int sliceCount, boxCount;
   string pizzaType;

   while (getline(in, line))
   {
      sliceCount = 0;
      boxCount = 0;
      istringstream iss(line);

      while (iss >> pizzaType)
      {
         for (char & c: pizzaType) { c = tolower(c); }

         if (pizzaType == "slice") {
            sliceCount += 1;
            boxCount += 1;
         }
         else if (pizzaType == "half") {
            sliceCount += 4;
            boxCount += 1;
         }
         else if (pizzaType == "whole") {
            sliceCount += 8;
            boxCount += 1;
         }
      }

      int boxesNeeded {(sliceCount + 7) / 8}; // Use integer division to round up
      out << boxesNeeded << " / " << boxCount << " pizza boxes used\n";
   }
}

// Above here
int main()
{
    istringstream in("slice half slice whole whole half half half\n"
        "whole HALF   WhoLE half WHOLE  WhOlE  Slice         half sLICe halF\n"
        "WHOLE slice   WHOLE SLICE whole SLICE    whole slice WHOLE half\n"
        "\n"
        "slice\n"
    );
    pizza(in, cout);
}

```

/*
```text
Running pizza.cpp

5 / 8 pizza boxes used
7 / 10 pizza boxes used
6 / 10 pizza boxes used
0 / 0 pizza boxes used
1 / 1 pizza boxes used

pass

Score

1/1
```
\*/

// https://codecheck.io/files/23041118257ai9t2mj3v0tlx04bcujvn4qo