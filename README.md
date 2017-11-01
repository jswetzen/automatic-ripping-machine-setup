Automatic Ripping Machine Ansible Role
=========

An Ansible role that sets up the [Automatic Ripping Machine](https://github.com/ahnooie/automatic-ripping-machine) on Ubuntu Xenial.

Requirements
------------

There are no pre-requisites other than Ubuntu Xenial, but it's recommended to install the A.R.M. inside a virtual machine as it takes over the DVD/Blu-ray drive completely.

Installation instructions that use a Vagrant virtual machine can be found in the README for [A.R.M.](https://github.com/ahnooie/automatic-ripping-machine).

Role Variables
--------------

* ´arm_setup_cifs_user´ CIFS (samba) user to connect as. If left blank, log in as guest.
* ´arm_setup_cifs_password´ CIFS (samba) password.
* ´arm_setup_cifs_path´ CIFS share to mount.
* ´arm_setup_cifs_mount_point´ Where to mount the CIFS share (default: "/mnt/video").
* ´arm_setup_armpath´: Where unidentified ripped movies are stored (default: "/vagrant/Data/Media/Unidentified").
* ´arm_setup_rawpath´: Path for storing raw data (default: "/vagrant/Data/Raw").
* ´arm_setup_media_dir´: Path for storing correctly identified movies (default: "/vagrant/Data/Media/Movies").

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: automatic-ripping-machine }

License
-------

MIT

Author Information
------------------

Created by [Johan Swetén](https://github.com/jswetzen)
Automatic Ripping Machine by [Benjamin Bryan](https://b3n.org)
