# Ansible-Role-gpupassthrough
an Ansible playbook to setup gpu passthrough to windows vm on a remote fedora 28 host (can be deployed on localhost with some slight modifcations)

Before running this playbook install windows on its own physical drive.
run lspci -nnk to list gpu ids and enable ssh on target. Add the ansible machines keys to the authorized_keys file on target machine. Be sure to update /roles/common/vars/main.yml with you target hosts devices.


After playbook is done, open virt-manager attach gpu, keyboard and mouse. Also for best results install virtIO hdd and nic. Then install virtIO drivers.

##### Before running this please insure IOMMU is enabled in UEFI
#####  Run dnf update on target system prior to running this playbook
##### For best results install windows 10 on a seperate SSD and use the latest VirtIO drivers
##### Also Look into CPU pinning for your model CPU
##### If you are using to Identical GPUS you will have to do some additional setup
