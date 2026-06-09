### Optical Spectrum

The SDSS spectrum of PGC1818175 is stored in pgc1818175-spec-2231-53816-0422.fits, which follows the naming convention: 

[object name]-spec-[plate]-[MJD]-[fiber].fits

The 'flux' column is in 10<sup>-17</sup> erg/s/cm<sup>2</sup>/&angst;, the 'ivar
' column stores the inverse variance for the same, and the 'loglam' column store
s the wavelengths in log<sub>10</sub>(&lambda;/&angst;).

An example of reading in these data is below:

```python
from astropy.io import fits
import numpy as np

spec = fits.open('pgc1818175-spec-2231-53816-0422.fits')

flux = spec[1].data['flux']*1e-17
wave = 10**spec[1].data['loglam']
err = 1e-17/np.sqrt(spec[1].data['ivar'])
```

Each file corresponds to an independent specObjID:

7450251314179889152 -- ugc7827-spec-6617-56365-0624

7471477386187659264 -- ugc7827-spec-6636-56367-0020

7470471882854389760 -- ugc7827-spec-6635-56370-0458


### Ground-based Imaging

PGC1818175_data.pkl includes the cropped image(s), mask(s), RMS image(s), and PSF(s) used in fitting the galaxy's integrated photometry, alongside the best fit model for both a single Sérsic and double Sérsic fit. 

To open:

```python
import pickle

with open('PGC1818175_data.pkl', 'rb') as pkl:
    datdict = pickle.load(pkl)
```

The keys of `datdict` are then `img`, `mask`, `rms`, `psf`, `single_model`, and `double_model`. Each entry is then a dictionary with keys `g`, `r`, and `z` to access the data and models filter-by-filter.