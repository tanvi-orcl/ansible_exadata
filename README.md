# Ansible for Exadata

This ansible project allows for Exadata Cloud@Customer and Exadata Cloud Service set-up. 

## Getting Started

### AWX Set-Up

1. Set-up AWX

2. Create project
    - Sync Git Repo
    - Sync Dynamic Inventory

### Additional Set-Up


## Using Ansible

### Running a Playbook
 
    1. Create a Job Template
    
    2. Define Variables
        - vars_file: File name for variables to be used for that playbook. Workload specfic. Be sure to edit these files to set variables such as workload_tag (used for naming resources) and database parameters. Path to the vars_file has already been included, just have to provide the actual file name. 
        - hostgroup: Host group to run DB operations on. Currently only required for PDB operations (other playbooks are for provisioning so use localhost).
        - additional variables: These variables are only defined at runtime, not stored in a file. Check out the Playbooks below for instructions on which plays require additional variables.

## Playbooks

basic_test.yml
- Description
- Required Variables
    - vars_file
    - hostgroup

dataguard_setup.yml
- Description
- Required Variables
    - vars_file
    - db_admin_password

db_backup.yml
- Description
- Required Variables
    - vars_file

db_create.yml
- Description
- Required Variables
    - vars_file
    - db_admin_password

db_home_create.yml
- Description
- Required Variables
    - vars_file

db_teardown.yml
- Description
- Required Variables
    - vars_file

exacc_setup.yml
- Description
- Required Variables
    - vars_file

exacs_setup.yml
- Description
- Required Variables
    - vars_file

networking_setup.yml
- Description
- Required Variables
    - vars_file

networking_teardown.yml
- Description
- Required Variables
    - vars_file

pdb_create.yml
- Description
- Required Variables
    - vars_file
    - hostgroup
    - pdb_password

pdb_delete.yml
- Description
- Required Variables
    - vars_file
    - hostgroup


## Roles