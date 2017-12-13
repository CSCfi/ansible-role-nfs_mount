[![Build Status](https://travis-ci.org/CSCfi/ansible-role-nfs_mount.svg)](https://travis-ci.org/CSCfi/ansible-role-nfs_mount)
ansible-role-nfs_mount
=========

Mounts NFS

Requirements
------------

An NFS server

Role Variables
--------------

This only works if nfs_mount variable is not defined

<pre>
nfs_mounts:
 - { fstype: "nfs4", name: "/home", src: "{{ nfs_mount_addr }}:/home", state: "mounted", opts: "defaults" }
 - { name: "/scratch", src: "{{ nfs_mount_addr }}:/scratch", dirmode: "1777" }
</pre>

Notice how fstype defaults to "nfs4", state defaults to "mounted" and opts defaults to "defaults".

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: ansible-role-nfs_mount }

License
-------

MIT

Author Information
------------------
