# Contributing to SPOUT

This file applies org-wide to every repository under [spout-task](https://github.com/spout-task).

SPOUT is designed to grow: each component is its own repository, and new components become
new repositories under the org. Within a repository, add a folder rather than editing
existing components, so every published/citable version stays stable.

## Ground rules
- Open an issue before a large change.
- One logical change per pull request.
- Keep firmware's public interface (pin map, serial protocol, CSV output schema)
  backward-compatible within a major version; breaking changes bump the major version.
- Document as you go: code without a README entry is considered incomplete.

## Recipes
- **New task mode:** add its state-machine logic in [software](https://github.com/spout-task/software) under the
  right `SPOUTn/teensy_firmware/`, add its settings folder in [settings](https://github.com/spout-task/settings)
  under `SPOUTn/<task>/`, and note it in the software CHANGELOG.
- **New hardware module:** add a folder in [hardware](https://github.com/spout-task/hardware) with design files, a
  README, its parts/cost, and assembly notes.
- **New analysis:** add scripts in [analyses](https://github.com/spout-task/analyses) with a header stating inputs,
  outputs, and required MATLAB toolboxes.
- **A whole new component:** create a new repository under the org and link it from the
  org profile README.

## Versioning and releases
Semantic versioning (`MAJOR.MINOR.PATCH`); tagged releases (`vX.Y.Z`) are archived to
Zenodo, each with its own DOI. Cite the version you used.

## Licensing of contributions
Contributions are licensed under the same terms as the repository they touch: software
(GPL-3.0-or-later), hardware (CERN-OHL-S-2.0), or settings/data/docs (CC-BY-4.0).
