### Optical Spectra

Files containing the SDSS (and BOSS) spectra of UGC 7827 are stored in .fits fil
es with the following naming convention:

[name]-spec-[plate]-[MJD]-[fiber].fits

The 'flux' column is in 10<sup>-17</sup> erg/s/cm<sup>2</sup>/&angst;, the 'ivar
' column stores the inverse variance for the same, and the 'loglam' column store
s the wavelengths in log<sub>10</sub>(&lambda;/&angst;).

An example of reading in these data is below:

```python
from astropy.io import fits
import numpy as np

spec = fits.open('ugc7827-spec-6636-56367-0020.fits')

flux = spec[1].data['flux']*1e-17
wave = 10**spec[1].data['loglam']
err = 1e-17/np.sqrt(spec[1].data['ivar'])
```

Each file corresponds to an independent specObjID:

7450251314179889152 -- ugc7827-spec-6617-56365-0624

7471477386187659264 -- ugc7827-spec-6636-56367-0020

7470471882854389760 -- ugc7827-spec-6635-56370-0458
