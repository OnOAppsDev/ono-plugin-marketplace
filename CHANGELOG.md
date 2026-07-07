# Changelog

All notable changes to this marketplace are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this marketplace adheres to [Semantic Versioning](https://semver.org/).
The version below is the marketplace's own `metadata.version` in
[`marketplace.json`](.claude-plugin/marketplace.json) — bumped **minor** when
a plugin is added, **patch** for any other change (renames, source
swaps, or a listed plugin's own version bump).

## [1.3.2] - 2026-07-07

### Changed
- Renamed `ono-plugin-QA-ReactNative` to `ono-plugin-qa` (source repo,
  description, and version updated to reflect broader QA scope across
  React, React Native, iOS, and Android).

## [1.3.1] - 2026-07-07

### Changed
- Renamed `ono-react-native-dev-plugin` to `ono-mobile-dev-plugin` (source
  repo and description updated to reflect its broader mobile scope).

## [1.3.0] - 2026-07-07

### Added
- `spec-team-toolkit` — HLD and LLD document builders for the spec team.

## [1.2.0] - 2026-07-06

### Added
- `ono-plugin-QA-ReactNative` — Figma-grounded QA test planning and dev/QA
  coverage gap analysis for React Native features.

## [1.1.0] - 2026-07-05

### Added
- `ono-react-native-dev-plugin` — React Native SDLC workflow plugin (feature
  analysis, dev planning, implementation, code review, debugging, QA
  handoff, release readiness).

## [1.0.7] - 2026-07-05

### Changed
- Renamed the marketplace identifier from `ono-claude-marketplace` to
  `ono-plugin-marketplace` and updated the `ono-project-inspector` source URL
  and README instructions to match.

## [1.0.6] - 2026-07-04

### Changed
- Bumped `ono-project-inspector` to `0.7.0`.

## [1.0.5] - 2026-07-04

### Changed
- Bumped `ono-project-inspector` to `0.6.0`.

## [1.0.4] - 2026-07-04

### Changed
- Switched `ono-project-inspector`'s source from a `github` source to an
  HTTPS `url` source so installs work on any machine without SSH keys
  configured.

## [1.0.3] - 2026-07-04

### Changed
- Bumped `ono-project-inspector` to `0.5.0`.

## [1.0.2] - 2026-07-03

### Changed
- Bumped `ono-project-inspector` to `0.4.0`.

## [1.0.1] - 2026-07-03

### Changed
- Switched `ono-project-inspector` from a local symlink to a GitHub source.

## [1.0.0] - 2026-07-02

### Added
- Initial marketplace with the `ono-project-inspector` plugin (referenced via
  a local symlink).
