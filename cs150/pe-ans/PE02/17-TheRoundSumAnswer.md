// Given 3 ints, a b c, return the sum of their rounded values. For this problem, we'll round an int value up to the next multiple of 10 if its rightmost digit is 5 or more, so 15 rounds up to 20. Alternately, round down to the previous multiple of 10 if its rightmost digit is less than 5, so 12 rounds down to 10. To avoid code repetition, you may write a separate helper function but that is not required. The helper should appear before the tested program.

// * input of 16, 17, 18 → 60
// * input of 12, 13, 14 → 30
// * input of 6, 4, 4 → 10

```cpp
#include <string>
using std::string;

/**
 *  Given 3 ints, a b c, set result to the sum of their 
 *  "rounded" values. For this problem, we'll round an 
 *  int value up to the next multiple of 10 if its rightmost 
 *  digit is 5 or more, so 15 rounds up to 20. Alternately, 
 *  round down to the previous multiple of 10 if its rightmost 
 *  digit is less than 5, so 12 rounds down to 10. 
 *  To avoid code repetition, you may write a separate helper 
 *  function but that is not required. The helper should appear 
 *  before the tested function. 
 */
int round10(int num)
{
	if (num % 10 < 5) { return num / 10 * 10; }
	else { return (num / 10 + 1) * 10; }
}

int round_sum(int a, int b, int c)
{
   int result;

   // ---- YOUR CODE GOES ONLY BELOW THIS LINE
   // Add your code here
   result = round10(a) + round10(b) + round10(c);
   
   return result;
}
```

/*

Calling with Arguments

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|round_sum|16, 17, 18|60|60|
|pass|round_sum|12, 13, 14|30|30|
|pass|round_sum|6, 4, 4|10|10|

Score

3/3

\*/

// https://codecheck.io/files/23020919426qn6540nw5qnrj40w3wdof8k3
