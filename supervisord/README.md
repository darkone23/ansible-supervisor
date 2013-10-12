This role installs supervisord into a virtual environment

It can also be used to make sure any supervisorctl actions happen against an environment with supervisord.

Requirements:

  - virtualenv

See: supervisord/defaults/main.yaml for possible role configuration

Provides `{{ super_args }}` for use in the supervisorctl module

