# New to automating pure?
# start by searching galaxy.ansible.com for "pure"
# select the collection that best matches your application
# we'll assume "flash array"

# https://galaxy.ansible.com/purestorage/flasharray

# to find ansible version
ansible --version

# see the file requirements.txt for install steps of prereqs


# now install the collection
ansible-galaxy collection install purestorage.flasharray

# if security does not allow direct installs from galaxy.ansible.com
# clone the repo to your internal GitHub (https://github.com/Pure-Storage-Ansible/FlashArray-Collection)
# 
# if cloning from an internal repo-- replace "https://github.com..." with the location of the repo inside your firewall (on your copy of github)
ansible-galaxy collection install git+https://github.com/Pure-Storage-Ansible/FlashArray-Collection
#
# the above command is the same as running the "typical" command found on galaxy.ansible.com
ansible-galaxy collection install purestorage.flasharray


# now that your collection is installed, run the ansible doc command
# against the namespace.collection
# such as the following (the -l provides a LIST of all modules within that namespace.collection)
# 
ansible-doc purestorage.flasharray -l


# always start testing with an "info" or "facts" module
ansible-doc purestorage.flasharray.purefa_info


# in order to run the solution with your own values...
ansible-playbook playbook.yml -e fa_url=192.168.70.22 -e api_token=abc-def-123-123-123


# RESOURCES

# A large list of solutions only using URI module to FLash array
https://github.com/ColdBird2012/Ansible-playbooks-for-PureStorage/blob/master/ps_ports_info.yml

# role solutions (ok examples)
https://github.com/powerhome/ansiblerole-purefa

# GREAT examples! - Pure & VMWare connection
https://github.com/wwt/pure_ansible_workshop
