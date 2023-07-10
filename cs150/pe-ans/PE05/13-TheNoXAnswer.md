// Given a string, compute recursively a new string where all the 'x' chars have been removed.

// * noX("xaxb") → "ab"
// * noX("abc") → "abc"
// * noX("xx") → ""

```cpp
string noX(const string& str)
{
   if (str.empty()) return "";
   else
   {
      char firstChar {str.at(0)};
      string restOfString {noX(str.substr(1))};
      if (firstChar == 'x') return restOfString;
      else return firstChar + restOfString;
   }
}
```

// https://codecheck.io/files/2303022325br2wzp9s2auafh74101um4en9