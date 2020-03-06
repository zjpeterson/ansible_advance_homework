setup-workstation
=========

This role completes prerequisite setup of an OpenStack environment to run servers built with the `osp-servers` role.

There are multiple task files:
- `main.yml` - Calls the rest of the playbooks in the order they appear here.
- `create-flavor.yml` - Creates server flavor
- `create-keypair.yml` - Creates access keypair for servers
- `create-sg.yml` - Creates security groups
- `create-image.yml` - Creates image to build servers with
- `create-network.yml` - Creates internal and extral networks for server connectivity

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
