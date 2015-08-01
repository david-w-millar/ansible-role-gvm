# Ansible GVM Role - Work In Progress

Ansible role to help manager your Groovy ecosystem with [GVM](http://gvmtool.net).

This role is a work in progress. It will probably work for most cases, but needs a bit of polishing.

## Requirements

This role requires Java to be installed in order to use any GVM managed tools.

Currently, it installs an openjdk package to satisfy this requirement,
but this is likely to change very soon for the sake of flexibility.

## Role Variables

Nothing yet.

## Dependencies

Nothing yet.

## Example Playbook

    - hosts: servers
      roles:
         - dwm.gvm

## License

http://www.apache.org/licenses/LICENSE-2.0.html[Apache License, Version 2.0].


