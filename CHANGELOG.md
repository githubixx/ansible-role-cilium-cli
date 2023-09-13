Changelog
---------

**2.7.0+0.15.8**

- set `cilium_cli_version` to `0.15.8`
- add Molecule test for Ubuntu 22.04
- `molecule/default/molecule.yml`: move `memory` and `cpus` options to instances

**2.7.0+0.14.6**

- set `cilium_cli_version` to `0.14.6`

**2.6.0+0.13.2**

- set `cilium_cli_version` to `0.13.2`
- add `molecule/default/prepare.yml` and move tasks from `molecule/default/converge.yml`

**2.5.0+0.13.1**

- set `cilium_cli_version` to `0.13.1`
- fix Molecule `converge.yml`

**2.4.0+0.12.11**

- set `cilium_cli_version` to `0.12.11`
- add Github release action to push new release to Ansible Galaxy
- add `.yamllint`
- add `verify` for Molecule tests

**2.3.0+0.12.3**

- set `cilium_cli_version` to `0.12.3`
- `tasks/main.yml`: add mode for `get_url` task
- `tasks/main.yml`: use FQDN Ansible module names
- `meta/main.yml`: platform versions values should be string
- `defaults/main.yml`: ansible-lint
- `meta/main.yml`: `min_ansible_version` value should be string

**2.2.2+0.11.9**

- set `cilium_cli_version` to `0.11.9`

**2.2.1+0.11.7**

- set `cilium_cli_version` to `0.11.7`

**2.2.0+0.11.4**

- set `cilium_cli_version` to `0.11.4`

**2.1.0+0.10.3**

- set `cilium_cli_version` to `0.10.3`

**2.0.0+0.9.3**

- set `cilium_cli_version` to `0.9.3`
- changed default for `cilium_cli_bin_directory` from `~/.local/bin` to `/usr/local/bin`
- introduced `cilium_cli_bin_directory_owner`
- introduced `cilium_cli_bin_directory_group`
- introduced `cilium_cli_bin_directory_mode`
- changed default for `cilium_cli_owner` to `root`
- changed default for `cilium_cli_group` to `root`

**1.2.0+0.9.2**

- update to Cilium CLI `v0.9.2`

**1.1.0+0.9.0**

- update to Cilium CLI `v0.9.0`

**1.0.1+0.8.6**

- update to Cilium CLI `v0.8.6`

**1.0.0+0.8.5**

- initial commit for Cilium CLI `v0.8.5`

