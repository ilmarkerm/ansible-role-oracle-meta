oracle-meta
=========

This role maintaims metadata for Oracle RDBMS home management roles. Like what are the configured RDBMS homes and what they should contain.

This role is part of full Oracle RDBMS home management solution:
https://github.com/ilmarkerm/ansible-oracle-home-mgmt

Requirements
------------

Oracle Grid Infrastructure or Oracle Restart is required

Role Variables
--------------

| Variable | Default | Description |
| --- | --- | --- |
| oracle_db_owner | oracle | OS user who runs oracle |
| oracle_db_group | oinstall | OS groups who own oracle installation |
| oracle_dba_group | dba | OS group with SYSDBA/SYSDG/SYSKMS/SYSBACKUP privileges |
| oracle_osasm_group | osasm | OS group with SYSASM privileges |
| oracle_base | /u01/app/oracle | $ORACLE_BASE | 
| oracle_inventory_location | /u01/app/oraInventory | Oracle inventory location |
| oracle_tnsnames_common_path | /u02/app/oracle | Shared location within a cluster where common sqlnet.ora and tnsnames.ora are located |
| oracle_link_tns | True | Should sqlnet.ora and tnsnames.ora be linked from a common path to $ORACLE_HOME/network/admin |
| oracle_installer_base | /nfs/install/base_installers | Shared location mounted on all database hosts where database installers are unzipped |
| oracle_patch_base: | /nfs/install/patch | Shared location mounted on all database hosts where database patch files are unzipped |
| oracle_os_common_path | /usr/lib64/qt-3.3/bin:/usr/local/bin:/bin:/usr/bin:/usr/local/sbin:/usr/sbin:/sbin:/home/oracle/bin | PATH for oracle OS user that does not include $ORACLE_HOME |
| oracle_meta_generic_groups | ['non-prod','production'] | List containing all hostgroups in Ansible inventory file, that are NOT clusters. For example groups that contain clusters. | 

Example Playbook
----------------

Check out playbook and full Oracle RDBMS home management solution example here: https://github.com/ilmarkerm/ansible-oracle-home-mgmt

License
-------

Apache 2.0

Author Information
------------------

Ilmar Kerm, ilmar.kerm@gmail.com
https://ilmarkerm.eu
