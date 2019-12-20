# Ansible Role: anydesk

[![Build Status](https://img.shields.io/travis-ci/sbaerlocher/ansible.anydesk.svg?branch=master&style=popout-square)](https://travis-ci.org/sbaerlocher/ansible.anydesk) [![license](https://img.shields.io/github/license/mashape/apistatus.svg?style=popout-square)](https://sbaerlo.ch/licence) [![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-anydesk-blue.svg?style=popout-square)](https://galaxy.ansible.com/sbaerlocher/anydesk) [![Ansible Role](https://img.shields.io/ansible/role/d/id.svg?style=popout-square)](https://galaxy.ansible.com/sbaerlocher/anydesk)

## Description

Ansible Role which AnyDesk stores on all desktops.

## Installation

```bash
ansible-galaxy install sbaerlocher.anydesk
```

## Requirements

None

## Role Variables

### Download Linl

Dwonload link from AnyDesk.

```yml
anydesk_download_url: 'https://download.anydesk.com/AnyDesk.exe'
```

### Directory

Directory where the file should be stored

```yml
anydesk_root_directory: "{{ ansible_env.SystemDrive }}\\{{ source_of_supply_name | default('Support') }}"
anydesk_tools_directory: '{{ anydesk_root_directory }}\\tools.d'
```

### binary

Name of the binary file.

```yml
anydesk_binary_nane: AnyDesk.exe'
```

## Dependencies

None

## Example Playbook

```yml
- hosts: all
  roles:
    - sbaerlocher.anydesk
```

## Author

- [Simon Bärlocher](https://sbaerlocher.ch)

## License

This project is under the MIT License. See the [LICENSE](https://sbaerlo.ch/licence) file for the full license text.

## Copyright

(c) 2020, Simon Bärlocher
