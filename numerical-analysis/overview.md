# Numerical Analysis and optimization

# Lecture 1
## Def: Optimization Problem

Let $C \in R^n$ and mapping $f: C\to R \cup \{+ \infty \}$. 
Then an optimization problem (OP) is defined with: 
$$\min_{x\in C} f(x)$$

We are looking for $x^*\in C$ such that
$f(x^*)\leq f(x) \forall x \in C$

TODO: ...

## 1D case

Let $C = I = [a,b]$ with $a < b$, and $f \in C(I,R)$ ~convex and continues functions

OP: $min_{x\in I}f(x)$
### Q1: Does OP has at least one solution?

-> Yes: A continues function on a non empty compact set has at least one solution
- Conclusion: $f(x^*) = \inf_I f$ = $min_I f$

### Q2: If $f \in C^1([a,b])$ find a condition satisfied by $x^*$
- a < b
- If $x* \in (a,b)$, then $f^{'}(x^*)=0$
- If $x^* \in [a,b)$, then for $h$ with $0<h<b-x^*: x^++h \in [a,b)$
- If $x^* \in (a,b)$, then  $f^{'}(x^*)= 0$
- If $x^* = a$, then $f^{'}(x^*)\ge 0$
- If $x^* = b$ , then $f^{'}(x^*)\le 0$
- $\forall x \in I: f^{'}(x)(x-x^*) \ge 0$
### Q3: if moreover $f \in C^2([a,b])$ what can we say about $f^{'}(x^*)$ and $f^{''}(x^*)$
- If $x^* \in (a,b)$, then $f^{'}(x^*)=0$ and $f^{''}(x^*) \ge 0$
- If $x^*=a$, then $f^{'}(a) \ge 0$ and if $f^{'}(a)$, then $f^{''}(a) \ge 0$
- **Definition (Convexity):**  
$I \ne \empty$ interval, $f:I \to R \cup \{+\infty\}$, then f is *convex* iff. $\forall x,y \in I, t\in [0,1):$ 
$$f(tx+(1-t)y) \le tf(u) + (1-t)f(y)$$
- TODO: add graphic, intuitive explanation
- works also for $A_0 = \binom{x_1}{x_2}, A_2 = \binom{y_1}{y_2}$:
 $$f(tA_0) + (1-t)A_2 \le tf(A_0) + (1-t)f(A_2)$$
- **Remarks:** 
    - if $f,g$ convex, $\gamma \ge 0$, then $\gamma f + g$ is convex  
    - f, -f convex iff. f is *affine* (TODO: affine?)
- **Proposition:** $f:I \to R \cup \{+\infty\}$ be convex, $I\ne \empty$ interval, $S_f = \{u\in I: f(u) = inf_I f\}$, then $S_f$ is an interval (possibly empty)
- **Proposition:** If $f:I \to R$ is strictly convex, then $S_f = \empty$ or $S_f$ has only one element
- **Corollary:** If $S_f \ne \empty, f$ strictly convex, then $S_f = \{x^*\}$   
$\exists!$ $x^* \in I$ such that $f(x^*) \le f(x) \forall \in I$  
i.e. $x^*$ is the unique solution of the (OP): $min_{x\in I} f(x)$
### Q4 Find a condition on f so that $S_f \ne \empty$ 
- example (1): $f(x) = e^x$  
$\inf f = 0 < f => S_f = \empty$ 
- example (2): $f:(0,1) \to R, f(x) = x$  
- **Definition (coercive):** $f:I \to R$ is *coercive*  
if $f(x) \to +\infty$ whenever $|x| \to +\infty$  or $d(x, \delta I) \to 0$  (x goes to the edge of the interval)  
(TODO: add image that explains the situation)
- **Proposition:** If $f \in C(I,R), I \ne \empty$ and $f$ coercive then $S_f \ne \empty$

### Convexity in 1D
- **Property:** If $I \ne \empty$ interval, $f,g:I \to R$ convex and $\gamma > 0$, then $\gamma f + g$ is convex.  
Moreover if $f,g$ strictly convex $\gamma f + g$ is strictly convex too.
- **Propostion:** if $f:I \ne \empty \to R$ is differentiable the following properties are equivalent:
    a) $f$ is convex
    b) $f^{'}$ is non decreasing
    c) $\forall x_0, x_1 \in I f(x_1) \ge f(x_0)$ + f'(x_0)(x_1 - x_0)$ (Taylor Theorem)
- **Property:** If moreover $f' > 0$ is increasing f is strictly convex.
- **Propostion:** If f is twice differentiable. f is convexe iff. $f'' \ge 0$.  
Moreover $f'' > 0$, then f is strictly convex.  
But if f is strictly convex, then $f''>0$ *isn't* true in general. Example: $f(x)=x^4$ is strictly convex, but $f''(0) = 0$.
- **Definition ($\alpha$-convex):** Let $f:I \ne \empty \to R$ and $\alpha > 0$ f is said to be $\alpha$-convex if $\forall x_1,x_2 \in I, \forall t \in [0,1]$: 
$$f(x_t) \le (1-t)f(x_0) + tf(x_1) - t(1-t)\alpha(x_1 - x_2)^2$$
- **Proposition:** f is $\alpha$-convex => f strictly convex => f convex
- **Proposition:** Let $f:T \to R$ and $\bar{x} \in R$:   
$f$ is  $\alpha$-convex <=> $x \to f(x) - \frac{\alpha}{2}|x-\bar{x}|^2$ is convex
($\frac{\alpha}{2}|x-\bar{x}|^2$ means concave by $alpha$)
- **Proposition:** $f \in C'(I,R)$: f is $\alpha$-convex <=> $(f'(y)-f'(x))(y-x) \ge 0$




