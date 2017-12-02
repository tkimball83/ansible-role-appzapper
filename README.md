# ansible-role-appzapper

[![Build Status](https://travis-ci.org/tkimball83/ansible-role-appzapper.svg?branch=master)](https://travis-ci.org/tkimball83/ansible-role-appzapper)

macOS - The uninstaller Apple forgot

## Requirements

This role requires homebrew and homebrew cask to be installed

## Role Variables

Available variables are listed below, along with default values:

    appzapper_pkg: AppZapper
    appzapper_domain: "com.appzapper.{{ appzapper_pkg }}"
    appzapper_defaults: {}

## Dependencies

None

## Example Playbook

    - hosts: localhost
      connection: local
      roles:
        - role: tkimball83.appzapper
          appzapper_defaults:
            AppleAppsSafe:
              type: bool
              value: true
            DefaultsSet:
              type: bool
              value: true
            Registration_Code:
              type: string
              value: APZP-000-000-000-000
            Registration_Name:
              type: string
              value: 'Taylor Kimball'
            ZapEffects:
              type: bool
              value: true

## License

GPLv3

## Author Information

This role was created by [Taylor Kimball](http://www.linuxhq.org).
