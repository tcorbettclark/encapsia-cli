# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

_Nothing yet_

## [0.4.0] - 2020-12-07

### Added

- Support for searching S3 buckets for plugins below specified paths.

## [0.3.3] - 2020-10-27

### Fixed

- Fixed bug which created a `cwd/plugins-local-dir/` folder e.g. when running `encapsia plugins --force dev-update .`

## [0.3.2] - 2020-10-26

### Fixed

- Fixed bug which prevented pre-release semver compatible version numbers for plugins. #46.

## [0.3.1] - 2020-10-15

### Fixed

- Fixed bug which prevented local store from being updated from a versions TOML file.

## [0.3.0] - 2020-09-15

### Changed

- Moved the `--host` option to the top level. So e.g. `encapsia users --host foo` is now `encapsia --host foo users`.
- Changed all `--yes` options to `--force` for consistency.
- Changed `encapsia httpie shell` to `encapsia httpie` because it can only launch interactive httpie.

### Added

- Added support for providing options in a `~/.encapsia/config.toml` file.
- Added uniform support for providing options as env vars following click conventions. E.g.
  `ENCAPSIA_HOST` and `ENCAPSIA_PLUGINS_LOCAL_DIR`.
- Added support for upstream sources of plugins from multiple S3 buckets.

### Fixed

- Don't use `datetime.datetime.fromisoformat` because it is not present in Python 3.6.

## [0.2.3] - 2020-09-08

### Added

- A changelog!

### Fixed

- Removed traceback from users without roles (by upgrading to latest encapsia-api)