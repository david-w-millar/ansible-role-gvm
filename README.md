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

## Caveats

The GVM / SdkMan installation scripts only update shell startup scripts the first time that it is run.

If a user changes her shell after this role is applied, subsequent applications will fail
to update the new users shell startup scripts.

Until I find a more elegant solution for this problem (or someone is kind enough to issue a pull request),
you can work around this adding the following snippet to your bash compatible startup scripts,

```bash
#THIS MUST BE AT THE END OF THE FILE FOR SDKMAN TO WORK!!!
export SDKMAN_DIR="/Users/<username>/.sdkman"
[[ -s "/Users/$(whoami)/.sdkman/bin/sdkman-init.sh" ]] && source "/Users/$(whoami)/.sdkman/bin/sdkman-init.sh"

```

See [this](https://github.com/sdkman/sdkman-cli/blob/master/src/main/bash/install.sh#L112) for more information.

## TODO

* CI & Testing
* Automate releases and publishing
* Add vars for GVM config
* Add feature to install tools, optionally with a specified version
* Use ansigenome

## License

http://www.apache.org/licenses/LICENSE-2.0.html[Apache License, Version 2.0].


