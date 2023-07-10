// Given a string, compute recursively a new string where all the lowercase 'x' chars have been moved to the end of the string.

// * endX("xxre") → "rexx"
// * endX("xxhixx") → "hixxxx"
// * endX("xhixhix") → "hihixxx"

```cpp
string endX(const string& str)
{
   if (str.empty()) return "";
   else
   {
      char firstChar {str.at(0)};
      string restOfString {endX(str.substr(1))};
      if (firstChar == 'x') return restOfString + firstChar;
      else return firstChar + restOfString;
   }
}
```

// https://codecheck.io/files/2303022312mp4bni0v6pev4kg0xke2b91