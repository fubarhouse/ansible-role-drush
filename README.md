# Ansible Role: DVM

Installs Drush Version Manager on Debian/Ubuntu servers.

## Requirements

Requires `composer` to be installed on the server.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

Change installation directory which will contain the git repository

    dvm_dir: "/usr/lib/dvm"

Location to the executable file which is constructed from the `{{ dvm_dir }}` variable above.

    dvm_location: "{{ dvm_dir }}/dvm"

Version which this role which automatically ensure is installed and being used by default.

    dvm_drush_version: 7.0.0-rc1

## Dependencies

  none

## Example Playbook

```
  - { role: fubarhouse.dvm, when: '"dvm" in installed_extras' }
```

## Installation

  * Add "dvm" to the installed_extras variable in your config.yml file to use this role with the playbook example above.
  * Add dvm to playbook, as per the playbook example above.

## License

MIT / BSD

## Author Information

This role was created in 2015 by [Karl Hepworth](https://twitter.com/fubarhouse).
