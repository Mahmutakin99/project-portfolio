# DIY Particle Detector — Desktop & Web Recorder

<img src="../assets/case-studies/particle-detector/icon.png" alt="Original particle detector recorder application icon" width="110">

A bilingual recording and analysis interface for audio-based DIY particle detectors, connecting acquisition, live visualization, portable recordings, and later inspection.

**Stage:** packaged software; physical measurement performance is hardware-dependent. **Source:** private.

## Problem

An educational detector can produce pulses through an audio input, but students and makers still need a practical way to capture those signals, inspect count rates, preserve measurements, and compare recordings across computers.

## Contribution and attribution

This case focuses on the desktop/web software adaptation and packaging. The underlying DIY Particle Detector hardware, scientific method, and inherited research materials originate from [Oliver Keller and collaborators' project](https://github.com/ozel/DIY_particle_detector). Their hardware invention, publication, and original reference measurements are not claimed as original work here.

## Measurement workflow

1. Choose an electron/beta or alpha profile, input device, and threshold.
2. Start acquisition and inspect waveform, pulse amplitude, and count rate.
3. Stop and save a versioned recording with session metadata.
4. Reopen recordings and inspect the pulse-amplitude histogram.
5. Supply valid physical reference points before interpreting an energy axis.

## Capabilities

- PySide6 desktop interface and Web Audio browser recorder
- Turkish and English language switching
- Profile-specific filtering, pulse detection, and dead-time handling
- Background acquisition with bounded queues and lost-sample accounting
- Versioned MessagePack-based `.pdet` recording format
- Atomic file saving and legacy MessagePack import
- Explicit trust confirmation for legacy Pickle recordings
- Calibration validation and command-line recording inspection
- Platform-specific packaging workflows and synthetic-recording smoke checks

## Engineering approach

Acquisition, signal processing, storage, and interface code are separated. Audio callbacks hand blocks to background processing so they do not wait on disk writes or interface updates. Dropped samples are counted and persisted, making a measurement's data-loss limitations visible.

## Technology

Python, PySide6, NumPy, SciPy, sounddevice, pyqtgraph, MessagePack, Web Audio API, PyInstaller, and GitHub Actions.

## Evidence and limits

The software's September 2026 methodology note records 14 passing local tests and synthetic-recording package checks for version 0.1.1. [The public showcase](https://github.com/Mahmutakin99/project-portfolio/tree/main/showcases/particle-detector) documents the application and retains access to the existing release packages. These recorded results were not rerun for this case study.

The software does not infer radiation dose or automatically identify isotopes. Energy interpretation requires calibration; software tests do not validate a physical detector or its noise conditions. Initial packages are documented as lacking macOS notarization and Windows code signing.

The icon above is original repository artwork, not an application screenshot. No verified software screenshot with public-safe measurement data was available. Existing hardware photographs and scientific plots were not reused as screenshots of this application.
