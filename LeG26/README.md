### Optical Spectrum

leg26_lris.txt contains the co-added 1D Keck/LRIS spectrum of LeG 26. Note that the flux calibration is very uncertain below ~5600 &angst;.

Columns are flux (erg/s/cm<sup>2</sup>/&angst;), err (erg/s/cm<sup>2</sup>/&angst;), and wave (&angst;). 

An easy way to load these spectra is:

```python
import numpy as np

spec = np.loadtxt('leg26_lris.txt')

flux = spec[:, 0]
err = spec[:, 1]
wave = spec[:, 2]
```
