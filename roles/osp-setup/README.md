osp-setup
=========

This role completes prerequisite setup of an OpenStack environment to run servers built with the `osp-servers` role.

Requirements
------------

Back-end OpenStack elements should already be configured. The cloud used in `cloud_name` declarations must match a defined cloud in your OSP `clouds.yaml` file.

Role Variables
--------------

`osp_networks` - Should contain keys `internal` and `external` describing the corresponding networks. See `vars/main.yml`.

`osp_router` - Should contain key `router` describing the external route. See `vars/main.yml`.

License
-------

BSD
