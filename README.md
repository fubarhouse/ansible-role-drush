# Ansible Role: DVM

  Installs Drush Version Manager on Debian and Darwin servers.

## Requirements

  None.

## Role Variables

  Copy the defaults/main.yml into the ansible system and add to the playbook, and change the variables accordingly.

  ````
    fubarhouse_dvm:
      # User
      user: "{{ ansible_user_id }}"
      # Application versions
      dvm_drush_version: 7
      # Application versions (non-default)
      all_drush_versions:
        - 6
        - 7
        - 8
      # Clean install
      clean_install: false
      # Process controls
      install_dvm: true
      dvm_drush_update: false
      dvm_install_packages: true
      # Repositories
      dvm_repo: "https://github.com/fubarhouse/dvm"
      # Install directories
      dvm_dir: "/home/{{ ansible_user_id }}/.dvm"
      # Symlinks
      symlinks:
        - name: dvm
          src: "/home/{{ ansible_user_id }}/.dvm/dvm"
          dest: "/usr/local/bin/dvm"
        - name: drush
          src: "/home/{{ ansible_user_id }}/.dvm/drush"
          dest: "/usr/local/bin/drush"
      # Install paths
      # Executables
      dvm_exec: "dvm"
      # Packages
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
