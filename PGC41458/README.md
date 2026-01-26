### Optical Spectrum

pgc41458_imacsf4.txt contains the co-added 1D IMACS f/4 longslit spectrum of PGC 41458.

pgc41458b_imacsf4.txt contains the co-added 1D IMACS f/4 longslit spectrum of PGC 41458's smaller satellite, which we refer to as PGC 41458b.

Columns are flux (erg/s/cm<sup>2</sup>/&angst;), err (erg/s/cm<sup>2</sup>/&angst;), and wave (&angst;). 

An easy way to load these spectra is:

```python
import numpy as np

spec = np.loadtxt('pgc41458_imacsf4.txt')

flux = spec[:, 0]
err = spec[:, 1]
wave = spec[:, 2]


specb = np.loadtxt('pgc41458b_imacsf4.txt')

fluxb = specb[:, 0]
errb = specb[:, 1]
waveb = specb[:, 2]
```
