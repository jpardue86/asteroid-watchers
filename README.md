# Real SPHEREx observations: 3I/ATLAS

This package contains two calibrated SPHEREx spectral-image cutouts downloaded from NASA/IPAC IRSA. Open **index.html** to inspect the two epochs locally. The self-contained viewer uses local previews and needs no password or API key. To make it public, publish this folder through a static web host such as GitHub Pages.

## Contents

- Two original, unmodified FITS cutouts (QR2, detector D6), observed 2025-08-01 and 2025-12-14.
- Two PNG visualizations generated from the FITS IMAGE extension. These are scientific-data display conversions, not AI-generated images.
- manifest.json: observation IDs, exposure times, coordinates, archive URLs, display transform and SHA-256 checksums.
- IRSA-3I-ATLAS-observations.vot: the official 259-row observation list used to select the files. It lists candidate observation coverage, not newly confirmed detections by this project.

## Interpretation limits

3I/ATLAS is a comet, not one of the asteroids in the existing NeoWs database. These cutouts follow its predicted position at different sky locations. They do not show the same fixed sky field, and this viewer does not establish an independent detection or measure motion. The data have low signal-to-noise at many wavelengths. Bright pixels may be stars, noise, artifacts, or comet emission; the viewer does not identify them automatically.

QR2 is a legacy calibration release. IRSA states that DR1/QR3 supersede it. These specific QR2 files remain available through February 2027 according to the November 2026 archive documentation. Use current releases for subsequent research when available. Shared grayscale scaling alone does not justify quantitative brightness or composition comparisons: local wavelength, WCS, PSF, masks, background, and calibration need validation. FLAGS, VARIANCE, ZODI and PSF extensions remain in the FITS files. The PNGs do not apply a science-quality mask or subtract the zodiacal background.

This download establishes real SPHEREx data access. It does not add these images to Supabase, deploy a public website, or make the existing asteroid monitor a SPHEREx detection system.

## Sources

- https://irsa.ipac.caltech.edu/data/SPHEREx/docs/comet3iatlas/index.html
- https://irsa.ipac.caltech.edu/spherex-archive-documentation/spherex-data-access/
- https://irsa.ipac.caltech.edu/ibe/cutouts.html

Data credit: NASA SPHEREx and Caltech/IPAC Infrared Science Archive (IRSA). Retain these source links with reused data. For formal publication follow the archive's acknowledgment guidance.
