// Write a function triathlon that accepts an input stream and an output stream as arguments.
// The input stream represents triathlon race results for athletes. Add up the swimming, biking, and running times for each athlete and report the total time for each athlete and their time difference from the winner's. Each athlete's data is represented by four tokens in the following order: athlete's first name, swimming time, biking time, and running time (all times are given in minutes). The data for an athlete may or may not span multiple lines, but you are guaranteed the athletes will come in the order they finished the race (the winner's data is first, the second place triathlete's data comes next, etc.).

// Here is an example input. Notice the spacing and that the order the athletes appear are in the same order that they finished the race:

/*
```text
// Meghan 12 40 23 Bryan 16
// 42 20 Lori 14 41 29 Jessica 18
// 37 30 Toni 19 43
// 29 Tamara 17 42 34
```
\*/

// For this input, you function should produce the output below. For example, Meghan swam for 12 minutes, biked for 40 minutes, and ran for 23 minutes so it took for Meghan 75 minutes to finish the race. Notice that for the athletes that did not win the race, in addition to reporting their total race time, the difference in their time from the winner's is also reported. For example, Bryan swam for 16 minutes, biked for 42 minutes, and ran for 20 minutes so it took Bryan 78 minutes to finish the race, which is 3 minutes longer than Meghan's winning time of 75 minutes.

/*
```text
// Meghan: 75 min
// Bryan: 78 min (+3 min)
// Lori: 84 min (+9 min)
// Jessica: 85 min (+10 min)
// Toni: 91 min (+16 min)
// Tamara: 93 min (+18 min)
```
\*/

// You may assume that the input stream contains data for at least one athlete. You may also assume that the input is valid; that the input has four tokens per athlete, the first token for an athlete is a string and the following three are integers.

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

void triathalon(..., ...)
{
  . . .
}

// Above here
int main()
{
    istringstream in("Meghan 12 40 23 Bryan 16\n"
                    "42 20 Lori 14 41 29 Jessica 18\n"
                    "\n"
                    "       37 30 Toni 19   43\n"
                    "29 Tamara 17 42 34\n");
    triathalon(in, cout);
}
```

/*
```text
Running triathalon.cpp

Meghan: 75 min
Bryan: 78 min (+3 min)
Lori: 84 min (+9 min)
Jessica: 85 min (+10 min)
Toni: 91 min (+16 min)
Tamara: 93 min (+18 min)

pass

Score

1/1
```
\*/

// https://codecheck.io/files/23041117321gby4r9iyyr504vwjjl7q4nwx