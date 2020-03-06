base-config
=========

This role is a basic config for all server types. It currently configures internal `yum` repositories for internal-hosted servers.

The repo file to be used is located under `files/` and is encrypted.

Role Variables
--------------

* `repo_dest` - The intended full path of the repo file on the server

License
-------

BSD
