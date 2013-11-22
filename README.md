This repository is an [ansible](http://ansibleworks.com) role for installing a supervisor daemon, with a focus on being simple & usable without root.

Because of this it installs the supervisor utility into a virtualenv instead of into the systems python like many system packages do. Hopefully in the future this will be a configurable feature.

## Requirements:

  - virtualenv

You can use `{{ pip_args }}` if you have special pip set-up, like an in-house pypi.

## Installation:
Just check out this repository and add the checkout location to your [roles_path](http://www.ansibleworks.com/docs/intro_configuration.html#roles-path) in your ansible.cfg

    git clone https://github.com/eggsby/ansible-supervisor supervisor/

## Usage:

    roles:
      - name: supervisor
        supervisor_home: ~/apps/supervisor

This will ensure a supervisor daemon is installed and running in the context you run the role in.
    
It provides `{{ super_args }}` for use interacting with the supervisorctl ansible module, providing things like the path to the config for your supervisord instance.

    supervisorctl: name=webserver state=restarted {{ super_args }}

See [supervisord](http://supervisord.org/) and the ansible [supervisorctl module](http://www.ansibleworks.com/docs/modules.html#supervisorctl) for more information.

## Configuration

You can control where supervisor installs, what version it installs, who it installs as, and any special installation options.

It installs shell aliases for accessing the supervisor using `supervisorctl -c path-to.conf` -- you can control this using `alias_file`

Or you can just let the defaults do their thing.

  * [supervisord defaults](https://github.com/eggsby/ansible-supervisor/blob/master/defaults/main.yaml)

Enjoy
