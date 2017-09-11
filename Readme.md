# dsmachine
Vagrant/Ansible usage to generate a simple - data science machine -
* I'll improve the env_vars part asap (DRY)

## Install necessary packages  (debian based systems)

* Install vagrant

```
 https://releases.hashicorp.com/vagrant/2.0.0/vagrant_2.0.0_x86_64.deb
 sudo dpkg -i vagrant_2.0.0_x86_64.deb

```
* Install virtualbox

```
sudo apt-get install virtualbox
sudo apt-get install virtualbox-dkms
sudo apt-get install virtualbox-guest-dkms
```

* Install ansible

```
sudo apt-get install software-properties-common
sudo apt-add-repository ppa:ansible/ansible
sudo apt-get update
sudo apt-get install ansible
```

### Now generate your data science machine i.e.

You can provision everything direct inside the Vagrant file , but I'd like to have it decoupled

```
* Total installation (not recommended)
vagrant up
ansible-playbook data-science.yml

* Single tags
ansible-playbook data-science.yml --list-tags
ansible-playbook data-science.yml -t base

* Grouped tags
ansible-playbook data-science.yml -t "base,spark,mongodb"

* Install local
ansible-playbook data-science.yml  -i "localhost," -c local -t base
```


#### Contributors
* [Christian Schulz](https://twitter.com/nnfuzzy)