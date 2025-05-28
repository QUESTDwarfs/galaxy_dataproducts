### Optical Spectra

Files containing the SDSS (and BOSS) spectra of NGC 5486 are stored in .fits files with the following naming convention:

[name]-spec-[plate]-[MJD]-[fiber].fits

The 'flux' column is in 10<sup>-17</sup> erg/s/cm<sup>2</sup>/&angst;, the 'ivar' column stores the inverse variance for the same, and the 'loglam' column stores the wavelengths in log<sub>10</sub>(&lambda;/&angst;).

An example of reading in these data is below:

```python
from astropy.io import fits
import numpy as np

spec = fits.open('ngc5486_spec-1324-53088-0491.fits')

flux = spec[1].data['flux']*1e-17
wave = 10**spec[1].data['loglam']
err = 1e-17/np.sqrt(spec[1].data['ivar'])
```

Each file corresponds to an independent specObID:

1490826493520013312 -- ngc5486_spec-1324-53088-0491

9489301150144681984 -- ngc5486_spec-8428-57837-0788

9488057877522569216 -- ngc5486_spec-8427-57846-0361

1491909507004000256 -- ngc5486-spec-1325-52762-0335
