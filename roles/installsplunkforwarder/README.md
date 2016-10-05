Role Name
=========

A installer/upgrader for Splunk forwarder role.

Requirements
------------

A Splunk server, at least one Splunk forwarder, the latest Splunk DEB and/or RPM package, and a text editor to edit a variable file (splunk-forwarder-version.yml).

You will need to:
   * Download the latest Splunk forwarder DEB and RPM packages
   * Copy that package into the /files/ directory
   * Edit the file vars/splunk-forwarder-version.yml and include
     the new version and build numbers from the file DEB package name.
   * Edit the file vars/splunk-servers.yml and include Splunk servers in the 
     splunkservers variable

Role Variables
--------------

The splunkforwarderversion variable in vars/splunk-forwarder-version.yml contains the version and build number for the Splunk package. It is used to test if the lates t version of Splunk is already installed, and finding the package name.
The splunkservers variable in vars/splunk-servers.yml contains a list of Splunk servers.

Dependencies
------------

None.

Example Playbook
----------------

```yml
- hosts: splunkforwarders
  become: true
  roles:
    - installsplunkforwarder
```

License
-------

GPLv3

Author Information
------------------

Troy Johnson
troy@jdmz.net
http://troy.jdmz.net/

