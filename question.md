**Final Practice 3 Rephrased.** Suppose $f\in\mathcal M(\mathbb R)$ is such that $\hat f\in C^0(\mathbb R)$ and, for some $\alpha\in(0,1)$ and $C>0$, that $|\hat f(\xi)|\le\dfrac{C}{|\xi|^{1+\alpha}}$ for all $|\xi|\ge1$. Show that for some $M>0$, $|f(x+h)-f(x)| \le M|h|^\alpha$ for all $x,h\in\mathbb R$. 

**Question 1.** Would you consider this question sufficiently challenging to warrant a hint such as "split the integral near $|\xi h|=1$," if this had been an exam question?

**Question 2.** Is the value 1 in the exercise statement significant? That is, could one attempt as follows without reference to that 1?

---

*Attempt.* Because Fubini's theorem continues to apply due to absolute integrability, the argument from class for Fourier inversion holds for $f$ as well; that is, $f=\mathcal F^{-1}\{\hat f\}$. Let $A=\max\{C,1+\displaystyle\max_{\xi\in[-1,1]} |\xi^{1+\alpha}\cdot\hat f(\xi)|\}>0$, so $|\hat f(\xi)|\le\dfrac{A}{|\xi|^{1+\alpha}}$ for all $\xi\in\mathbb R$.
>
Suppose $h\ne0$. Any arc on the circle is as long as its chord, so
```math
\begin{aligned}\int_{|\xi h|\le 1}|\hat f(\xi)|\cdot\left(|\mathrm e^{2\pi\mathrm i \xi h}-1| \le 2\pi|\xi h|\right)\,\mathrm d\xi &\le 2\pi A|h|\int_{-1/|h|}^{1/|h|}\frac{\mathrm d\xi}{|\xi|^{\alpha}}=2\pi A|h|\cdot\frac2{1-\alpha}\xi^{1-\alpha}\bigg|_{\xi=0}^{1/|h|}=\frac{4\pi A}{1-\alpha}|h|^\alpha.\end{aligned}`
```
Meanwhile, two points on the unit circle are apart by at most the diameter 2, so
```math
\begin{aligned}\int_{|\xi h|\ge 1}|\hat f(\xi)|\cdot|\mathrm e^{2\pi\mathrm i \xi h}-1|\,\mathrm d\xi\le4A\int_{1/|h|}^\infty\frac{\mathrm d\xi}{\xi^{1+\alpha}}=-\frac{4A}{\alpha}\xi^{-\alpha}\bigg|_{\xi=1/|h|}^\infty=\frac{4A}{\alpha}|h|^\alpha.\end{aligned}
```
Thus,
```math
\begin{aligned}|f(x+h)-f(x)|\le\int_{|\xi h|\le 1}|\hat f(\xi)\cdot\mathrm e^{2\pi \mathrm i\xi x}\cdot\left(\mathrm e^{2\pi\mathrm i \xi h}-1\right)|\,\mathrm d\xi\end{aligned}\le\left(\frac{4\pi A}{1-\alpha}+\frac{4A}{\alpha}\right)|h|^\alpha.
```
This is also true, of course, when $h=0$. $\quad\square$

---

**Question 3.** If the above attempt is correct, could you explain the significance of the "1" referenced in Question 2?
