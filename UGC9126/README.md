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


### Ground-based Imaging

UGC9126_data.pkl includes the cropped image(s), mask(s), RMS image(s), and PSF(s) used in fitting the galaxy's integrated photometry, alongside the best fit model for both a single Sérsic and double Sérsic fit. 

To open:

```python
import pickle

with open('UGC9126_data.pkl', 'rb') as pkl:
    datdict = pickle.load(pkl)
```

The keys of `datdict` are then `img`, `mask`, `rms`, `psf`, `single_model`, and `double_model`. Each entry is then a dictionary with keys `g`, `r`, and `z` to access the data and models filter-by-filter.