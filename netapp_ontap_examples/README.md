# Ansible Galaxy galaxy.ansible.com
https://galaxy.ansible.com/netapp/ontap

# connection to repo
https://github.com/ansible-collections/netapp.ontap

# grab version of python supporting ansible
ansible --version

# look to end of python version line
# take the path to python, usually /usr/bin/python3 or /usr/bin/python
# use it to install the requirements file
# https://github.com/ansible-collections/netapp.ontap/blob/main/requirements.txt
/usr/bin/python3 -m pip install -r requirements.txt

# after collection is installed, we can see what we installed with ansible-doc
ansible-doc netapp.ontap -l
ansible-doc netapp.ontap.na_ontap_info


# ontap upgrade firmware example
https://github.com/ansible-collections/netapp.ontap/blob/main/playbooks/examples/na_ontap_pb_upgrade_firmware_with_vars_file.yml


