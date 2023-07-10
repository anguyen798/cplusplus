// Given a string, compute recursively a new string where identical chars that are adjacent in the original string are separated from each other by a "\*".

// * pairStar("hello") → "hel\*lo"
// * pairStar("xxyy") → "x\*xy\*y"
// * pairStar("aaaa") → "a\*a\*a\*a"

```cpp
string pairStar(const string& str)
{
   if (str.size() <= 1) return str;
   else
   {
      if (str.at(0) == str.at(1)) return str.at(0) + string("*") + pairStar(str.substr(1));
      else return str[0] + pairStar(str.substr(1));
   }
}
```

// https://codecheck.io/files/23030223185pjkpn88ibjwhi55rmkg3h9lm