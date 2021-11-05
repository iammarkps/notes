# Integration

## Overview

Integral is not the same as **antiderivative**, they are related, but not the same. We usually defined it with Riemann sum, but I omitted in this note for the sake of simplicity.

## Definite Integral

We can define definite integral with Riemann sum, but we can also use fundamental theorem of calculus to help us compute it.

$$\int_{a}^{b} f(x) \,dx = F(b) - F(a)$$

where $F$ is any antiderivative of $f$

or we can define to show that differentiation and integration are inverse process with

$$\int_{a}^{b} F'(x) \,dx = F(b) - F(a)$$


## Indefinite Integral

Now we need a proper way in finding antiderivative called indefinite integral defined with

$$\int f(x) \,dx = F(x) + C$$ 

meaning $F'(x) = f(x)$

## Fundamental Theorem of Calculus
 
 ### Theorem 1 
$$\frac{d}{dx} \int_{a}^{x} f(t) dt = f(x)$$

### Theorem 2
$$\int_{a}^{b} f(x) \,dx = F(b) - F(a)$$

## Integration Technique

### Substitution

We change $x$ and $dx$ to $u$ and $du$ to simplify integration.

### Integration by parts

$$\int u \,dv = uv - \int v \,du$$

### Partial Fraction

When we have function defined with $f(x) = \frac{P(x)}{Q(x)}$ we can express $f$ as a sum of simpler fraction when $deg(P) < deg(Q)$

$$\frac{A_1}{(x-r)} + \frac{A_2}{(x-r)^2} + ... +\frac{A_m}{(x-r)^m}$$ 

## Application

### Finding Demand Function from marginal-revenue function

First, we define marginal revenue function with:
$$MR = \frac{dr}{dq}$$ 
Thus, $\int \frac{dr}{dq} \,dq$ yield original revenue function ($r$) with constant $C$. 

We know that when quantity is 0, revenue is also 0. So we can substitute $q$ with $0$ and $r = 0$ to find $C$.

Revenue function is defined with:

$$r = qp(q)$$

dividing $r$ with $q$ then resulted in original $p(q)$ (demand) function.

### Consumer and Producer surplus under equilibrium

![[surplus.png]]

Consumer surplus, when $q$ is equilibrium quantity, $p(q)$ is demand function and $p$ is the equilibrium price:

$$\int_{0}^{q} p(q) - p \,dq$$

Producer surplus, when $q$ is equilibrium quantity, $p(q)$ is supply function and $p$ is the equilibrium price:

$$\int_{0}^{q} p - p(q) \,dq$$

We can solve for $q$ by letting demand function equal to supply function.