# Demo packer
Demo Packer / Vagrant build

Run the Packer command 
```
packer build -only virtualbox-iso packer.json
```
Builds an image for use with vagrant

Packer template runs the Ubuntu install process with a seed file.
Once complete the SSH provisioner runs and installs postgresql as an example.
The output is a box file for use in vagrant

## Next steps
Use Ansible provisioner rather than SSH

Use a another builder to send image to cloud e.g. AWS or Azure

### Requires ubuntu-18.04.1-live-server-amd64 in the root

