OULibraries.gitolite3
=========

Provides a minimally configured EPEL-based gitolite3 install with
managed keys and administrative users.

Settings controlled by this role are placed in
`conf/gitolite.conf`. Additional unmanaged configuration files may be
placed in `conf/conf.d`.


Requirements
------------

No special role requirements. 

Role Variables
--------------

```
# dict with account config
gitolite_users:
  - name: 'jdoe'
    pubkey: '{{ jdoe_key }}'

# list of admins
gitolite_admins:
  - jdoe
```
      

Dependencies
------------

Probably depends on `OULibraries.centos7`, but maybe just needs a working EPEL. 

Example Playbook
----------------

Something like this should work:

```
- hosts: gitserver
  roles:
  - role: OULibraries.gitolite
    tags: gitolite
```	 

License
-------

MIT

Author Information
------------------

Written for OU Libraries. 
