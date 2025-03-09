### Triple Integrals

Triple integrals are an extension of double integrals to three dimensions. They are used to calculate volumes of regions in 3D space, as well as to find masses or averages over such regions when the density is not constant.

To understand triple integrals, let's start with a basic example where we calculate the volume of a rectangular box. Suppose we have a box defined by the ranges $$0 \leq x \leq a$$, $$0 \leq y \leq b$$, and $$0 \leq z \leq c$$. The volume of this box can be calculated using a triple integral:

$$ V = \int_{0}^{c}\int_{0}^{b}\int_{0}^{a} 1 \, dx \, dy \, dz $$

Here's how we evaluate it step-by-step:
1. Integrate with respect to $$x$$ from 0 to $$a$$:
$$ \int_{0}^{a} 1 \, dx = [x]_0^a = a $$
2. Substitute the result and integrate with respect to $$y$$ from 0 to $$b$$:
$$ \int_{0}^{b} a \, dy = a[y]_0^b = ab $$
3. Finally, substitute and integrate with respect to $$z$$ from 0 to $$c$$:
$$ \int_{0}^{c} ab \, dz = ab[z]_0^c = abc $$

Thus, the volume of the box is $$abc$$.

Triple integrals can also be used for more complex regions. For example, consider finding the volume of a solid bounded by the paraboloid $$z = x^2 + y^2$$ and the plane $$z = 4$$. The region in the xy-plane is defined by the circle $$x^2 + y^2 \leq 4$$.

The triple integral for this volume would be:

$$ V = \int_{-2}^{2}\int_{-\sqrt{4-x^2}}^{\sqrt{4-x^2}}\int_{0}^{x^2+y^2} dz \, dy \, dx $$

This can be simplified using polar coordinates to make the integration easier:

$$ V = \int_{0}^{2\pi}\int_{0}^{2}\int_{0}^{r^2} r \, dz \, dr \, d\theta $$

First, integrate with respect to $$z$$ from 0 to $$r^2$$:
$$ \int_{0}^{r^2} r \, dz = r[z]_0^{r^2} = r^3 $$
Next, integrate with respect to $$r$$ from 0 to 2:
$$ \int_{0}^{2} r^3 \, dr = \left[\frac{1}{4}r^4\right]_0^2 = 4 $$
Finally, integrate with respect to $$\theta$$ from 0 to $$2\pi$$:
$$ \int_{0}^{2\pi} 4 \, d\theta = 4\theta[0]^{2\pi} = 8\pi $$

Therefore, the volume of the solid is $$8\pi$$.