# Install vagrant

# Install plugins
sudo ln -s /opt/VBoxGuestAdditions-4.3.10/lib/VBoxGuestAdditions /usr/lib/VBoxGuestAdditions
vagrant plugin install vagrant-vbguest

# Run  provisioning for a tag
ansible-playbook -t mongodb --private-key=/home/nnfuzzy/project/dev/dmp4vagrant/ansible/.vagrant/machines/default/virtualbox/private_key --user=vagrant --connection=ssh --limit='default' --inventory-file=/home/nnfuzzy/project/dev/dmp4vagrant/ansible/.vagrant/provisioners/ansible/inventory vagrant_provisioning.yml

