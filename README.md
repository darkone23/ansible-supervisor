This repository is a collection of ansible roles to work with supervisord

See [supervisord](http://supervisord.org/) and the ansible [supervisorctl module](http://www.ansibleworks.com/docs/modules.html#supervisorctl) for more information.

Installation:
Just check out this repository and add the checkout location to your [roles_path](http://www.ansibleworks.com/docs/intro_configuration.html#roles-path) in your ansible.cfg

### [supervisord](https://github.com/eggsby/ansible-supervisor/blob/master/supervisord)

This role just installs supervisord into a virtualenv.
This mean you can run it as any user.
It provides `{{ super_args }}` for use interacting with the supervisorctl ansible module.

### [supervise](https://github.com/eggsby/ansible-supervisor/blob/master/supervise)

The supervise app creates a supervised daemon out of simple user-level commands.
See the simple [http server](https://github.com/eggsby/ansible-supervisor/blob/master/http-server.yaml) playbook for an idea how to get started using supervisor & ansible to manage your apps.

Enjoy
