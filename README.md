import scipy.integrate as spi
def integrand(y, x):
    return x**2 + y**2

volume, error = spi.dblquad(integrand, 0, 1, lambda x: 0, lambda x: 1)
print(f"Volume under the surface z = x² + y²: {volume:.4f}")
