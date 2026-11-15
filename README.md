# Asteroid Watchers

[Public SPHEREx viewer](https://jpardue86.github.io/asteroid-watchers/) · [Six-slide project demonstration](Asteroid-Watch-Connected-Story.pptx)

## Project

Asteroid Watch preserves space data for future research through two separate working components:

- A public SPHEREx viewer showing two real infrared observations of comet 3I/ATLAS, with dates, coordinates, original FITS files and provenance metadata.
- A NASA NeoWs catalogue archive in Supabase with dated asteroid snapshots, reviewed AI summaries, and an ESP32 / Uno R3 / LCD status display.

The historical record is central: source inputs, retrieval dates, model and prompt versions, and review decisions remain available for inspection. Linking SPHEREx images to the cloud database is future work. The AI currently summarizes catalogue data, not SPHEREx image pixels.

This repository contains the SPHEREx viewer, data sample, credits, and presentation. It does not contain privileged cloud credentials or a complete export of the deployed NeoWs backend.

## Super Intelligence / AI-use acknowledgment

OpenAI Codex and ChatGPT assisted with ideation, source research, code generation, debugging, interpretation, writing, interface design, and presentation preparation. The OpenAI API generates the catalogue summaries stored by the cloud prototype; summaries start unreviewed and require human checks. Code and explanatory text were developed with this assistance.

NASA observational data were downloaded from IRSA and were not AI-generated. Preview PNGs are deterministic visualizations of FITS IMAGE arrays, not generative imagery. Hardware photographs were supplied by the participant. No AI-generated voice or video is included. Model-generated catalogue summaries are derived text, not new astronomical measurements.

## Development resources

- [NASA NeoWs](https://api.nasa.gov/)
- [NASA CNEOS PHA definitions](https://cneos.jpl.nasa.gov/about/neo_groups.html)
- [Supabase](https://supabase.com/docs)
- [OpenAI API](https://developers.openai.com/)
- [Arduino](https://docs.arduino.cc/)
- [Espressif Arduino-ESP32](https://docs.espressif.com/projects/arduino-esp32/en/latest/)
- [ArduinoJson by Benoit Blanchon](https://arduinojson.org/)
- [hd44780 by Bill Perry](https://github.com/duinoWitchery/hd44780)
- [Python](https://www.python.org/), [NumPy](https://numpy.org/), [Pillow](https://python-pillow.org/)
- [GitHub Pages](https://docs.github.com/en/pages)

## Scope

The public viewer is a limited two-epoch case study, not arbitrary sky search, registered fixed-field image comparison, or automated discovery. The comet views cover different sky coordinates. PHA classification alone does not establish impact probability. Future satellite networks, tracking models and debris-sampling missions are research concepts, with no NASA partnership or immediate operational capability claimed.

---

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

This viewer establishes real SPHEREx data access. It is publicly deployed through GitHub Pages. The SPHEREx images remain separate from Supabase and the NeoWs catalogue pipeline; the prototype does not claim image-based discovery or impact prediction.

## Sources

- https://irsa.ipac.caltech.edu/data/SPHEREx/docs/comet3iatlas/index.html
- https://irsa.ipac.caltech.edu/spherex-archive-documentation/spherex-data-access/
- https://irsa.ipac.caltech.edu/ibe/cutouts.html

Data credit: NASA SPHEREx and Caltech/IPAC Infrared Science Archive (IRSA). Retain these source links with reused data. For formal publication follow the archive's acknowledgment guidance.
