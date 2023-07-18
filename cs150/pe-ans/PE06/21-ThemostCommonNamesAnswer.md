// Write a function named mostCommonNames that accepts an input stream and an output stream as parameters. The input stream represents an input file whose data is a sequence of lines, where each line contains a set of first names separated by spaces. Your function should print (to the output stream) the name that occurs the most frequently in each line of the file. The function should also return the total number of unique names that were seen in the file. You may assume that no name appears on more than one line of the file.

// Each line should be considered separately from the others. On a given line, some names are repeated; all occurrences of a given name will appear consecutively in the file. If two or more names occur the same number of times, print the one that appears earlier in the file. If every single name on a given line is different, every name will have 1 occurrence, so you should just print the first name in the file. 

// For example, if the input file contains the following text:

/*
```text
// Benson Eric Eric Marty Kim Kim Kim Jenny Nancy Nancy Nancy Paul Paul
// Stuart Stuart Stuart Ethan Alyssa Alyssa Helene Jessica Jessica Jessica Jessica
// Jared Alisa Yuki Catriona Cody Coral Trent Kevin Ben Stefanie Kenneth
```
\*/

//  On the first line, there is one occurrence of the name Benson, two occurrences of Eric, one occurrence of Marty, three occurrences of Kim, one of Jenny, three of Nancy, and two of Paul.

// Kim and Nancy appear the most times (3), and Kim appears first in the file. So for that line, your function should print that the most common is Kim. The complete output would be the following. The function would also return 23, since there are 23 unique names in the entire file

/*
```text
// Most common: Kim
// Most common: Jessica
// Most common: Jared
```
\*/

// You may assume that there is at least one line of data in the file and that each line will contain at least one name.


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

int mostCommonNames(istream & in, ostream & out)
{
   string line;
   vector < string > uniqueNames;
   int uniqueCount {0};
   while (getline(in, line))
   {
      istringstream iss(line);
      string name, prevName, mostCommon;
      int maxCount {0}, count {0};
      while (iss >> name)
      {
         if (name == prevName) { ++count; }

         else
         {
            if (count > maxCount) {
               maxCount = count;
               mostCommon = prevName;
            }

            count = 1;

            bool isUnique {true};
            for(const auto& uniqueName : uniqueNames)
            {
               if(name == uniqueName) {
                  isUnique = false;
                  break;
               }
            }
            if(isUnique) {
               uniqueNames.push_back(name);
               ++uniqueCount;
            }
         }

         prevName = name;
      }

      if (count > maxCount) { mostCommon = prevName; }
      out << "Most common: " << mostCommon << endl;
   }
   return uniqueCount;
}

// Above here
int main()
{
    istringstream in(
        "Benson Eric   Eric  Marty Kim  Kim Kim   Jenny  Nancy Nancy  Nancy  Paul  Paul\n"
        "Stuart Stuart Stuart Ethan Alyssa Alyssa Helene Jessica Jessica Jessica Jessica\n"
        "Jared  Alisa Yuki   Catriona  Cody   Coral   Trent Kevin  Ben Stefanie Kenneth\n"
    );
    int unique = mostCommonNames(in, cout);
    cout << unique << " unique names" << endl;
}
```

/*
```text
Running mostCommonNames.cpp

Most common: Kim
Most common: Jessica
Most common: Jared
23 unique names

pass

Score

1/1
```
\*/

// https://codecheck.io/files/23041119351b87fhale87kgnqliqdmgzzbq