### Optical Spectrum

ugca285_lris.txt contains the co-added 1D Keck/LRIS spectrum of UGCA 285. Note that the flux calibration is very uncertain below ~5600 &angst;.

Columns are flux (erg/s/cm<sup>2</sup>/&angst;), err (erg/s/cm<sup>2</sup>/&angst;), and wave (&angst;). 

An easy way to load these spectra is:

```python
import numpy as np

spec = np.loadtxt('ugca285_lris.txt')

flux = spec[:, 0]
err = spec[:, 1]
wave = spec[:, 2]
```
