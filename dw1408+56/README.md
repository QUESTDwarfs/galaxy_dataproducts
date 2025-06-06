### Optical Spectrum

dw1408+56_1d.txt contains the co-added 1D spectrum from MMT/Binospec.

Columns in dw1408+56_1d.txt are flux (erg/s/cm<sup>2</sup>/&angst;), err (erg/s/cm<sup>2</sup>/&angst;), and wave (&angst;).

An easy way to load this spectrum is:

```python
import numpy as np

spec = np.loadtxt('dw1408+56_1d.txt')

flux = spec[:, 0]
err = spec[:, 1]
wave = spec[:, 2]
```

