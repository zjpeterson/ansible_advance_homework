osp-facts
=========

Gathers information about an OpenStack environment, and builds an in-memory inventory of the server infrastructure it discovers.

Requirements
------------

The OpenStack clouds.yaml file must contain access information for a cloud with a name that you specify in this role in `osp_cloud`.

Role Variables
--------------

`osp_cloud` - The OSP cloud to reference according to your OSP workstation's clouds.yaml file.

License
-------

BSD
