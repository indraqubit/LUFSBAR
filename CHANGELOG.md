# Changelog

All notable changes to LUFSBar are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.1] - 2026-11-11

### Fixed

- Loudness reading dropped when playing audio from a DAW (e.g. REAPER). LUFSBar now listens for sample-rate changes on the output device and rebuilds its tap, so metering stays correct when a DAW switches the interface clock.
- Release pipeline aborted when no leftover DMG volume was mounted (`hdiutil detach` loop).

## [1.0.0] - 2026-11-11

### Added

- Initial release: system-wide audio loudness meter for the macOS menu bar.
- ITU-R BS.1770-4 / EBU R128 loudness (Momentary, Short-term, Integrated).
- Zero-driver Core Audio process tap (macOS 14.2+).
- Universal binary (Apple Silicon + Intel), notarized and stapled.
