# Ansible Role: DVM

Installs Drush Version Manager on Debian/Ubuntu servers.

## Requirements

Requires `composer` to be installed on the server.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```
dvm_dir: "/usr/lib/dvm"
dvm_location: "{{ dvm_dir }}/dvm"
```

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
