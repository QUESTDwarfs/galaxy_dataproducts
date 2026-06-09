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

leg26_lris_center.txt contains the galaxy spectrum restricted just to the bright center of the galaxy in order to drive down the SNR for a cz determination. The file structure and caveats are the same as the full 1D spectrum described above.


### Ground-based Imaging

leg26_data.pkl includes the cropped image(s), mask(s), RMS image(s), and PSF(s) used in fitting the galaxy's integrated photometry, alongside the best fit model for both a single Sérsic and double Sérsic fit. 

To open:

```python
import pickle

with open('leg26_data.pkl', 'rb') as pkl:
    datdict = pickle.load(pkl)
```

The keys of `datdict` are then `img`, `mask`, `rms`, `psf`, `single_model`, and `double_model`. Each entry is then a dictionary with keys `g`, `r`, and `z` to access the data and models filter-by-filter.