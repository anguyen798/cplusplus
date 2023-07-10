// Write a function named swapPairs() that accepts a string reference as a parameter and modifies that string so that each pair of adjacent letters will be reversed. If the string has an odd number of letters, the last letter is unchanged. For example, if a string variable s stores "example", the call of swapPairs(s); should change the string to "xemalpe". If s had been "hello there", the call would produce "ehll ohtree".

// The function should return the number of "swaps" made. (Remember that there are three assignments involved in each swap.) Do not use any string functions from the standard library other than size() and at().

```cpp
int swapPairs(string &str)
{
   int swaps {0};
   for (size_t i {0}, len {str.size()}; i < len - 1; i += 2)
   {
      char temp = str.at(i);
      str.at(i) = str.at(i + 1);
      str.at(i + 1) = temp;
      ++swaps;
   }
   
   return swaps;
}
```

// https://codecheck.io/files/2303032026hvngaa56ghfik3g3vfz29yek