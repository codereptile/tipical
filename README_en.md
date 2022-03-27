# tipical
A summary of most typical mistakes in C++ and programming languages in general

Under TL , OL is also taken

WA/RE/TL/ML:
* overflow (data types)
* initialization (fill with zeros /default values)
* go beyond the boundaries of the array
* wrong formula (wrong code)

WA/RE:
* there is no return from the function (the function should have returned something, but did not return anything (that is, returned garbage))
* access the wrong pointer
* mixed up the order of traversing a multidimensional array

RE/TL/ML:
* infinite recursion

WA:
* working with float/double incorrectly (comparing them incorrectly)
```cpp
#include <iostream>
#include <cmath>

#define EPS 0.00000001
#define double_cmp(a, b) std::fabs(a - b) < EPS

int main() {
double a = 1.0/3;
double b = 1.0/33;
if (double_cmp(a, b * 11)) {
std::cout << "OK\n";
} else {
std::cout << "not OK\n";
}
}
```

RE:
* will refer to `nullptr`

TL:
* infinite loop
* lack of I/O optimization

TL/ML:
* Do 'push_back' without 'reserve`

Stubborn mistakes:
* `;`
* name conflict
* `if (a = 0) ...`
* `double x = 1/3;`
