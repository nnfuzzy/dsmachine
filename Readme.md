# dsmachine
Vagrant/Ansible usage to generate a simple - data science machine -


## Install necessary packages  (debian based systems)

* Install vagrant

```
 wget https://releases.hashicorp.com/vagrant/1.8.1/vagrant_1.8.1_x86_64.deb
 sudo dpkg -i vagrant_1.8.1_x86_64.deb

```
* Install virtualbox

```
sudo apt-get install virtualbox
sudo apt-get install virtualbox-dkms
sudo apt-get install virtualbox-guest-dkms
```

* Install ansible

```
pip install ansible
```

### Now generate your data science machine i.e.

You can provision everything direct inside the Vagrant file , but I'd like to have it decoupled

```
vagrant up
ansible playbook dsmachine -t base 

```




#### Contributors
* [Christian Schulz](https://twitter.com/nnfuzzy)
