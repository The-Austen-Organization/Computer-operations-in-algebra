For the operations that rely on calculator accuracy, so rememeber to set the calculator to 9 decimal places, go to the calculator settings, go to `Fix` and then sellect 9.

| Computer Operation| Algebraic representation|
|--------------|-----------|
| absolute value, $abs(x)$ | $f(x) = \sqrt{x^2}$ |
| floor function, $\lfloor x \rfloor$ | $f(x) = Rnd(\frac{x - 0.499999999}{10^9}) \cdot 10^9$ |
| ceiling function, $\lceil x \rceil$ | $f(x) = Rnd(\frac{x + 0.499999999}{10^9}) \cdot 10^9$ |
| modulo, $x$ $mod$ $y$ | $f(x, y) = \sqrt{(y(\frac{x}{y} - Rnd(\frac{\frac{x}{y} - 0.499999999}{10^9}) \cdot 10^9))^2}$ |
| checks if the number is even (returns 1 if true and 0 if false) | $f(x) = 2(\frac{x + 1}{2} - Rnd(\frac{\frac{x + 1}{2} - 0.499999999}{10^9}) \cdot 10^9)$ |
| checks if the number is odd (returns 1 if true and 0 if false) | $f(x) = 2(\frac{x}{2} - Rnd(\frac{\frac{x}{2} - 0.499999999}{10^9}) \cdot 10^9)$ |
