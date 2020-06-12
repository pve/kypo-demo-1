# telnet-server-sandbox

A simple sandbox with a Telnet server configured using Ansible variables.

## Usage

1. Run `vagrant up`, then connect to the client using `vagrant ssh client`.
2. At client, run `telnet server <telnet_port>` and login as `<username>` using `<password>`. `telnet_port`, `username` and `password` are variables which default values are set in provisioning/roles/server/defaults/main.yml.
3. Destroy the server machine using `vagrant destroy server -f`.
4. Override the default values of the variables by setting arbitrary (but meaningful) values using a BASH variable and bring up the server again:
```
ANSIBLE_ARGS='--extra-vars "telnet_port=12345 username=user password=123456"' vagrant up server
```
5. At client, connect to the Telnet server from the client using the port number and credentials set in the previous step.
