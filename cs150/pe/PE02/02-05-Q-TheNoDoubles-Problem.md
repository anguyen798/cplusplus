Return the sum of two 6-sided dice rolls, each in the range 1..6. However, if has_doubles (the third value input) is true, and, if the two dice show the same value, increment one die to the next value, wrapping around to 1 if its value was 6. Here are some examples.

* input of 2, 3, true → 5
* input of 3, 3, true → 7
* input of 3, 3, false → 6