# Provenance / Kaynak kaydı

## Application and documentation

The source repository was read privately to verify the modern recorder, packaging documentation and original license. No application source files or source snippets are included in this public showcase.

- Verified source revision: `6c69577c459e1a2229a353397f0f7175c3eb1f16`.
- Recorded application release: `0.1.1`.
- Capability evidence: modern-recorder section of the source README and its 25 September 2026 methodology note.
- Historical test evidence: the methodology note reports 14 local passing tests and synthetic-recording package checks. This preparation did not rerun them or acquire physical data.

## Screenshot capture

`assets/web-recorder-tr.png` and `assets/web-recorder-en.png` were captured on 2 October 2026 using Playwright CLI with installed Google Chrome, serving the genuine source web recorder on a temporary localhost-only server. Viewport: 1440 × 1050 CSS pixels. Only page content is captured.

The Turkish view uses the application's language selector. The English view uses its default English language state. The interface was not restyled, recreated, translated externally or populated with synthetic measurements. No microphone permission, detector connection or recording start was performed. The empty waveform and zero counts are idle defaults. The only browser console error observed was a missing `favicon.ico` (HTTP 404).

These are **web recorder** screenshots, not desktop application screenshots. Some calibration labels remain Turkish in the English view. Actual device acquisition, desktop startup, export, calibration and physical detector performance were not tested in this capture.

## Artwork and attribution

`assets/icon.png` is the existing recorder artwork from the repository's packaging assets. No generated application mockups, hardware photographs or upstream scientific plots were substituted for screenshots.

The hardware invention, underlying scientific method and inherited research materials belong to Oliver Keller and collaborators' [upstream project](https://github.com/ozel/DIY_particle_detector). See the original publication: [Sensors 2019, 19(19), 4264](https://doi.org/10.3390/s19194264).

The upstream BSD-2-Clause license is retained verbatim in [LICENSE](LICENSE), including `Copyright (c) 2019, Oliver Keller`. Keeping current application source private does not remove rights granted by that license. Hardware is separately covered by CERN Open Hardware License; hardware files and scientific datasets are not distributed in this repository.

## Release distribution

The public release destination is [particle-detector-showcase v0.1.1](https://github.com/Mahmutakin99/project-portfolio/releases/tag/particle-detector-v0.1.1). The intended packages are the already published v0.1.1 files, moved without modification. Package migration, availability and hash verification are separate from screenshot preparation; screenshots are not evidence of native package behavior on any target system.
