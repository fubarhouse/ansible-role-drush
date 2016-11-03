# Ansible Role: DVM

[![Build Status](https://travis-ci.org/fubarhouse/ansible-role-drush.svg?branch=master)](https://travis-ci.org/fubarhouse/ansible-role-drush)

* Installs DVM (Drush Version Manager)
* Installs Drush version 6, 7 and 8 (or configured)
* Sets a default Drush version (as configured)
* Installs Drush packages (optional)

## Requirements

* PHP
* Composer

## Role Variables

Default Drush version
````
drush_version: 7.2.0
````

All Drush versions to install
````
drush_versions:
  - 6
  - 7.2.0
  - 8
````

Drush packages to download
````
drush_packages:
  - drush_extras
  - drush_sql_extras
  - registry_rebuild
````

## Dependencies

None.

## Example Playbook

````
- hosts: localhost
  sudo: true
  vars:
    drush_version: 2.3.0
    drush_versions: []
    drush_packages:
      - registry_rebuild
  roles:
    - fubarhouse.drush
````

## License

MIT / BSD

## Author Information

This role was created in 2015 by [Karl Hepworth](https://twitter.com/fubarhouse).
