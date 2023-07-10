// Write a function named crazyCaps() that accepts a string as an input-output parameter and changes that string to have its capitalization altered such that the characters at even indexes are all in lowercase and odd indexes are all in uppercase. For example, if a variable s stores "Hey!! THERE!", then the call of crazyCaps(s); should change s to store "hEy!! tHeRe!". The function should return the original (unmodified) string.

// Do not use any string functions from the standard library other than size() and at(). Remember that you can find the difference between upper and lowercase characters by subtracting 'A' from 'a'. Do not use the topper() or tolower() macros from cctype.

```cpp
string crazyCaps(string &str)
{
   char capitalize {'a' - 'A'};
   string originalStr {str};
   for (size_t i {0}, len {str.size()}; i < len; ++i)
   {
      if (i % 2 == 0)
      {
         // Convert even indexed characters to lowercase
         if (str.at(i) >= 'A' && str.at(i) <= 'Z') str.at(i) += capitalize;
      }
      else
      { 
         // Convert odd indexed characters to uppercase
         if (str.at(i) >= 'a' && str.at(i) <= 'z') str.at(i) -= capitalize;
      }
   }
   
   return originalStr;
}
```

// https://codecheck.io/files/23030320438iehks5sezscbbkmxjd45x3f1