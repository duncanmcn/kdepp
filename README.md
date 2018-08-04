# kdepp

Kernel density estimation for C++. Multidimensional.

### Installation:

kdepp is a header only library.

Include the "include" folder of this repository.

### Example usage:


``` C++
    // 2D:

    #include "kdepp/kde.h"

    std::array<double, 2> p1 = {0, 1}; // a point of data (x, y)
    std::array<double, 2> p2 = {1, 2};

    std::vector<std::array<double, 2>> data = {p1, p2};

    kdepp::Kde2d kernel(data);

    std::array<double, 2> test_point = {1, 2.5};
    double result = kernel.eval(test_point);
    std::cout << res << std::endl;

```
