# ansible-role-appzapper

[![Build Status](https://travis-ci.org/tkimball83/ansible-role-appzapper.svg?branch=master)](https://travis-ci.org/tkimball83/ansible-role-appzapper)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-appzapper-blue.svg?style=flat)](https://galaxy.ansible.com/tkimball83/appzapper)
[![License](https://img.shields.io/badge/license-GPLv3-brightgreen.svg?style=flat)](COPYING)

macOS - The uninstaller Apple forgot

## Requirements

This role requires homebrew and homebrew cask to be installed

## Role Variables

Available variables are listed below, along with default values:

    appzapper_defaults: []
    appzapper_domain: "com.appzapper.{{ appzapper_package }}"
    appzapper_package: AppZapper

## Dependencies

None

## Example Playbook

    - hosts: localhost
      connection: local
      roles:
        - role: tkimball83.appzapper
          appzapper_defaults:
            - name: AppleAppsSafe
              type: bool
              value: true
            - name: DefaultsSet
              type: bool
              value: true
            - name: "Registration Code"
              type: string
              value: APZP-000-000-000-000
            - name: "Registration Name"
              type: string
              value: 'Taylor Kimball'
            - name: ZapEffects
              type: bool
              value: true

## License

Copyright (C) 2018 Taylor Kimball <tkimball@linuxhq.org>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.
