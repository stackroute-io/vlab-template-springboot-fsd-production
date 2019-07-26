# VLAB Template for SpringBoot CloudNative FSD

## Development Prerequisites
- VirtualBox
- Vagrant
- Ansible
- Remmina

## Development Instructions

1. Install ansible roles: `ansible-galaxy install -r roles.yml -p roles`
1. Start vagrant: `vagrant up`
1. If you want to test changes after provisioning: `vagrant execute`
1. To connect to the GUI using xrdp, use Remmina with options `Relax Order Checks` and `Glyph Cache`