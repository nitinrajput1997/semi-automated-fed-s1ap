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
sudo chown -R $USER magma/.cache/test_certs
```

### Setup Environment
```
cd magma/lte/gateway/python/integ_tests/federated_tests
fab build_all_and_configure
```
After this has run, you can check whether your gateways have been bootstrapped using the magmad logs on the AGW and FeG. The command below will try to reach Orc8r from AGW and FeG, and FeG from AGW:
```
cd magma/lte/gateway/python/integ_tests/federated_tests
fab test_connectivity
```
Once it has been built, start the magma_trfserver and magma_test VMs:
```
cd magma/lte/gateway
vagrant up magma_test
vagrant up magma_trfserver
```
