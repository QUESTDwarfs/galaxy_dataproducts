### Optical Spectrum

ugc7485_imacsf2.txt contains the co-added 1D (red chip) IMACS f/2 longslit spectrum of UGC 7485.

Columns are flux (erg/s/cm<sup>2</sup>/&angst;), err (erg/s/cm<sup>2</sup>/&angst;), and wave (&angst;). 

An easy way to load these spectra is:

```python
import numpy as np

spec = np.loadtxt('ugc7485_imacsf2.txt')

flux = spec[:, 0]
err = spec[:, 1]
wave = spec[:, 2]
```
