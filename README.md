# gpupassthrough
an Ansible playbook to setup gpu passthrough to windows vm on a fedora 28 host 

Before running this playbook install windows on its own physical drive.
run lspci -nnk to list gpu ids and enable ssh on target. Add the ansible machines keys to the authorized_keys file on target machine.
