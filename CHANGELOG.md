# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.3.0] - 2020-03-17

### Added

* Add acceptance testing

### Changed

* Install NiFi version `1.11.3` by default.
* Set NiFi local state directory to `${var_directory}/state/local` to
  ensure it survives future NiFi upgrades. To avoid losing state when
  upgrading to this module version, stop the NiFi service, move
  `/opt/nifi/nifi-${version}/state/local` to
  `/var/opt/nifi/state/local`, then run Puppet to configure NiFi.

## [0.2.0] - 2020-02-22

### Added

* Management of `nifi.properties`

### Changed

* Default nifi version to install is now `1.11.1`.

## [0.1.1] - 2020-01-22

### Changed

* systemd now starts the process as a simple instead of a forking
  service.

## [0.1.0] - 2020-01-14

### Added

* Initial release.
* Download, install and start Apache NiFi.
