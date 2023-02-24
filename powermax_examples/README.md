# start by searching galaxy.ansible.com
https://galaxy.ansible.com/dellemc/powermax

# install the collection
ansible-galaxy collection install dellemc.powermax

# check out the repo (see upper right corner of collection page on galaxy)
https://github.com/dell/ansible-powermax/

# look @ requirements.txt (this is Python requirements)

# if any are listed in requirements.txt, first get the python interpreter supporting your app
ansible --version

# look @ the end of the line "python version"...
# use that python path to customize the following command
/usr/bin/python3 -m pip install -r requirements.txt
<python path> -m pip install -r requirements.txt

# The python path really is only necessary to prevent installing the python requirements to the 
# CORRECT version of python that ansible is using. The only time this is ia concern, is if you have
# python multihomed (i.e multiple version of python on your system)


# so IF requirements.yml exists, this is ANSIBLE dependencies
ansible-galaxy install -r requirements.yml
