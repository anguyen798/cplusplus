// Write a function dupeCount that accepts an input stream and an output stream as arguments.
// The input stream contains a series of lines as shown below. Examine each line looking for consecutive occurrences of the same token on the same line and output each duplicated token along how many times it appears consecutively.
// For example, if the input stream contains the following text:
/*
```text
// hello how how are you you you you
// I I I am Jack's Jack's smirking smirking smirking smirking smirking revenge
// bow wow wow yippee yippee yo yippee yippee yay yay yay
// one fish two fish red fish blue fish
// It's the Muppet Show, wakka wakka wakka
```
\*/

// Your function would produce the following output:
/*
```text
// how*2 you*4
// I*3 Jack's*2 smirking*5
// wow*2 yippee*2 yippee*2 yay*3
// wakka*3
```
\*/

// Only output repeated tokens; the ones that only appear once in a row are not shown. Place a single space between each reported duplicate token; respect the line breaks in the input. This is why a blank line appears in the expected output, corresponding to the fourth line of the input that did not contain any consecutively duplicated tokens. You may assume that each line of the input contains at least 1 token of.

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
void dupeCount(istream &in, ostream &out)
{
    string line;

    while(getline(in, line))
    {
        istringstream iss(line);
        string prevWord, word;
        int count {0};
        bool first = true;

        while(iss >> word)
        {
            if(first) {
                prevWord = word;
                count = 1;
                first = false;
            }
            else if(word == prevWord) {
                count++;
            }
            else
            {
                if(count > 1) {
                    out << prevWord << "*" << count << " ";
                }
                prevWord = word;
                count = 1;
            }
        }

        if(count > 1) {
            out << prevWord << "*" << count << " ";
        }

        out << endl;
    }
}
// Above here
int main()
{
    ifstream in("dupeCount.txt");
    dupeCount(in, cout);
}
```

/*
```text
hello how how are you you you you
I I I am Jack's Jack's smirking smirking smirking smirking smirking revenge
   bow  wow wow yippee yippee   yo yippee   yippee yay  yay yay
one fish two fish red fish blue fish
It's the Muppet Show, wakka wakka wakka
```

```text
Running dupeCount.cpp

how*2 you*4 
I*3 Jack's*2 smirking*5 
wow*2 yippee*2 yippee*2 yay*3 

wakka*3 

pass

Score

1/1
```

\*/

// https://codecheck.io/files/23041020038m7y1zfjxqpn6x16hygtwrmak