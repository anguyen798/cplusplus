// Write a function stripHtmlTags that accepts an input stream and an output stream as arguments. The input stream contains an HTML web page as its parameter. Output the text with all HTML tags removed. A tag is any text between the characters < and >. For example, consider the following text:

/*
```text
// <html>
// <head>
// <title>My web page</title>
// </head>
// <body>
// <p>There are many pictures of my cat here,
// as well as my <b>very cool</b> blog page,
// which contains <font color="red">awesome
// stuff about my trip to Vegas.</p>
// Here's my cat now:<img src="cat.jpg">
// </body>
// </html>
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
// Below here

void stripHtmlTags(..., ...)
{
  . . .
}


// Above here
int main()
{
    ifstream in("webpage.html");
    stripHtmlTags(in, cout);
}
```

/*
```text
Running stripHtmlTags.cpp

My web page


There are many pictures of my cat here,
as well as my very cool blog page,
which contains awesome
stuff about my trip to Vegas.

Here's my cat now:

pass

Score

1/1
```
\*/

// https://codecheck.io/files/23041019459jo4fvcb5d41kn34b0zyiwkf6