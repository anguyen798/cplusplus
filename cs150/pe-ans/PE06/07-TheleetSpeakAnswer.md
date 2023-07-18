// Write a function leetSpeak that accepts an input stream and an output stream as arguments. Your function should convert the input file's text to "leet speak" (aka 1337 speak), an internet dialect where various letters are replaced by other letters/numbers. Output the leet version of the text to the given output stream. Preserve the original line breaks from the input. Also wrap each word of input in parentheses.

// Perform the following replacements:

// Original character : 'Leet' character
// o : 0
// l (lowercase L) : 1
// e : 3
// a : 4
// t : 7
// s (at the end of a word only) : Z

// For example, if the input file lincoln.txt contains the following text:
/*
```text
four score and seven years ago our fathers brought forth on this continent a new nation
```
\*/
// And your function is called in the following way:
// ifstream input("lincoln.txt");
// ofstream output("leet.txt");
// leetSpeak(input, output);

// Then after the call, the output file leet.txt should contain the following text:

/*
```text
(f0ur) (sc0r3) (4nd) (s3v3n) (y34rZ) (4g0) (0ur) (f47h3rZ) (br0ugh7) (f0r7h) (0n) (7hiZ) (c0n7in3n7) (4) (n3w) (n47i0n)
```
\*/

// You may assume that each token from the input file is separated by exactly one space.


```cpp
#include <iostream>
#include <fstream>
#include <sstream>
#include <string>
using namespace std;
// Below here

void leetSpeak(istream & in, ostream & out)
{
   string line;
   while (getline(in, line))
   {
      if (line.empty()) {
         out << endl;
         continue;
      }
      
      istringstream iss(line);
      string word;
      
      while (iss >> word)
      {
         for (auto & ch: word)
         {
            switch (ch)
            {
               case 'o': { ch = '0'; break; }
               case 'l': { ch = '1'; break; }
               case 'e': { ch = '3'; break; }
               case 'a': { ch = '4'; break; }
               case 't': { ch = '7'; break; }
               default: { break; }
            }
         }

         if (word.back() == 's') { word.back() = 'Z'; }
         out << "(" << word << ") ";
      }
      
      out << endl;
   }
}

// Above here
int main()
{
    istringstream in(
        "four score and\n"
        "seven years ago our\n"
        "\n"
        "fathers brought forth on this continent\n"
        "a new nation\n"
    );
    leetSpeak(in, cout);
}

```

/*
```text
Running leetSpeak.cpp

(f0ur) (sc0r3) (4nd) 
(s3v3n) (y34rZ) (4g0) (0ur) 

(f47h3rZ) (br0ugh7) (f0r7h) (0n) (7hiZ) (c0n7in3n7) 
(4) (n3w) (n47i0n) 

pass

Score

1/1
```
\*/

// https://codecheck.io/files/2304111351adz13w74eej1bkh4d0ebhzh0x