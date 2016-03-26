# Ansible Role: DVM

  Installs Drush Version Manager on Debian/Ubuntu servers.

## Requirements

  None.

## Role Variables

  Available variables are listed below, along with default values (see `defaults/main.yml`):

  ### Clean install
  ````
  clean_install: true
  ````
  ### Process controls
  ````
  install_dvm: true
  dvm_drush_update: false
  dvm_install_packages: true
  ````
  ### Repositories
  ````
  dvm_repo: "https://github.com/fubarhouse/dvm"
  ````
  ### Symlinks
  ````
  dvm_symlink: "/usr/local/bin/dvm"
  drush_symlink: "/usr/local/bin/drush"
  ````
  ### Install directories
  ````
  dvm_dir: "~/.dvm"
  ````
  ### Install paths
  ### Executables
  ````
  dvm_exec: "dvm"
  ````
  ### Application versions
  ````
  dvm_drush_version: 7.1.0
  ````
  ### Packages
  ````
  packages:
    - drush_extras
    - drush_sql_extras
    - registry_rebuild
  ````


## Dependencies

  None.

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

This role was redeveloped in 2016 by [Karl Hepworth](https://twitter.com/fubarhouse).
