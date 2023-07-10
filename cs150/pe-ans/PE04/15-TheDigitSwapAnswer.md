// Write a function named swapDigitPairs() that accepts a positive integer n as an input-output parameter which is changed to a new value similar to n's but with each pair of digits swapped in order. For example:

// int n = 482596;
// int old = swapDigitPairs(n);
// cout << "n->" << n << ", old->" << old << endl;

// This returns 482597 but changes n to 845269. Notice that the 9 and 6 are swapped, as are the 2 and 5, and the 4 and 8. If the number contains an odd number of digits, leave the leftmost digit in its original place. For example:
// n = 1234567;
// old = swapDigitPairs(n);
// cout << "n->" << n << ", old ->" << old << endl;

// This converts n into 1325476. Solve this problem without using a string.

```cpp
int swapDigitPairs(int &n)
{
    int originalN {n}, result {0}, multiplier {1};
    
    while (n > 0)
    {
       int digit1 = n % 10;
       n /= 10;
       
       if (n > 0)
       {
          int digit2 = n % 10;
          n /= 10;
          
          result += multiplier * (10 * digit1 + digit2);
          multiplier *= 100;
       }
       
       else result += multiplier * digit1;
    }
    
    n = result;
    
    return originalN;
}
```

// https://codecheck.io/files/2303031759acpkr7fo214t37v4c5yx3v70n