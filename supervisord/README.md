This role installs supervisord into a virtual environment

It can also be used to make sure any supervisorctl actions happen against an environment with supervisord.

Requirements:

  - virtualenv

See: supervisord/defaults/main.yaml for possible role configuration
Because all vars in the role are defaults if you need to override any of the settings you can specify them in vars, or inventories, or anywhere else.

Including the role provides `{{ super_args }}` for use in the supervisorctl module.

You can use `{{ pip_args }}` if you have special pip set-up, like an in-house pypi.
