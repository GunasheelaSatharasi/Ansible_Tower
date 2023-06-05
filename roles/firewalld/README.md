firewalld
=========

## A brief description of the role goes here.

1. Installs firewalld package if not present
2. Configures a rule using firewalld
3. Verifies if the rule is added by outputting value on terminal

Role Variables
--------------

# firewalld variables:

- icmp_block: (string) The ICMP block you would like to add/remove to/from a zone in firewalld.

- icmp_block_inversion: (string) Enable/Disable inversion of ICMP blocks for a zone in firewalld.

- immediate: (boolean) Should this configuration be applied immediately, if set as permanent. Choices: false (default) or true

- interface: (string) The interface you would like to add/remove to/from a zone in firewalld.

- masquerade: (string) The masquerade setting you would like to enable/disable to/from zones within firewalld.

- offline: (boolean)  Whether to run this module even when firewalld is offline. Choices: false or true

- permanent: (boolean) Should this configuration be in the running firewalld configuration or persist across reboots. As of Ansible 2.3, permanent operations can operate on firewalld configs when it is not running (requires firewalld >= 0.3.9).Note that if this is false, immediate is assumed true.

- port: (string) Name of a port or port range to add/remove to/from firewalld. Must be in the form PORT/PROTOCOL or PORT-PORT/PROTOCOL for port ranges.

- rich_rule: (string)  Rich rule to add/remove to/from firewalld. See Syntax for firewalld rich language rules - https://firewalld.org/documentation/man-pages/firewalld.richlanguage.html

- service: (string) Name of a service to add/remove to/from firewalld. The service must be listed in output of firewall-cmd –get-services.

- source: (string) The source/network you would like to add/remove to/from firewalld.

- state: (string) Enable or disable a setting. For ports: Should this port accept (enabled) or reject (disabled) connections. The states present and absent can only be used in zone level operations (i.e. when no other parameters but zone and state are set). Choices: absent, disabled, enabled or present.

- target: (string) firewalld Zone target. If state is set to absent, this will reset the target to default. Choices: default, ACCEPT, DROP or %%REJECT%%

- timeout: (integer)  The amount of time in seconds the rule should be in effect for when non-permanent. Default: 0

- zone: (string) The firewalld zone to add/remove to/from.
Note that the default zone can be configured per system but public is default from upstream.
Available choices can be extended based on per-system configs, listed here are “out of the box” defaults. Possible values include block, dmz, drop, external, home, internal, public, trusted, work.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - firewalld