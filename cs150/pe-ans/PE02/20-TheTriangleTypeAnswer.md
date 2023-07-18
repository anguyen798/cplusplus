// Given three integers (a, b and c) representing the lengths of the sides of a triangle, return what type of triangle it is. The three types are equilateral, isosceles, and scalene. An equilateral triangle has all three sides the same length, an isosceles triangle has two sides the same length, and a scalene triangle has three sides of different lengths. Here are some examples:

// * for input of 5, 7, 7 →isosceles
// * for input of 6, 6, 6 →equilateral
// * for input of 5, 7, 8 →scalene
// * for input of 12, 18, 12 →isosceles

```cpp
#include <string>
using std::string;

/**
 *  Given three integers (a, b and c) representing 
 *  the lengths of the sides of a triangle, return
 *  what type of triangle it is. The three types 
 *  are equilateral, isosceles, and scalene. 
 *     An equilateral triangle has all three sides the same length
 *     An isosceles triangle has two sides the same length
 *     A scalene triangle has three sides of different lengths.
 */
string triangle_type(int a, int b, int c)
{
   string result;

  // Add your code here
  if (a == b && b == c) { result = "equilateral"; }
  else if (a == b || b == c || a == c) { result = "isosceles"; }
  else { result = "scalene"; }
   
   return result;
}
```

/*
Calling with Arguments

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|triangle_type|5, 7, 7|"isosceles"|"isosceles"|
|pass|triangle_type|6, 6, 6|"equilateral"|"equilateral"|
|pass|triangle_type|15, 7, 8|"scalene"|"scalene"|

Score

3/3

\*/

// https://codecheck.io/files/23020919529pi5ko5kbtopazppu81xhorfh