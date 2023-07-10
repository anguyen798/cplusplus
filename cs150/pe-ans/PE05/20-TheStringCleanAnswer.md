// Given a string, return recursively a "cleaned" string where adjacent chars that are the same have been reduced to a single char. So "yyzzza" yields "yza".

// * stringClean("yyzzza") → "yza"
// * stringClean("abbbcdd") → "abcd"
// * stringClean("Hello") → "Helo"

```cpp
string stringClean(const string& str)
{
   if (str.length() < 2) return str;
   else
   {
      if (str.at(0) == str.at(1)) return stringClean(str.substr(1));
      else return str.at(0) + stringClean(str.substr(1));
   }
}
```

// https://codecheck.io/files/230302225587s2mghg7hwvn5606zgimtxvd