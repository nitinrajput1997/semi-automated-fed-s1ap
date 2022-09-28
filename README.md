# semi-automated-fed-s1ap

### Pre-requisite

Docker, Docker-Compose, Ansible, Fabric3

```
sudo curl -O https://releases.hashicorp.com/vagrant/2.2.19/vagrant_2.2.19_x86_64.deb
sudo apt update
sudo apt install ./vagrant_2.2.19_x86_64.deb
vagrant plugin install vagrant-vbguest vagrant-disksize vagrant-vbguest vagrant-mutate vagrant-reload
sudo apt-get install virtualbox virtualbox-qt
sudo apt install python3-pip
pip3 install --upgrade pip
pip3 install jsonpickle
```

### Clone Magma Repo
```
git clone https://github.com/magma/magma.git
```

### 
