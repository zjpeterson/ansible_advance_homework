config-tower
=========

A brief description of the role goes here.

Task Files
------------

* `ec2_dynamic.yml` - For creating Dynamic inventory in Ansible tower. Use `AWS Access Key` for credential
* `job_template.yml` - For creating job templates
* `pre-config-tower.yml` - Any pre config tasks needed
* `workflow_template.yml` - genrate workflow from `workflow.yml` file
* `post-config-tower.yml` - any post config jobs

Role Variables
--------------

In `defaults/main.yml`, define a dictionary containing key locations like so:
```
keys:
  personal: /root/.ssh/mykey.pem
  openstack: /root/.ssh/openstack.pem
```
You should have put these keys in place and verified their existence.
* `keys.personal` is your OPENTLC private key to be used for accessing OpenStack via Tower Bastion
* `keys.openstack` is the lab-distributed OpenStack private key.

There are several variables set in `vars/main.yml` that should not be changed.

License
-------

BSD
