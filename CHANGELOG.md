# Changelog

All notable changes to this project are documented here.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and the project
uses [Semantic Versioning](https://semver.org/spec/v2.0.0.html). Before 1.0.0, a minor version
bump may include breaking changes; these are always called out below.

## [0.2.0] - Unreleased

The first packaged version. Nothing before this was tagged or released.

### Added

- `carry_the_one` package installable with `pip install -e .`, defined in `pyproject.toml`.
- Console entry points: `carry-the-one` (the drill) and `carry-the-one-insights` (analysis).
- `carry-the-one-insights` options: an optional session name, `--file` and `--save`.
- GUI-free modules (`core`, `features`, `storage`) that run headless.
- A pytest suite covering drill logic, features, storage, insights and timer callbacks.
- GitHub Actions CI: ruff lint and format, pytest on Python 3.10–3.12, a clean-install check,
  and pip-audit on runtime and development dependencies.
- Sample counts and baseline counts in the feature comparison chart.
- A reproducible synthetic dashboard image (`python -m scripts.render_demo`).
- MIT license.

### Changed

- Renamed the project from Math Drill to Carry the One. `$MATHDRILL_DATA_DIR` and an existing
  `math-drill` data directory are still honoured.
- Session data is resolved to an absolute path: `$CARRY_THE_ONE_DATA_DIR`, then `Data/` in a
  source checkout, then a per-user data directory when installed.
- Sessions are written atomically and validated on load.
- Records store `operation`. Older logs that use `question_type` are still read.
- Countdown and answer timing use a monotonic clock.
- Session-rate statistics average per-session rates instead of pooling durations.

### Fixed

- `requirements.txt` listed `tkinter`, which made `pip install -r requirements.txt` fail.
- A named session filter was silently ignored.
- Duplicate submissions and pending timer callbacks could record or save a session twice.
- Sessions with repeated names were merged in the analysis.
- A named filter on an empty log raised an error.
- Broken README images and captions.

### Security

- Required pytest 9.0.3 or later (PYSEC-2026-1845) and started auditing development dependencies
  in CI.

## [0.1.0] - 2025-08-10

The original Math Drill: a three-file Tkinter app with timed drills, a JSON practice log and
pandas/matplotlib analysis. It was never tagged.

[0.2.0]: https://github.com/aman25singh/carry-the-one/compare/bc6f2aa...v0.2.0
[0.1.0]: https://github.com/aman25singh/carry-the-one/commit/bc6f2aa
