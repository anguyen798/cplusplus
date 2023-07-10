// Write a function named makeChange() that takes two double input parameters, cost and amount, along with three int output parameters: quarters (25 cents), dimes (10 cents) and cents. We'll skip using nickels (5 cent coins) for this problem.

// The cost is the cost of your purchases, and the amount is the amount you give to the cashier. Your function will calculate the change after subtracting the cost of the purchases from the amount. The output variables quarters, dimes and cents will be used for to return the coins and the return statement will be used to return the dollars.

// Here's an example. Your purchases are $1.08 and you pay with a $5.00 bill. Your change is:
// int quarters, dimes, cents;
// int dollars = makeChange(1.08, 5.00, quarters, dimes, cents); cout << dollars << " dollars, " << quarters << " quarters, " << dimes << " dimes, and " << cents << " cents" << endl; // 3 dollars, 3 quarters, 1 dimes, and 7 cents

```cpp
int makeChange(double cost, double amount, int &quarters, int &dimes, int &cents)
{
    double change {amount - cost};
    int dollars {static_cast<int>(change)};
    change = (change - dollars) * 100; // convert to cents

    quarters = static_cast<int>(change) / 25;
    change -= quarters * 25;

    dimes = static_cast<int>(change) / 10;
    change -= dimes * 10;

    cents = static_cast<int>(change + 0.5); // rounding to nearest cent

    return dollars;
}
```

// https://codecheck.io/files/230303212966piz800ikvl3tr926mlmjhyc