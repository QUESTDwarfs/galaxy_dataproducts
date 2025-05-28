#### Optical Spectra

Files containing the SDSS spectra of UGC 5427 are stored in .fits files with the following naming convention:

[name]-spec-[plate]-[MJD]-[fiber].fits

The 'flux' column is in 10<sup>-17</sup> erg/s/cm<sup>2</sup>/&angst;, the 'ivar
' column stores the inverse variance for the same, and the 'loglam' column store
s the wavelengths in log<sub>10</sub>(&lambda;/&angst;).

An example of reading in these data is below:

```python
from astropy.io import fits
import numpy as np

spec = fits.open('ugc5427_spec-1950-53436-0047.fits')

flux = spec[1].data['flux']*1e-17
wave = 10**spec[1].data['loglam']
err = 1e-17/np.sqrt(spec[1].data['ivar'])
```

Each file corresponds to an independent specObjID:

2195517795251283968 -- ugc5427_spec-1950-53436-0047
12779137532475758592 -- ugc5427-spec-11350-58455-0631
7283574696637126656 -- ugc5427-spec-6469-56328-0466
