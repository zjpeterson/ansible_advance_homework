osp-servers
=========

This role provisions OpenStack serversm and applies network and security configuration to them, according to a dictionary provided by the user,

Requirements
------------

The OpenStack clouds.yaml file must contain access information for a cloud with a name that you specify in this role in `osp_cloud`.

Role Variables
--------------

`osp_cloud` - The OSP cloud to reference according to your OSP workstation's clouds.yaml file.

`osp_servers` - A list of dictonaries, each defining a server to be built. Each dictionary should have a defined `name`, `image`, `flavor`, `security_group`, and `meta`. The `meta` value should be a dictonary containing `group` and `deployment_name`. Example list item:
```
  - name: app1
    image: rhel-guest
    flavor: m2.small
    security_group: apps
    meta:
      group: apps
      deployment_name: QA
```

`osp_network` - A dictonary defining the network details to be used. Sub-keys are `internal` and `external` for the respective network details. Each of those keys should have a `name` and `cidr` defined. Example:
```
osp_network:
  internal:
    name: int_network
    cidr: 10.10.10.0/24
  external:
    name: ext_network
    cidr: 20.20.20.0/24
```

License
-------

BSD
