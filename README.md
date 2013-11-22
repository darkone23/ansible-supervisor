This repository is a collection of [ansible](http://ansibleworks.com) roles to work with supervisord, with a focus on being as simple to use as possible, and configurable enough to cope with any environmental concerns.

See [supervisord](http://supervisord.org/) and the ansible [supervisorctl module](http://www.ansibleworks.com/docs/modules.html#supervisorctl) for more information.

## Roles:

This role just install supervisord into a virtualenv.
This mean you can run it as any user.

It provides `{{ super_args }}` for use interacting with the supervisorctl ansible module.

You can use `{{ pip_args }}` if you have special pip set-up, like an in-house pypi.

## Requirements:

  - virtualenv

## Installation:
Just check out this repository and add the checkout location to your [roles_path](http://www.ansibleworks.com/docs/intro_configuration.html#roles-path) in your ansible.cfg

    git clone https://github.com/eggsby/ansible-supervisor supervisor/

## Configuration

You can control where supervisor installs, what version it installs, who it installs as, and any special installation options.

It installs aliases for accessing the supervisor using `supervisorctl -c path-to.conf` -- you can control this using `alias_file`

Or you can just let the defaults do their thing.

  * [supervisord defaults](https://github.com/eggsby/ansible-supervisor/blob/master/defaults/main.yaml)

Enjoy
