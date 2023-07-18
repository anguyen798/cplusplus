// Write a function countCoins that accepts an input stream and an output stream as arguments. The input stream represents a person's money grouped into stacks of coins. Add up the cash values of all the coins and print the total money at the end. Input is arranged as pairs of tokens, where each pair begins with an integer and is followed by the type of coin, which will be either "pennies" (1 cent each), "nickels" (5 cents each), "dimes" (10 cents each), or "quarters" (25 cents each), case-insensitively. A given coin might appear more than once on the same line.
// For example, if the input file contains the following text:
// 3 pennies 2 quarters 1 pennies 3 nickels 4 dimes
// 3 pennies are worth 3 cents, and 2 quarters are worth 50 cents, and 1 penny is worth 1 cent, and 3 nickels are worth 15 cents, and 4 dimes are worth 40 cents. The total of these is 1 dollar and 9 cents, therefore your function would produce the following output if passed this input data. Notice that the function should show exactly two digits after the decimal point, so it says 09 for 9 cents:
// Total money: $1.09
// Here is a second example. Suppose the input file contains the following text. Notice the capitalization and spacing:

// 12    QUARTERS    1    Pennies    33
// PeNnIeS
// 10 niCKELs

// Then your function would produce the following output:
// Total money: $3.84

// You may assume that the file contains at least 1 pair of tokens. You may also assume that the input is valid; that the input has an even number of tokens, that every other token is an integer, and that the others are valid coin types.

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

void countCoins(istream & in, ostream & out)
{
   int count;
   string type;
   double totalCents {0.0};

   while (in >> count >> type)
   {
      // Convert the type to lower case for case-insensitive comparison
      for (char & c: type) c = tolower(c);

      if (type == "pennies") { totalCents += count; }
      else if (type == "nickels") { totalCents += count * 5; }
      else if (type == "dimes") { totalCents += count * 10; }
      else if (type == "quarters") { totalCents += count * 25; }
   }

   // Convert cents to dollars
   double totalDollars {totalCents / 100};

   // Set precision to exactly 2 digits after the decimal point
   out << fixed << setprecision(2);

   // Output the result
   out << "Total money: $" << totalDollars << endl;
}

// Above here
int main()
{
    istringstream in("3 pennies 2 quarters 1 pennies 3 nickels 4 dimes");
    countCoins(in, cout);
    in.clear();
    in.str("12   QUARTERS      1   Pennies      33\n" 
            "PeNnIeS      \n"
            "\n"
            "    10    niCKELs\n"
            );
    countCoins(in, cout);
}

```

/*
```text
Running countCoins.cpp

Total money: $1.09
Total money: $3.84

pass

Score

1/1
```
\*/

// https://codecheck.io/files/23041117176dq9qpu1cgzmy1k396zoj5le2