// Given a string, compute recursively (no loops) a new string where all appearances of "pi" have been replaced by "3.14".

// * changePi("xpix") → "x3.14x"
// * changePi("pipi") → "3.143.14"
// * changePi("pip") → "3.14p"

```cpp
string changePi(const string& str)
{
   if (str.size() < 2) return str;
   else
   {
      if (str.substr(0, 2) == "pi") return "3.14" + changePi(str.substr(2));
      else return str.at(0) + changePi(str.substr(1));
   }
}
```

// https://codecheck.io/files/23030223304plcu8b16kwuz354xl69h8hmp