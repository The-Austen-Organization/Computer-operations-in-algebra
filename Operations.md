For the operations that rely on calculator accuracy, so rememeber to set the calculator to 9 decimal places, go to the calculator settings, go to `Fix` and then sellect 9. If you are using Desmos to graph out this programs use a `, 9` after the value of x that you want to round, for example `round(10/3, 9)`, what the equation in the back did was essencially round 10/3 to 9 decimal places.

| Computer Operation| Algebraic representation | Alternate representation |
| - | - | - |
| absolute value, $abs(x)$ | $f(x) = \sqrt{x^2}$ | sqrt(x^2) |
| floor function, $\lfloor x \rfloor$ | $f(x) = round(\frac{x - 0.499999999}{10^9}) \cdot 10^9$ | round((x - 0.499999999) / 10^9) * 10^9 |
| ceiling function, $\lceil x \rceil$ | $f(x) = round(\frac{x + 0.499999999}{10^9}) \cdot 10^9$ | round((x + 0.499999999) / 10^9) * 10^9 |
| modulo, $x$ $mod$ $y$ | $f(x, y) = \sqrt{(y(\frac{x}{y} - round(\frac{\frac{x}{y} - 0.499999999}{10^9}) \cdot 10^9))^2}$ | sqrt((y(x / y - round((x / y - 0.499999999) / (10^9)) * 10^9))^2) |
| checks if the number is even (returns 1 if true and 0 if false) | $f(x) = 2(\frac{x + 1}{2} - round(\frac{\frac{x + 1}{2} - 0.499999999}{10^9}) \cdot 10^9)$ | 2((x + 1) / 2 - round(((x + 1) / 2 - 0.499999999) / 10^9) * 10^9) |
| checks if the number is odd (returns 1 if true and 0 if false) | $f(x) = 2(\frac{x}{2} - round(\frac{\frac{x}{2} - 0.499999999}{10^9}) \cdot 10^9)$ | 2((x) / 2 - round(((x) / 2 - 0.499999999) / 10^9) * 10^9) |
| amount of digits in a number, $x \neq 0$, $len(x)$ | $f(x) = round(\frac{log(\sqrt{x^2}) - 0.499999999}{10^9}) \cdot 10^9 + 1$ | round(log(sqrt(x^2)) - 0.499999999) / 10^9 * 10^9 + 1
| if command, $if$ $x$ = 0, return 0, else return 1 | $f(x) = round(\frac{\frac{\sqrt{x^2}}{10^{round((log(\sqrt{x^2} + 1) - 0.499999999) / (10^9)) \cdot 10^9 + 1}} + 0.499999999}{10^9}) \cdot 10^9$ | round(((sqrt(x^2)/10^{round(log(sqrt(x^2) + 1) - 0.499999999) / 10^9 * 10^9 +1 }) + 0.499999999) / 10^9) * 10^9 |
