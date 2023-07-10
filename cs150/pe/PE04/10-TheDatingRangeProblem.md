// Write a function named datingRange() that accepts three parameters: an integer input parameter for a person's age, and two integer output parameters for a minimum and maximum. The function should fills the min/max integers with the person's xkcd "dating range" as described in the following web comic strip:

// Panel 1 | This sucks. The Median First Marriage Age is 26. The Pool of Singles is Shrinking. I'm running out of time. | Actually not quite.
// Panel 2 | No dialogue | Yes, older singles are rarer. but as you get older, the date-able age range gets wider. An 18-Year-Old's range is 16-22, whereas as 30-year-old's might be more like 22-46. Standard Creepiness Rule: Don't date under (Age / 2 + 7)

// Your minimum xkcd dating age is half your own age plus 7. Your maximum xkcd dating range is your own age, minus 7, then doubled. For example, the call datingRange(48, min, max); sets min to 31 and max to 82. You may assume that the age value passed is a non-negative integer.

// https://codecheck.io/files/23030319072sp975gsr4r01hdxbiovom8nl