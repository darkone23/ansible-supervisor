This repository is a collection of [ansible](http://ansibleworks.com) roles to work with supervisord, with a focus on being as simple to use as possible, and configurable enough to cope with any environmental concerns.

See [supervisord](http://supervisord.org/) and the ansible [supervisorctl module](http://www.ansibleworks.com/docs/modules.html#supervisorctl) for more information.

## Roles:

### [supervisord](https://github.com/eggsby/ansible-supervisor/blob/master/supervisord)

This role just [installs supervisord](https://github.com/eggsby/ansible-supervisor/blob/master/supervisord.yaml) into a virtualenv.
This mean you can run it as any user.
It provides `{{ super_args }}` for use interacting with the supervisorctl ansible module.


### [supervise](https://github.com/eggsby/ansible-supervisor/blob/master/supervise)

The supervise app creates a supervised daemon out of simple user-level commands.
See the simple [http server](https://github.com/eggsby/ansible-supervisor/blob/master/http-server.yaml) playbook for an idea how to get started using supervisor & ansible to manage your apps.


## Installation:
Just check out this repository and add the checkout location to your [roles_path](http://www.ansibleworks.com/docs/intro_configuration.html#roles-path) in your ansible.cfg

## Configuration

You can control where supervisor installs, what version it installs, who it installs as, and any any special installation options.
With apps, you can control the command, the directory they start in, where they log to, and the environment they run in.

Or you can just let the defaults do their thing.

  * [supervisord defaults](https://github.com/eggsby/ansible-supervisor/blob/master/supervisord/defaults/main.yaml)
  * [supervise defaults](https://github.com/eggsby/ansible-supervisor/blob/master/supervise/defaults/main.yaml)

Enjoy
