### Optical Spectrum

UGC4527_1d.txt contains the co-added 1D spectrum from MMT/Binospec. 

Columns in UGC4527_1d.txt are flux (erg/s/cm<sup>2</sup>/&angst;), err (erg/s/cm<sup>2</sup>/&angst;), and wave (&angst;).

An easy way to load this spectrum is:

```python
import numpy as np

spec = np.loadtxt('UGC4527_1d.txt')

flux = spec[:, 0]
err = spec[:, 1]
wave = spec[:, 2]
```

### Ground-based Imaging

UGC4527_data.pkl includes the cropped image(s), mask(s), RMS image(s), and PSF(s) used in fitting the galaxy's integrated photometry, alongside the best fit model for both a single Sérsic and double Sérsic fit. 

To open:

```python
import pickle

with open('UGC4527_data.pkl', 'rb') as pkl:
    datdict = pickle.load(pkl)
```

The keys of `datdict` are then `img`, `mask`, `rms`, `psf`, `single_model`, and `double_model`. Each entry is then a dictionary with keys `g`, `r`, and `z` to access the data and models filter-by-filter.