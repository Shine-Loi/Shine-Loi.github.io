---
title:  "[Python-Algebra] Chapter 1. Solution of Equations"
excerpt: ""

categories:
  - Python-Algebra
tags:
  - [Python, Algebra]

toc: true
toc_sticky: true
 
date: 2024-07-02
last_modified_at: 2024-07-02
---

&nbsp;

# 1. Sympy Module
The sympy module provides funcions for algebraic operations, solving equations, matrix operations, and more. In the example code below, I used the sympy module to set 'x' as an unknown and to solve equations.

&nbsp;

&nbsp;

&nbsp;

# 2. Example codes
## 2-1. Solution of Equations
**(Ex 1) Solve the equation \\(3x+7=-2\\).**

&nbsp;

At first, I defined the unknown 'x' with the function 'symbols()'. The unknowns generated by the 'symbols()' function can be used in operations performed in the sympy module. And then, substitute the expression into the variable 'exp'. Make sure to write the expression in the form '\\((expression)=0\\)' by moving all terms to one side. You don't need to simplify the expression; Python will do it automatically. Finally, the equation will be solved automatically by the 'solve()' function. In the case of multiple solutions, the 'solve()' function stores the solutions as a list. In (Ex 1), There is only one solution, so just print the first solution with the 'solutoin[0]' command.

&nbsp;

```python
import sympy as sym

x=sym.symbols('x')

exp=3*x+7+2

solution=sym.solve(exp)
print("x =", solution[0])
```

&nbsp;

| Output |
|---|
| x=-3 |

&nbsp;

## 2-2. The 'latex()' Function
**(Ex 2) Solve the equation \\(7x-23=72\\).**

&nbsp;

```python
import sympy as sym

x=sym.symbols("x")
exp=7*x-23-72
solution=sym.solve(exp)
print("x =", solution[0])
```

&nbsp;

| Output |
|---|
| x=95/7 |

&nbsp;

I used the same method as in (Ex 1) to solve (Ex 2). However, the solution of (Ex 2) is in the form of a fraction. So I used the IPython.display module to format the solution with LaTex. Use the 'Math()' function inside the 'display()' function. This allows you to print fractions neatly using the 'latex()' functoin as shown below.

&nbsp;

```python
import sympy as sym
from IPython.display import display, Math

x=sym.symbols("x")
exp=7*x-23-72
solution=sym.solve(exp)
display(Math("\\text{x = } %s" %sym.latex(solution[0])))
```

&nbsp;

**Output**\\
\\(\displaystyle x= \frac{95}{7}\\)

&nbsp;

## 2-3. Equations with Multiple Solutions
**(Ex 3) Solve the equation \\(\displaystyle x^2 =9\\).**

&nbsp;

```python
import sympy as sym

x=sym.symbols("x")
exp=x**2-9
solution=sym.solve(exp)
for i in range(0,len(solution)):
    print("x =", solution[i])
```

&nbsp;

| Output |
|---|
| x=-3 |
| x=3 |

&nbsp;

I also used the same method as in (Ex 1) to solve (Ex 3). However, (Ex 3) has multiple solutions, so I used a 'for' statement to print all solutions.

&nbsp;

## 2-4. Equations with Imaginary solutions
**(Ex 4) Solve the equation \\(\displaystyle -2(x^2 -12)=110\\).**

&nbsp;

```python
import sympy as sym

x=sym.symbols("x")
exp=-2*(x**2-12)-110
solution=sym.solve(exp)
for i in range(0,len(solution)):
    print("x =", solution[i])
```

&nbsp;

| Output |
|---|
| x=-sqrt(43)*I |
| x=sqrt(43)*I |

&nbsp;

(Ex 4) has imaginary solutions. The 'I' in the output represents an imaginary number. You can also use the 'latex()' function as in (Ex 2).

&nbsp;

```python
import sympy as sym
from IPython.display import display, Math

x=sym.symbols("x")
exp=-2*(x**2-12)-110
solution=sym.solve(exp)
for i in range(0,len(solution)):
    display(Math("\\text{x = } %s" %sym.latex(solution[i])))
```

&nbsp;

**Output**\\
\\(\displaystyle x=-\sqrt{43} i\\)\\
\\(\displaystyle x=\sqrt{43} i\\)