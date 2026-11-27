# Roadmap

Where Carry the One is heading. Each release has one theme. Dates are deliberately left out,
and plans may change. Released work is recorded in [CHANGELOG.md](CHANGELOG.md).

Suggestions are welcome as [issues](https://github.com/aman25singh/carry-the-one/issues).

## Next goal

**Install and play Carry the One without Python and without cloning the repository.**

## v0.2.0: First release

- [ ] Changelog
- [ ] Tag `v0.2.0`
- [ ] GitHub Release with a source distribution and a wheel

## v0.3.0: Installable app

- [ ] Standalone Windows executable
- [ ] Standalone macOS app
- [ ] Practice data saved to the per-user data directory when running as an app
- [ ] Install guide for people who have never used Python, including the warnings shown for
      unsigned apps on macOS and Windows

## v0.4.0: Automated releases

- [ ] Release workflow triggered by pushing a version tag
- [ ] Tests and builds on Linux, Windows and macOS
- [ ] `SHA256SUMS` published with every release
- [ ] Dependabot for Python dependencies and GitHub Actions
- [ ] Possibly: publish to PyPI

## v0.5.0: Command-line interface

- [ ] A single `carry` command with subcommands:

  ```
  carry train --operation multiplication --duration 60
  carry stats --last 7d
  carry history
  carry export --format csv
  carry report --output report.html
  ```

- [ ] `carry-the-one` and `carry-the-one-insights` keep working

## v0.6.0: Better analysis

- [ ] Response-time distributions per operation and feature
- [ ] Confidence intervals on "this feature costs you X seconds"
- [ ] A difficulty model that predicts answer time from the problem
- [ ] Adaptive drills that serve more of the problems you are slow at

## v1.0.0: Stable

- [ ] A versioned data format (`schema_version`) with migrations
- [ ] Contributing guide and issue templates
- [ ] A documented support policy for Python versions and dependencies

## Not planned for now

- A web version (see the deferred items in [PROJECT_REPORT.md](PROJECT_REPORT.md))
