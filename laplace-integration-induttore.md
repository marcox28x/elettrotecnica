## Deriving the Differentiation Property of Laplace Transform

**Goal:** Find 

$\mathcal{L} \lbrace \frac{df}{dt} \rbrace = \int_{0}^{\infty} \frac{df}{dt} e^{-st} dt $
### Step 1: Set up Integration by Parts
For integration by parts: $$\int u \, dv = uv - \int v \, du$$

Choose:
- $$u = e^{-st}$$ 
- $$dv = \frac{df}{dt} dt = df$$

Therefore:
- $$du = -se^{-st} dt$$
- $$v = f(t)$$

### Step 2: Apply Integration by Parts
$$\int_0^{\infty} \frac{df}{dt} e^{-st} dt = \left[f(t)e^{-st}\right]_0^{\infty} - \int_0^{\infty} f(t)(-se^{-st}) dt$$

$$= \left[f(t)e^{-st}\right]_0^{\infty} + s\int_0^{\infty} f(t)e^{-st} dt$$

### Step 3: Evaluate the Boundary Terms

$f(t)e^{-st}  0^{ \infty } = \lim_{t \to \infty} f(t)e^{-st} - f(0^-)e^{0} $

For convergence, we assume $$\lim_{t \to \infty} f(t)e^{-st} = 0$$

Therefore:
$$\left[f(t)e^{-st}\right]_0^{\infty} = 0 - f(0^-) = -f(0^-)$$

### Step 4: Final Result
$$\mathcal{L}\left \lbrace \frac{df}{dt}\right \rbrace = -f(0^-) + s\int_0^{\infty} f(t)e^{-st} dt$$

Since $$\int_0^{\infty} f(t)e^{-st} dt = F(s)$$:

$$\boxed{\mathcal{L}\left\{\frac{df}{dt}\right\} = sF(s) - f(0^-)}$$

The negative sign comes from evaluating the boundary term $$[f(t)e^{-st}]$$ at the lower limit $$t = 0^-$$.
