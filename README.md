[![Test deployment](https://github.com/GeekOops/geekoops-dovecot/actions/workflows/CI.yml/badge.svg)](https://github.com/GeekOops/geekoops-dovecot/actions/workflows/CI.yml)

# ansible role for setting up Dovecot

Configurable ansible role for setting up dovecot. users can be configured to be taken from MySQL or LDAP
Works with

- openSUSE Leap 15.4 -> tested

## Role Variables
--------------

You can set the following variables to configure the role. Here listed are the variables and their default settings.

Firewall configuration (disable by default)


| Value | Description | Default |
|-------|-------------|---------|
|`mail_sql_backup` | file name of an SQL backup | "" |


## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: jellyfish
      roles:
         - { role: geekoops-clamav, fangfrisch_prefix="/opt/fangfrisch" }

An advanced example for the imaginary `jellyfish` test server

    - hosts: jellyfish
      roles:
         - role: geekoops-clamav
           vars:
             fangfrisch_prefix: "/opt/fangfrisch"

## License

MIT

# Development
MySQL config follows this:
https://thomas-leister.de/mailserver-debian-buster/

## Add githooks

This repository ships pre-commit git hooks that will check the yaml syntax. To configure them do

    git config --local core.hooksPath .githooks/
