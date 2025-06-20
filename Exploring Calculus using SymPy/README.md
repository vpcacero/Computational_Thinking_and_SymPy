This notebook introduces key symbolic math concepts using the **SymPy** library in Python. It includes playing with algebraic expressions, limits, derivatives, series expansions, and solving equations all done programmatically.

##  Task 1: Playing with Symbols

###  Code:
x = symbols('x')  
x + x


**What it means:**
We define `x` as a symbolic variable. When we compute `x + x`, we’re adding the same variable to itself.

** Result:**

$$
x + x = 2x
$$

---

##  Task 2: Multiply a Symbol by Itself

###  Code:
x * x


**What it means:**
We multiply a variable by itself. This gives us:

** Result:**

$$
x \cdot x = x^2
$$

---

##  Task 3: Exploring Limits

###  Code:
limit(sin(x)/x, x, 0)

**What it means:**
We calculate the limit of $\frac{\sin(x)}{x}$ as $x$ approaches 0 — a famous limit in calculus.

** Result:**

$$
\lim_{x \to 0} \frac{\sin(x)}{x} = 1
$$

---

##  Task 4: Derivatives

###  Code:
diff(x**2, x)

**What it means:**
We take the derivative of $x^2$ with respect to $x$.

** Result:**

$$
\frac{d}{dx}(x^2) = 2x
$$

---

##  Task 5: Series Expansion

###  Code:
exp(x).series(x, 0, 4)

**What it means:**
We expand the exponential function $e^x$ around $x = 0$ up to the $x^3$ term.

** Output:**

$$
1 + x + \frac{x^2}{2} + \frac{x^3}{6} + \mathcal{O}(x^4)
$$

**Interpretation:**
This is the **Maclaurin series** for $e^x$. It shows the first **4 terms** before the remainder term $\mathcal{O}(x^4)$.

---

##  Task 6: Solving Equations

###  Code:
solve(Eq(x**2 - 4, 0), x)

**What it means:**
We solve the quadratic equation $x^2 - 4 = 0$.

** Result:**

$$
x = -2 \quad \text{or} \quad x = 2
$$

**Type of Problem:**
This is a **quadratic equation** — a second-degree polynomial that has two real roots.

---

##  Tools Used

* `symbols()` — defines variables
* `diff()` — finds derivatives
* `limit()` — computes limits
* `series()` — expands functions into power series
* `solve()` and `Eq()` — solve equations symbolically
