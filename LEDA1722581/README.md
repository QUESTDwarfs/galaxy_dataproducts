### Optical Spectra

Files containing co-added 1D spectra from MaNGA cube for LEDA 1722581 and the H$\alpha$-identified clump (LEDA 1722581-em) to the west end in \_MaNGAspec.txt.

Columns in \_MaNGAspec.txt files are flux (erg/s/cm<sup>2</sup>/&angst;), err (erg/s/cm<sup>2</sup>/&angst;), and wave (&angst;). 

An easy way to load these spectra is:

```python
import numpy as np

spec = np.loadtxt('LEDA1722581_MaNGAspec.txt')

flux = spec[:, 0]
err = spec[:, 1]
wave = spec[:, 2]
```
