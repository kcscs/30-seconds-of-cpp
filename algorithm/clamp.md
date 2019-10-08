# clamp

**Description:** Clamps a value `x` to a given range `[a, b]`.  

**Parameters:** `clamp(x, a, b)` clamps the value of `x` to the range `[a, b]`.  
A custom `Compare` object can be provided as a 4th parameter, othervise the operator `<` is used by default.

**Return value:** Returns a *reference* to either parameter such that the returned value is:
+ `a` if `x < a`
+ `x` if `a ≤ x ≤ b`
+ `b` if `b < x`


**Example**

```cpp
    std::cout << std::clamp(3, 1, 4) << '\n';         // prints 3
    std::cout << std::clamp(-2.6, 0.5, 3.0) << '\n';  // prints 0.5
    std::cout << std::clamp(3, 0, 1) << '\n';         // prints 1

    std::greater<int> cmp;  // Comparer object used for the comparison
    std::cout << std::clamp(0, 1, 2, cmp) << '\n';    // prints 2
```