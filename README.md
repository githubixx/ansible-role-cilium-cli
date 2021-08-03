ansible-role-cilium-cli
=======================

Installs cilium command line utility.

Versions
--------

I tag every release and try to stay with [semantic versioning](http://semver.org). If you want to use the role I recommend to checkout the latest tag. The master branch is basically development while the tags mark stable releases. But in general I try to keep master in good shape too. A tag `1.0.0+0.8.5` means this is release `1.0.0` of this role and it uses `cilium` CLI version `0.8.5`. If the role itself changes `X.Y.Z` before `+` will increase. If the `cilium` CLI version changes `X.Y.Z` after `+` will increase too. This allows to tag bugfixes and new major versions of the role while it's still developed for a specific `cilium` CLI release.

Role Variables
--------------

```yaml
---
# "cilium" CLI version to install
cilium_cli_version: "0.8.5"

# Where to install "cilium" binary. By default that's ".local/bin" in the
# users $HOME directory.
cilium_cli_bin_directory: "{{ '~/.local/bin' | expanduser }}"

# Directory to store the cilium cli archive
cilium_cli_tmp_directory: "{{ lookup('env', 'TMPDIR') | default('/tmp',true) }}"

# Owner/group of "cilium" binary. Both variables are commented by default.
# In this case the resulting binary will be owned by the current user.
#cilium_cli_owner: "root"
#cilium_cli_group: "root"

# Specifies the permissions of the "cilium" binary
cilium_cli_binary_mode: "0755"

# Operarting system on which "cilium" should run on.
# Use "darwin" for MacOS X
cilium_cli_os: "linux"

# Processor architecture "cilium" should run on.
# Other possible values: "386","arm64","arm"
cilium_cli_arch: "amd64"

# Name of the archive file name
cilium_cli_archive: "cilium-{{ cilium_cli_os }}-{{ cilium_cli_arch }}.tar.gz"

# The cilium CLI download URL (normally no need to change it)
cilium_cli_url: "https://github.com/cilium/cilium-cli/releases/download/v{{ cilium_cli_version }}/{{ cilium_cli_archive }}"
```

Example Playbook
----------------

Example 1 (without role tag):

```yaml
- hosts: your-host
  roles:
    - githubixx.cilium_cli
```

Example 2 (assign tag to role):

```yaml
-
  hosts: your-host
  roles:
    -
      role: githubixx.cilium_cli
      tags: role-cilium-cli
```

License
-------

GNU GENERAL PUBLIC LICENSE Version 3

Author Information
------------------

[http://www.tauceti.blog](http://www.tauceti.blog)
