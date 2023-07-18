// Write a function named boyGirl that accepts an input stream and an output stream as arguments. The input stream contains a series of names followed by integers. The names alternate between boys' names and girls' names. Compute the absolute difference between the sum of the boys' integers and the sum of the girls' integers. The input could end with either a boy or girl; you may not assume that it contains an even number of names.

// If the input file tas.txt contains the following text:
// Steve 3 Sylvia 7 Craig 14 Lisa 13 Brian 4 Charlotte 9 Jordan 6

// then your function could be called in the following way:

// ifstream input("tas.txt"); boyGirl(input, cout);
// and should produce the following output, since the boys' sum is 27 and the girls' sum is 29:
// 4 boys, 3 girls
//    Difference between boys' and girls' sums: 2

// Here is some extra test data: 
/*
```text
// Steve 3 Sylvia 7 Craig 14 Lisa 13 Brian 4 Charlotte 9 Jordan 6 4 boys, 3 girls
//    Difference between boys' and girls' sums: 2
// Steve 3 Sylvia 7 Craig 14 Lisa 13 Brian 4 Charlotte 9 Jordan 10 4 boys, 3 girls
//    Difference between boys' and girls' sums: 2
// Frank 12 Alexandra 8 Xandros 6 Kyrie 9 Luther 5 Electra 13 Benandre 7 4 boys, 3 girls
//    Difference between boys' and girls' sums: 0
// Jason 1 1 boys, 0 girls
//    Difference between boys' and girls' sums: 1
```
\*/

```cpp
#include <iostream>
#include <fstream>
#include <sstream>
#include <iomanip>
#include <string>
#include <vector>
#include <cmath>
using namespace std;
/**
 *  Write the procedure boyGirl
 *  @param in the input stream to read from
 *  @param out the output stream to write to
 */
// Below here

void boyGirl(istream &in, ostream &out)
{
   string name;
   int score;
   int boys {0}, girls {0}, sumBoys {0}, sumGirls {0};
   
   // loop over the input stream
   while(in >> name >> score)
   {
      if ((boys + girls) % 2 == 0) {
         boys++;
         sumBoys += score;
      }
      
      else {
         girls++;
         sumGirls += score;
      }
   }
   
   // compute and print the difference
   int diff = abs(sumBoys - sumGirls);
   out << boys << " boys, " << girls << " girls" << endl;
   out << "Difference between boys' and girls' sums: " << diff << endl;
}

// Above here
int main()
{
    istringstream in;
    in.str("Steve 3 Sylvia 7 Craig 14 Lisa 13 Brian 4 Charlotte 9 Jordan 6");
    boyGirl(in, cout);
    in.clear();
    in.str("Steve 3 Sylvia 7 Craig 14 Lisa 13 Brian 4 Charlotte 9 Jordan 10");
    boyGirl(in, cout);
    in.clear();
    in.str("Frank 12 Alexandra 8 Xandros 6 Kyrie 9 Luther 5 Electra 13 Benandre 7");
    boyGirl(in, cout);
    in.clear();
    in.str("Jason 1");
    boyGirl(in, cout);
    return 0;
}
```

/*
```text
Running boyGirl.cpp

4 boys, 3 girls
Difference between boys' and girls' sums: 2
4 boys, 3 girls
Difference between boys' and girls' sums: 2
4 boys, 3 girls
Difference between boys' and girls' sums: 0
1 boys, 0 girls
Difference between boys' and girls' sums: 1

pass

Score

1/1
```
\*/
// https://codecheck.io/files/23041019344qkghutu9lzrnrxw17q6p2r8u