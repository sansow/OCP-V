# OCP-V

Automate the migration of 100 VMs from vCenter to OpenShift Virtualization while retaining their IP addresses.
#Prerequisites:
Ansible Installed on your control node.
govc Installed: This is a CLI tool for VMware vCenter that will be used to export VMs.
OpenShift CLI (oc) and virtctl installed on the control node.
Credentials for accessing vCenter and OpenShift.
SSH access to the OpenShift nodes where the VMs will be imported.

#Step 1: Ansible Inventory
Create an inventory file (inventory.yml) with the details of your vCenter and OpenShift environments.

#Step 2: Ansible Playbook
Create an Ansible playbook (migrate_vms.yml) to automate the migration process.

#Step 3: VM Import YAML Template
Create a template (vmimport.yaml.j2) for importing VMs into OpenShift. This is a basic example, and you may need to customize it further.

#Step 4: Execute the Playbook
To execute the migration, run the playbook with the following command:

ansible-playbook -i inventory.yml migrate_vms.yml
