////--  Run Ansible PlayBook --////

Before running .yml file on target server copy id, on target server using ssh-copy-id.
#ssh-copy-id <AD_ID>@<Target_Server>

////--- Execute Playbook -- ////
#ansible-playbook <PlayBookFileName>.yml -i <PathToHostFileName>/hosts

####
#When sudo to root require password use option -K
####
ansible-playbook <PlayBookFileName>.yml -i <PathToHostFileName>/hosts -K

####
## Execute command for the tag
####
ansible-playbook -i<PathToHostFileName>/hosts <PlyaBookFileName>.yml --tags "<tagName>"
