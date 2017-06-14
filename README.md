OMERO Ansible Examples
----------------------

## Quick start ##

- Install `ansible`: e.g. `pip install ansible`
- Install roles: `ansible-galaxy install -r requirements.yml -p roles`
- Install OMERO server and setup public user: `ansible-playbook EXAMPLE.yml`

## Example: all-in-one ##

Starts all required OMERO services on a single host.

## Example: two-nodes ##

Starts all required OMERO services placing PostgreSQL
on a separate host from OMERO.server and OMERO.web.

## Example: public-user ##

This example recreates the configuration documented under
https://www.openmicroscopy.org/site/support/omero/sysadmins/public.html

Playbooks and the associated requirements.yml files can be used for
creating a basic OMERO configuration with a public user `public`. Most
likely you will want to copy the configuration into your own playbooks.
