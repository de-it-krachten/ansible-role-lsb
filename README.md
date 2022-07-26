[![CI](https://github.com/de-it-krachten/ansible-role-lsb/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-lsb/actions?query=workflow%3ACI)


# ansible-role-lsb

Installs all base LSB packages 


## Platforms

Supported platforms

- Red Hat Enterprise Linux 7<sup>1</sup>
- Red Hat Enterprise Linux 8<sup>1</sup>
- CentOS 7
- RockyLinux 8
- OracleLinux 8
- AlmaLinux 8
- Debian 10 (Buster)
- Debian 11 (Bullseye)
- Ubuntu 18.04 LTS
- Ubuntu 20.04 LTS
- Ubuntu 22.04 LTS
- Fedora 35
- Fedora 36

Note:
<sup>1</sup> : no automated testing is performed on these platforms

## Role Variables
### defaults/main.yml
<pre><code>

</pre></code>

### vars/family-RedHat.yml
<pre><code>
# list of lsb packages 
lsb_packages:
  - redhat-lsb-core
</pre></code>

### vars/family-Debian.yml
<pre><code>
# list of lsb packages 
lsb_packages:
  - lsb-base
  - lsb-release
</pre></code>



## Example Playbook
### molecule/default/converge.yml
<pre><code>
- name: sample playbook for role 'lsb'
  hosts: all
  become: "{{ molecule['converge']['become'] | default('yes') }}"
  tasks:
    - name: Include role 'lsb'
      include_role:
        name: lsb
</pre></code>
