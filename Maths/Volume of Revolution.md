### Volume of Revolution in Mathematics

Volume of Revolution refers to the volume of a three-dimensional solid formed by rotating a two-dimensional shape around an axis. This concept is often used in calculus, particularly when calculating volumes using integration.

To understand this better, consider a simple example: imagine you have a semicircle defined by the function \( y = \sqrt{r^2 - x^2} \) from \( x = -r \) to \( x = r \). If you rotate this semicircle around the x-axis, it forms a solid sphere of radius \( r \).

The volume \( V \) of this sphere can be found using the disk method. Each thin circular cross-section (disk) perpendicular to the axis of rotation has a radius equal to the function's value at that point and an infinitesimally small thickness \( dx \). The area of each disk is \( A(x) = \pi y^2 \), which in this case is \( A(x) = \pi (r^2 - x^2) \).

The volume of the solid is then given by integrating these disks from one end to the other:

\[ V = \int_{-r}^{r} A(x) \, dx = \int_{-r}^{r} \pi (r^2 - x^2) \, dx \]

Evaluating this integral gives us the volume of the sphere:

\[ V = \pi [ r^2x - \frac{x^3}{3}]_{-r}^{r} = \pi [(r^3 - \frac{r^3}{3}) - (-r^3 + \frac{r^3}{3})] = \pi (\frac{2r^3}{3} + \frac{2r^3}{3}) = \frac{4\pi r^3}{3} \]

This is the well-known formula for the volume of a sphere.

#Volume of Revolution #Maths