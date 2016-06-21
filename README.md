# Ansible Role: DVM

* Installs DVM (Drush Version Manager)
* Installs multiple versions of Drush
* Sets a default Drush version
* Installs Drush packages

## Requirements

None.

## Role Variables

Default Drush version

    drush_version: 7.2.0

All Drush versions to install

    drush_versions:
      - 6
      - 7.2.0
      - 8

Drush packages to download

    drush_packages:
      - drush_extras
      - drush_sql_extras
      - registry_rebuild

## Dependencies

Dependencies are handled by the role upon execution.

## Example Playbook

    - { role: fubarhouse.dvm }

## Installation

  * Add the DVM role to your playbook.
  * Modify above variables as desired.

## License

MIT / BSD

## Author Information

This role was created in 2015 by [Karl Hepworth](https://twitter.com/fubarhouse).
