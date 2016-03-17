# Ansible GVM Role - Work In Progress

Ansible role to help manager your Groovy ecosystem with [GVM](http://gvmtool.net).
The official name has been changed to [SdkMan](http://sdkman.io), but that's still growing on me.

This role is a work in progress. It will probably work for most cases, but needs a bit of polishing.

## Requirements

This role requires Java to be installed in order to use any GVM managed tools.

Currently, it installs an openjdk package to satisfy this requirement,
but this is likely to change very soon for the sake of flexibility.

## Role Variables

None.

## Dependencies

None.

## Example Playbook

    - hosts: servers
      roles:
         - david-w-millar.gvm

## TODO

* CI & Testing
* Automate releases and publishing
* Add vars for GVM config
* Add feature to install tools, optionally with a specified version
* Use ansigenome
* Address problem where this role does not play well with any roles that change the user's shell

## License

http://www.apache.org/licenses/LICENSE-2.0.html[Apache License, Version 2.0].


