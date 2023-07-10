// Write a function named nameDiamond() that accepts a string as an input parameter and returns a new string in a "diamond" format as shown below through the output parameter diamond. For example, the call of

// string s = nameDiamond("MARTY", diamond);

// should set diamond to a string with embedded newlines, that looks like this when printed. Use `\n` for the embedded newlines. The last line should end with a newline. The call should return the number of lines in the string (in this case, 9).
// M
// MA
// MAR
// MART
// MARTY
//    ARTY
//      RTY
//        TY
//          Y

```cpp
int namedDiamond(const string& str, string& diamond)
{
   int lines {0};
   // Upper half of the diamond
   for (size_t i {1}, len {(str.size())}; i <= len; ++i)
   {
      diamond += str.substr(0, i) + "\n";
      ++lines;
   }
   
   // Lower half of the diamond
   for (size_t i {1}, len {(str.size())}; i < len; ++i)
   {
      diamond += string(len -i, ' ') + str.substr(i) + "\n";
      ++lines;
   }
   
   return lines;
}
```

// https://codecheck.io/files/23030321114rkr7fdnvp95sdvvfjrzakujp