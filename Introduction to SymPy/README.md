This mini-project demonstrates how to use SymPy, a Python library for symbolic mathematics. Tasks include basic calculations, symbolic equations, simplification, and expansion of algebraic expressions.

##  Task #1: Include All Necessary SymPy Modules

**Purpose:**
Import SymPy functions for symbolic math, such as working with algebraic expressions, equations, and formatting outputs.

**Syntax Used:**

* `from sympy import symbols, Rational, sqrt, simplify, expand, Eq, pprint, init_printing`
* `init_printing(use_unicode=True)` — enables pretty textbook-style formatting of outputs.

---

##  Task #2: Basic Calculations

###  Expression 1:

Compute the sum of a rational number and a square root:

$$
\frac{5}{3} + \frac{\sqrt{10}}{2}
$$

**Output:**

$$
\frac{\sqrt{10}}{2} + \frac{5}{3}
$$

**Syntax Used:**

* `Rational(5, 3)`
* `sqrt(10)`
* `pprint(expression)`

---

###  Expression 2:

Multiply two square roots and divide by a constant:

$$
\frac{\sqrt{50} \cdot \sqrt{5}}{9} = \frac{5\sqrt{10}}{9}
$$

**Output:**

$$
\frac{5\sqrt{10}}{9}
$$

**Syntax Used:**

* `sqrt(50) * sqrt(5) / 9`
* `pprint(expression)`

---

##  Task #3: Symbols and Equations

###  Equation 1:

Define an equation using symbols:

$$
2x + 3y = 12
$$

###  Equation 2:

Another symbolic equation:

$$
x - y = 4
$$

**Syntax Used:**

* `symbols('x y')` — define symbolic variables
* `Eq(left, right)` — create an equation
* `pprint(equation)` — pretty print

---

##  Task #4: Simplification

###  Expression 1:

Simplify a rational expression:

$$
\frac{x^2 + 2x + 1}{x + 1} = x + 1
$$

###  Expression 2:

Simplify a nested expression:

$$
\frac{1 - \frac{1}{1 + \frac{1}{x}}}{1 + \frac{1}{x}} = \frac{x}{(x + 1)^2}
$$

**Syntax Used:**

* `simplify(expression)`
* `symbols('x')`
* `pprint(result)`

---

##  Task #5: Expansion

###  Expression 1:

Expand a squared binomial:

$$
(2x + 2)^2 = 4x^2 + 8x + 4
$$

###  Expression 2:

Expand the product of two binomials:

$$
(2x + y)(x - 2y) = 2x^2 - 3xy - 2y^2
$$

**Syntax Used:**

* `expand(expression)`
* `symbols('x y')`
* `pprint(result)`

