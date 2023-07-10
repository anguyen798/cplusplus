// Given a string that contains a single pair of parenthesis, compute recursively a new string made of only of the parenthesis and their contents, so "xyz(abc)123" yields "(abc)".

// * parenBit("xyz(abc)123") → "(abc)"
// * parenBit("x(hello)") → "(hello)"
// * parenBit("(xy)1") → "(xy)"

```cpp
string parenBit(const string& str)
{
   size_t len {str.size()};
   if (str.empty()) return "";
   else if (str.at(0) == '(')
   {
      if (str.at(len - 1) == ')') return str;
      else return parenBit(str.substr(0, len - 1));
   }
   else return parenBit(str.substr(1));
}
```

// https://codecheck.io/files/2303022237egyekqtask1iqvz76l92atadm