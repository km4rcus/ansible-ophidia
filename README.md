OPHIDIA
=========

This role helps to install OPHIDIA cluster on Centos 6.5.

Requirements
------------



Role Variables
--------------

ophidia_repository: 
ophidia_version: 
ophidia_db_user: 
ophidia_db_pwd: 
ophidia_db_port: 
ophidia_slurm_partition: 
ophidia_db_name: 
ophidia_dimdb_name: 
ophidia_server_port: 
mysql_root_password: 


Dependencies
------------

None

Example Playbook
----------------

 - hosts: ophidia_server
  user: root
  roles:
    - { role: km4rcus.ophidia, ophidia_node_type: 'server' }

- hosts: ophidia_computes
  user: root
  roles:
    - { role: km4rcus.ophidia, ophidia_node_type: 'compute' }

- hosts: ophidia_ios
  user: root
  roles:
    - { role: km4rcus.ophidia, ophidia_node_type: 'io' }


License
-------

MIT

Author Information
------------------

Marco Mancini