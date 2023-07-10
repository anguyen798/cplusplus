// Write a function named decToBin() that accepts an integer parameter whose digits are meant to represent decimal (base-10) digits, and converts that integer to a representation of binary (base-2). The function should return the integer value before it was converted. For example, given this code:

// int a = 43;
// int b = decToBin(a);
// cout << "a->" << a << ", b->" << b << endl;

// The output is: a->101011, b->43

// Constraints: Do not use a string in your solution. Also do not use any built-in base conversion functions from the system libraries. You must program this by "hand".

```cpp
int decToBin(int& a)
{
   int decimal {a}, binary {0}, base {1};
   while (a > 0)
   {
      int lastDigit = a % 2;
      binary += lastDigit * base;
      a /= 2;
      base *= 10;
   }
   a = binary;
   
   return decimal;
}
```

// https://codecheck.io/files/230303195570vk30y4ixii3tie9begifrr2