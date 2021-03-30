# cockpit-box

| License | Versioning | Build |
| ------- | ---------- | ----- |
| [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) | [![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release) | [![Build status](https://ci.appveyor.com/api/projects/status/ib9snsftkpd30k7e/branch/master?svg=true)](https://ci.appveyor.com/project/nikAizuddin/cockpit-box/branch/master) |

Developer box for [Cockpit](https://github.com/cockpit-project/cockpit) with Dashboard.


## Getting started

```
$ git clone --recursive https://github.com/extra2000/cockpit-box.git
$ cd cockpit-box
```


## Creating Vagrant Box

Copy vagrant file from `vagrant/examples/` and then create the vagrant box (you can change to `--provider=libvirt` if you want to use Libvirt provider):
```
$ cp -v vagrant/examples/Vagrantfile.cockpit-box.fedora-33.x86_64.example vagrant/Vagrantfile.cockpit-box
$ vagrant up --provider=virtualbox
```

Provision the vagrant box which will automatically install Cockpit with dashboard:
```
$ vagrant ssh cockpit-box -- sudo salt-call state.highstate
```
