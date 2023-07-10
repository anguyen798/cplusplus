// Given a string, compute recursively (no loops) a new string where all the lowercase 'x' chars have been changed to 'y' chars.

// * changeXY("codex") → "codey"
// * changeXY("xxhixx") → "yyhiyy"
// * changeXY("xhixhix") → "yhiyhiy"

```cpp
string changeXY(const string& str)
{
   if (str.empty()) return "";
   else
   {
      char firstChar {str.at(0)};
      string restOfString {changeXY(str.substr(1))};
      if (firstChar == 'x') return 'y' + restOfString;
      else return firstChar + restOfString;
   }
}
```

// https://codecheck.io/files/23030223347ikqoqk2e63qk8avk758nfjny