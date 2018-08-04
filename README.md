# kdepp

Kernel density estimation for C++. Multidimensional.

### Installation:

kdepp is a header only library.

Include the "include" folder of this repository.

### Example usage:


``` C++
// 1D:
#include "kdepp/kde.h"

std::vector<float> data = {-0.1, 0, 0.1, 0.1, 0.2};
kdepp::Kde1d kernel(data);

auto result = kernel.eval(0.05);
std::cout << result << std::endl;


// 2D:

#include "kdepp/kde.h"

std::array<double, 2> p1 = {0, 2}; // a point of data (x, y)
std::array<double, 2> p2 = {0.15, 2.3};
std::array<double, 2> p3 = {-0.1, 2.5};

std::vector<std::array<double, 2>> data = {p1, p2, p3};

kdepp::Kde2d kernel(data);

std::array<double, 2> test_point = {0.1, 2.5};
double result = kernel.eval(test_point);
std::cout << result << std::endl;

```

### Convenience typedefs:

The following are provide for convenience if you are using C++14 or lower:

``` C++
// The template type is the data type.
// kdepp always takes a std::vector of the data type as the paramater in the constructor:
using Kde1d_d = Kde1d<double>;
using Kde1d_f = Kde1d<float>;
using Kde2d_vecd = Kde2d<std::vector<double>>;
using Kde2d_vecf = Kde2d<std::vector<float>>;
using Kde2d_arrd = Kde2d<std::array<double,2>>;
using Kde2d_arrf = Kde2d<std::array<float,2>>;
```
