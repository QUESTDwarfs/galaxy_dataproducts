### Optical Spectrum

pgc4143_imacsf4.txt contains the co-added 1D IMACS f/4 longslit spectrum of PGC 4143.

Columns are flux (erg/s/cm<sup>2</sup>/&angst;), err (erg/s/cm<sup>2</sup>/&angst;), and wave (&angst;). 

An easy way to load these spectra is:

```python
import numpy as np

spec = np.loadtxt('pgc4143_imacsf4.txt')

flux = spec[:, 0]
err = spec[:, 1]
wave = spec[:, 2]
```
