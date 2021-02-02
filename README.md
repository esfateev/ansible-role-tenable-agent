# ansible-role-tenable-agent

Ansible role for installing and configuring Nessus Agent

## Role Variables

- `nessus_agent_key`: key used for linking with nessus host (this is a required variable)
- `nessus_agent_group`: host group this agent should be added to when linking with nessus host (this is a required variable)
- `nessus_agent_host`: nessus host to link with (default: `cloud.tenable.com`)
- `nessus_agent_port`: nessus host port (default: `443`)
- `nessus_agent_download_url`
- `nessus_agent_package`: can be either a repository package, path to a file, or a URL (default: `NessusAgent`)
  - nessus_agent_package: nessus-agent
  - nessus_agent_package: /tmp/nessus-agent_6.8.1_amd64.deb

## Dependencies

None.

## Example Playbook

## Simple usecase

```yaml
- hosts: all

  vars:
    nessus_agent_key: xxxxxxxxx
    tags: nessus-agent

  roles:
     - role: ansible-role-nessus-agent
```

## Advanced usecase

```yaml
- hosts: all

  vars:
    nessus_agent_key: xxxxxxxxx
    tags: nessus-agent

  roles:
     - role: ansible-role-nessus-agent
```

## TODOs

- Add entries to /opt/nessus_agent/etc/nessus/nessusd.rules - <https://community.tenable.com/s/article/What-is-the-Nessus-rules-file>
- Fixup
- CI & Tests
- Release Pipeline
