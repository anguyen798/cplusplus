Given an input string, set result to the length of the largest "block" in the string. A block is a run of adjacent chars that are the same.

* for input of "hoopla" → 2
* for input of "abbCCCddBBBxx" → 3
* for input of "" → 0

```cpp
#include <string>
using std::string;

/**
 *  Given an input string, set result to the length of
 *  the largest "block" in the string. A block is a run
 *  of adjacent chars that are the same.
 *  Do not use any string functions except for substr(),
 *  at(), and size().
 */
int max_run(const string& str)
{
   int result;
   // Add your code here
   result = 0;  // to avoid error with size_t i initialization
   int current_run {1};
   for (size_t i {1}, len {str.size()}; i < len; ++i)
   {
       if (str.at(i) == str.at(i - 1))
       {
           ++current_run;
           if (current_run > result)
           {
               result = current_run;
           }
       }
       else
       {
           current_run = 1;
       }
   }
   return result;
}
```

[maxBlock.cpp](https://codecheck.io/files/2302092037blz0eij5mubyn6u557wk7kgrc)

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|max_run|"hoopla"|2|2|
|pass|max_run|"abbCCCddBBBxx"|3|3|
|pass|max_run|""|0|0|

The task can be solved by iterating over the string and counting the length of each sequence of identical characters. If the length of the current sequence exceeds the length of the longest found sequence so far, we update our record. Here is how you can implement this:

This code counts the length of each block of identical characters and keeps track of the longest block it has seen so far. If the string is empty, the length of the longest block is 0, as there are no blocks at all. If the string has at least one character, the length of the longest block is at least 1.
