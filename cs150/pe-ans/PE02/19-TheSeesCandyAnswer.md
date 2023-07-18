// We want to pack up a box of custom chocolate bars. We have some small chocolates (1 gram each) and some large chocolates (5 grams each). Each box will have a goal. Print the number of small bars to use, assuming we always use big bars before small bars. Print -1 if it can't be done.

// * for input of small=4, large=1, goal=9 → 4
// * for input of small=4, large=1, goal=10 → -1
// * for input of small=4, large=1, goal=7 → 2

```cpp
#include <string>
using std::string;

/**
 *  We want to pack up a box of custom chocolate bars. 
 *  We have some small chocolates (1 gram each) and some 
 *  large chocolates (5 grams each). Each box will have a 
 *  goal. Set result to the number of small bars to use, assuming 
 *  we always use big bars before small bars. Set result to -1 
 *  if it can't be done. 
 */
int sees_candy(int small, int big, int goal)
{
    int result;

    // Add your code here
    // Maximum number of big chocolates that can be used
    int maxBig {goal / 5}; 
    
    // Use as many big chocolates as possible
    if (big >= maxBig)  { goal -= maxBig * 5;  }
    
    // Use all big chocolates if they are not enough
    else  { goal -= big * 5;  }
    
    // Use small chocolates to reach the goal
    if (goal <= small) { result = goal; }
    
    // Can't reach the goal even after using all chocolates
    else  { result = -1; }
    
    return result;
}
```

/*
Calling with Arguments

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|sees_candy|4, 1, 9|4|4|
|pass|sees_candy|4, 1, 10|-1|-1|
|pass|sees_candy|4, 1, 7|2|2|

Score

3/3
\*/

// https://codecheck.io/files/23020919496cge4uu9hdjkg29suibkvxg9e