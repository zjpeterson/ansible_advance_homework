osp-instance-delete
=========

Discovers and deletes servers in an OpenStack cloud. Meant for use with ephemeral testing environments.

Requirements
------------

The OpenStack clouds.yaml file must contain access information for a cloud with a name that you specify in this role in `osp_cloud`.

Role Variables
--------------

`osp_cloud` - The OSP cloud to reference according to your OSP workstation's clouds.yaml file.

License
-------

BSD
