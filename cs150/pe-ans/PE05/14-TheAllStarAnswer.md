// Given a string, compute recursively a new string where all the adjacent chars are now separated by a "\*".

// * allStar("hello") → "h\*e\*l\*l\*o"
// * allStar("abc") → "a\*b\*c"
// * allStar("ab") → "a\*b"

```cpp
string allStar(const string& str)
{
   if (str.length() <= 1) return str;
   else return str.at(0) + string("*") + allStar(str.substr(1));
}
```

// https://codecheck.io/files/2303022322ebbm9nq136v4vb5h40yrq6he9