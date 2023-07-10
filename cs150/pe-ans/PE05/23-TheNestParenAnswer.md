// Given a string, return true if it is a nesting of zero or more pairs of parenthesis, like "(())" or "((()))". Suggestion: check the first and last chars, and then recur on what's inside them.

// * nestParen("(())") → true
// * nestParen("((()))") → true
// * nestParen("(((x))") → false

```cpp
bool nestParen(const string& str)
{
   size_t len {str.size()};
   if (str.empty()) return true;
   else if (len == 1) return false;
   else if (str.at(0) == '(' && str.at(len - 1) == ')')
   {
      return nestParen(str.substr(1, len - 2));
   }
   else return false;
}
```

// https://codecheck.io/files/2303022229xgmiui3ki3d1rf0cei6s5ekr
