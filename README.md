# VLAB Template for SpringBoot CloudNative FSD

## Prerequisites

- VirtualBox (development and local testing)
- Vagrant (development and local testing)
- Ansible (>2.4, 2.8 preferred) (building image)
- Remmina (development, local and qa testing)
- Packer (building amis in qa and production)
- circleci (for running ci locally)
- docker (for running ci locally)

## Development Instructions

1. Install ansible roles: `ansible-galaxy install -r roles.yml -p roles`
1. Start vagrant: `vagrant up`
1. If you want to test changes after provisioning: `vagrant execute`
1. To connect to the GUI using xrdp, use Remmina with options `Relax Order Checks` and `Glyph Cache`
1. After verifying with vagrant, test CI with `circleci local execute` (requires docker). circleci will only run task named 'build'.

## Build Instructions

1. Configure AWS Credentials: `aws configure`
1. Install ansible roles: `ansible-galaxy install -r roles.yml -p roles`
1. Build image: `packer build template.json`
