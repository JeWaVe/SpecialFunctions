
# SpecialFunctions

A minimal C# library providing numerical implementations of common special functions, such as:



### Airy Functions
- `airy(z: Complex)`
- `airy(z: double)`
- `airy(k: int, z: Complex)`
- `airy(k: int, z: double)`

---

### Bessel Functions (First, Second, Modified, Hankel)
- `besselj(n: double, z: Complex)`
- `besselj(n: double, z: double)`
- `bessely(n: double, z: Complex)`
- `bessely(n: double, z: double)`
- `besseli(n: double, z: Complex)`
- `besseli(n: double, z: double)`
- `besselk(n: double, z: Complex)`
- `besselk(n: double, z: double)`
- `besselh(n: double, z: Complex)`
- `besselh(n: double, k: int, z: Complex)`

---

### Spherical Bessel Functions
- `sbesselj(n: double, z: Complex)`
- `sbesselj(n: double, z: double)`
- `sbessely(n: double, z: Complex)`
- `sbessely(n: double, z: double)`
- `sbesselh(n: double, z: Complex)`
- `sbesselh(n: double, k: int, z: Complex)`

---

### Beta and Log-Beta
- `beta(z: double, w: double)`
- `betaln(z: double, w: double)`

---

### Error Functions
- `erf(x: double)`
- `erfc(x: double)`
- `erfinv(z: double)`
- `erfcinv(z: double)`

---

### Legendre Functions
- `legendre0(n: int, x: double)`  
- `legendre(n: int, x: double)`

### Gamma Functions
- `gammaln(x: double)`
- `gamma(x: double)`

The package utilizes core numerical routines from [Math.NET Numerics](https://github.com/mathnet/mathnet-numerics), with updated APIs for functions such as Bessel and error functions. It also includes Legendre polynomial implementations adapted from [AminKH's Legendre Polynomials repository](https://github.com/AminKH/Legendre-Polynomials). The API is designed to closely mirror MATLAB’s structure and naming conventions, enabling a smooth transition for users familiar with MATLAB syntax. This compatibility facilitates rapid prototyping, intuitive function calls, and straightforward adaptation of existing MATLAB-based codebases to C#.

## Usage

```csharp
using static SpecialFunctions.SF;
using System.Numerics;

double result = erf(1.0);
Complex bessel = besselj(1.5, new Complex(1.0, 0.5));

```

For detailed functionalities, please visit the [manual page](./docs/MANUAL.md).

## Notes

- Most functions are overloaded for both real (`double`) and complex (`System.Numerics.Complex`) inputs.
- Many implementations delegate to the `Amos` library for accurate numerical evaluation.
- Ensure input values are valid to avoid `NaN` results.

## License

MIT License.
