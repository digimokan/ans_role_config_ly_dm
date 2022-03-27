# ans_role_config_ly_dm

Install and configure the Ly display manager.

[![Release](https://img.shields.io/github/release/digimokan/ans_role_config_ly_dm.svg?label=release)](https://github.com/digimokan/ans_role_config_ly_dm/releases/latest "Latest Release Notes")
[![License](https://img.shields.io/badge/license-MIT-blue.svg?label=license)](LICENSE.md "Project License")

## Table Of Contents

* [Purpose](#purpose)
* [Supported Operating Systems](#supported-operating-systems)
* [Requirements](#requirements)
* [Quick Start](#quick-start)
    * [Use From Playbook](#use-from-playbook)
* [Role Options](#role-options)
* [Role Dependencies](#role-dependencies)
* [Contributing](#contributing)

## Purpose

* Install the [Ly](https://github.com/fairyglade/ly) display manager.
* Configure Ly for launching target window manager or desktop environment.

## Supported Operating Systems

* Arch Linux.
* FreeBSD.

## Requirements

* Xorg `.xinitrc` has been configured to launch Ly for target user(s).

## Quick Start

### Use From Playbook

1. Create `requirements.yml` in ansible project root, and add this content:

   ```yaml
   # requirements.yml
   - src: https://github.com/digimokan/ans_role_config_ly_dm
   ```

2. From the project root directory, install/download the role:

   ```shell
   $ ansible-galaxy install --role-file requirements.yml --roles-path ./roles --force-with-deps
   ```

   * _NOTE:_ `--force-with-deps` _ensures subsequent calls download updates_

3. Include the role like any local role, from the project playbook:

   ```yaml
   # playbook.yml
   - hosts: localhost
     connection: local
     tasks:
       - name: "Install and configure the Ly display manager"
         ansible.builtin.include_role:
           name: ans_role_config_ly_dm
   ```

## Role Options

See the role `defaults` files for main role vars listings:

  * [defaults](../defaults/main/)

## Role Dependencies

* [ans_role_config_unofficial_packages](https://github.com/digimokan/ans_role_config_unofficial_packages)

## Contributing

* Feel free to report a bug or propose a feature by opening a new
  [Issue](https://github.com/digimokan/ans_role_config_ly_dm/issues).
* Follow the project's [Contributing](CONTRIBUTING.md) guidelines.
* Respect the project's [Code Of Conduct](CODE_OF_CONDUCT.md).

