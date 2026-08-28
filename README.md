## About this repository

This repository is a development mirror of postmarketOS `pmaports` used for the Samsung Galaxy Tab A 10.1 2016 (SM-T580 / `gtaxlwifi`) port.

Upstream repository:

`https://gitlab.postmarketos.org/postmarketOS/pmaports.git`

`pmaports` contains postmarketOS package build recipes, device packages, kernel package definitions, patches and related packaging files.

This mirror keeps the upstream Git history while carrying the temporary SM-T580-specific changes required during device bring-up.

The goal is not to replace upstream postmarketOS. Changes that are suitable for upstream inclusion may eventually be cleaned up and submitted there once the port is functional and properly tested.

No ownership of upstream postmarketOS code is claimed by this repository.

### Licensing

The pmaports repository itself is distributed under the GNU General Public License version 3 only (GPL-3.0-only).

Individual packages described by APKBUILD files may build software distributed under other licenses. Their `license=` metadata describes the packaged upstream software and does not replace the license of the pmaports repository itself.

Existing copyright notices, package metadata, license files, patch attribution and authorship history should be preserved.

See:

* `LICENSE`
* `https://postmarketos.org/source-code/`

### Development model

The repository is intended to use:

`origin` — this mirror

`upstream` — the official postmarketOS pmaports repository

Upstream changes can therefore continue to be fetched normally while the `port/gtaxlwifi-6.19` branch carries the SM-T580-specific work.

Changes are tested locally before a new known-good pmaports revision is recorded by the parent `gtaxlwifi-port` meta-repository.

# postmarketOS aports repository

This repository contains the APKBUILD files for postmarketOS-specific packages, along with the required patches and scripts, if any.

There are many more packages defined in the [Alpine Linux aports](https://gitlab.alpinelinux.org/alpine/aports/) on which these packages depend.

Helpful resources:

* [Issues](https://gitlab.postmarketos.org/postmarketOS/pmaports/-/work_items)
* [How to create a package](https://wiki.postmarketos.org/wiki/Create_a_package)
* [APKBUILD reference](https://wiki.alpinelinux.org/wiki/APKBUILD_Reference)
* [pmaports commit style](./COMMITSTYLE.md)
* [Approval rules](docs/merge-requests/approval-rules.md)
* [Alpine Linux aports](https://gitlab.alpinelinux.org/alpine/aports/)
* [Alpine Linux package search](https://pkgs.alpinelinux.org/packages)
* [postmarketOS package search](https://pkgs.postmarketos.org/packages)

## Git Hooks

You can find some useful git hooks in the `.githooks` directory.
To use them, run the following command after cloning this repository:

```sh
git config --local core.hooksPath .githooks
```
