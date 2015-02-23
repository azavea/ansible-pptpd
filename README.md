# ansible-pptpd

An Ansible role for installing `pptpd`.

## Role Variables

- `pptpd_version` - `pptpd `version
- `pptpd_connections` - Limit of `pptpd` connections accepted (default: `100`)
- `pptpd_interface` - Interface used for iptables NAT (default: `eth0`)
- `pptpd_localip` - IP address for the `pptpd` server (default: `172.31.0.1`)
- `pptpd_remoteip` - IP address range for the `pptpd` clients (default: `"172.31.0.234-238,172.31.0.245`)
- `pptpd_ms_dns` - List of DNS servers (default: `[ "8.8.8.8", "8.8.4.4" ]`)
- `pptpd_users` - List of `pptpd` users

```yaml
pptpd_users:
  - { client: "username", server: "*", secret: "password", address: "*" }
```

## Example Playbook

See the [examples](./examples/) directory.
