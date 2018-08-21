# gpupassthrough
an Ansible playbook to setup gpu passthrough to windows vm on a remote fedora 28 host (can be deployed on localhost with some slight modifcations)

Before running this playbook install windows on its own physical drive.
run lspci -nnk to list gpu ids and enable ssh on target. Add the ansible machines keys to the authorized_keys file on target machine. Be sure to update /roles/common/vars/main.yml with you target hosts devices.


After playbook is done, open virt-manager attach gpu and keyboard and mouse. Also for best results install virtIO hdd and nic. Then install virtIO drivers.
