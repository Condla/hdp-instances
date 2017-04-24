HDP Instances
=========

Hdp-instances is a role to create cloud infrastructure to be used for
an installation of an HDP cluster.

Requirements
------------

Don't forget to set these environment variables to connect to you AWS
instances.
```
export AWS_REGION="your-default-aws-region"
export AWS_ACCESS_KEY_ID="your-key-id-here"
export AWS_SECRET_ACCESS_KEY="your-key-here"
```

You need to install the boto package

```
pip install boto
```


Role Variables
--------------

The default variables are:

* image: define which AWS AMI you want to use as a base
* subnet-id: define the subnet you want to put your nodes into
* utility_instance_type: define the instance type you want for your utility
  nodes
* utility_count: define how many utility nodes you want to provision
* master_instance_type: define the instance type you want for your master nodes
* master_count: define how many master nodes you want to provision
* worker_instance_type: define the instance type you want for your worker nodes
* worker_count: define how many worker nodes you want to provision
* region: define the AWS region you want to provision the instances in
* key_name: define the name of the private/public keypair you want to use to
  access the nodes
* security_group: define which security group should be used


Dependencies
------------



Example Playbook
----------------

- name: create ec2 infrastructure
  hosts: localhost
  gather_facts: no
  roles:
    - hdp-instances
 


License
-------

BSD

Author Information
------------------

Stefan Kupstaitis-Dunkler
<a mailto:stefan.dun@gmail.com>stefan.dun@gmail.com</a>
[https://blog.kupstaitis-dunkler.com](https://blog.kupstaitis-dunkler.com)
