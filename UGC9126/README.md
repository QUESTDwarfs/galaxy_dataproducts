### Optical Spectrum

ugc9126_imacsf4.txt contains the co-added 1D IMACS f/4 longslit spectrum of UGC 9126 oriented along the galaxy's major axis.

ugc9126minor_imacsf4.txt contains the co-added 1D IMACS f/4 longslit spectrum oriented along UGC 9126's minor axis.

Columns are flux (erg/s/cm<sup>2</sup>/&angst;), err (erg/s/cm<sup>2</sup>/&angst;), and wave (&angst;). 

An easy way to load these spectra is:

```python
import numpy as np

spec = np.loadtxt('ugc9126_imacsf4.txt')

flux = spec[:, 0]
err = spec[:, 1]
wave = spec[:, 2]


specbm= np.loadtxt('ugc9126minor_imacsf4.txt')

fluxbm= specm[:, 0]
errm = specm[:, 1]
wavem = specm[:, 2]
```
