<!-- DOCSIBLE START -->

# 📃 Role overview

## nebula

```
Role belongs to kasefuchs/general
Namespace - kasefuchs
Collection - general
Version - 1.1.0
Repository - https://codeberg.org/kasefuchs/ansible-collection-general
```

Description: Install and configure Nebula overlay networking, including certificate generation, service setup, and configuration management.


| Field                | Value           |
|--------------------- |-----------------|
| Readme update        | 2026/02/15 |








### Defaults

**These are static variables with lower priority**

#### File: defaults/main/cert.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [nebula_cert_ca_cn](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/cert.yml#L3)   | str | `Nebula CA` |
| [nebula_cert_ca_duration](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/cert.yml#L6)   | str | `87600h` |
| [nebula_cert_host_cn](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/cert.yml#L9)   | str | `{{ inventory_hostname }}` |
| [nebula_cert_host_subnets](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/cert.yml#L12)   | list | `[]` |

#### File: defaults/main/config.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [nebula_config](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L3)   | dict | `{}` |
| [nebula_config.**firewall**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L4)   | str | `{{ nebula_config_firewall }}` |
| [nebula_config.**lighthouse**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L5)   | str | `{{ nebula_config_lighthouse }}` |
| [nebula_config.**listen**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L6)   | str | `{{ nebula_config_listen }}` |
| [nebula_config.**pki**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L7)   | str | `{{ nebula_config_pki }}` |
| [nebula_config.**punchy**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L8)   | str | `{{ nebula_config_punchy }}` |
| [nebula_config.**relay**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L9)   | str | `{{ nebula_config_relay }}` |
| [nebula_config.**static_host_map**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L10)   | str | `{{ nebula_config_static_host_map }}` |
| [nebula_config.**tun**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L11)   | str | `{{ nebula_config_tun }}` |
| [nebula_config_listen](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L14)   | dict | `{}` |
| [nebula_config_listen.**host**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L15)   | str | `0.0.0.0` |
| [nebula_config_listen.**port**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L16)   | int | `4646` |
| [nebula_config_lighthouse](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L19)   | dict | `{}` |
| [nebula_config_lighthouse.**am_lighthouse**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L20)   | bool | `False` |
| [nebula_config_lighthouse.**hosts**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L21)   | str | `{{ nebula_config_lighthouse_list }}` |
| [nebula_config_lighthouse_list](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L24)   | list | `[]` |
| [nebula_config_tun](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L27)   | dict | `{}` |
| [nebula_config_tun.**dev**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L28)   | str | `nebula0` |
| [nebula_config_firewall](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L31)   | dict | `{}` |
| [nebula_config_firewall.**inbound_action**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L32)   | str | `drop` |
| [nebula_config_firewall.**outbound_action**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L33)   | str | `drop` |
| [nebula_config_firewall.**inbound**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L34)   | list | `[]` |
| [nebula_config_firewall.inbound.**0**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L34)   | dict | `{}` |
| [nebula_config_firewall.inbound.0.**host**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L35)   | str | `any` |
| [nebula_config_firewall.inbound.0.**port**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L35)   | str | `any` |
| [nebula_config_firewall.inbound.0.**proto**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L35)   | str | `any` |
| [nebula_config_firewall.**outbound**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L36)   | list | `[]` |
| [nebula_config_firewall.outbound.**0**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L36)   | dict | `{}` |
| [nebula_config_firewall.outbound.0.**host**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L37)   | str | `any` |
| [nebula_config_firewall.outbound.0.**port**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L37)   | str | `any` |
| [nebula_config_firewall.outbound.0.**proto**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L37)   | str | `any` |
| [nebula_config_punchy](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L40)   | dict | `{}` |
| [nebula_config_punchy.**punch**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L41)   | bool | `False` |
| [nebula_config_punchy.**respond**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L42)   | bool | `False` |
| [nebula_config_relay](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L45)   | dict | `{}` |
| [nebula_config_relay.**relays**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L46)   | str | `{{ nebula_config_relay_list }}` |
| [nebula_config_relay.**am_relay**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L47)   | bool | `False` |
| [nebula_config_relay.**use_relays**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L48)   | bool | `True` |
| [nebula_config_relay_list](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L51)   | list | `[]` |
| [nebula_config_static_host_map](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L54)   | dict | `{}` |

#### File: defaults/main/download.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [nebula_download_version](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/download.yml#L3)   | str | `latest` |
| [nebula_download_github_user](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/download.yml#L6)   | str | `slackhq` |
| [nebula_download_github_repository](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/download.yml#L9)   | str | `nebula` |
| [nebula_download_architecture_map](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/download.yml#L12)   | dict | `{}` |
| [nebula_download_architecture_map.**x86_64**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/download.yml#L13)   | str | `amd64` |
| [nebula_download_architecture_map.**aarch64**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/download.yml#L14)   | str | `arm64` |
| [nebula_download_url](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/download.yml#L17)   | str | `https://github.com/{{ nebula_download_github_user }}/{{ nebula_download_github_repository }}/releases/download/v{{ download_version }}/nebula-linux-{{ download_architecture.value }}.tar.gz` |

#### File: defaults/main/install.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [nebula_install_extract_options](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/install.yml#L3)   | list | `[]` |
| [nebula_install_extract_include](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/install.yml#L6)   | list | `[]` |
| [nebula_install_extract_include.**0**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/install.yml#L6)   | str | `nebula` |
| [nebula_install_extract_include.**1**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/install.yml#L6)   | str | `nebula-cert` |


### Vars

**These are variables with higher priority**
#### File: vars/main/cert.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [nebula_cert_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/cert.yml#L3)   | str | `/etc/pki/nebula` |
| [nebula_cert_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/cert.yml#L6)   | str | `{{ (nebula_artifact_local_dir, 'cert') ¦ ansible.builtin.path_join }}` |
#### File: vars/main/config.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [nebula_config_file](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/config.yml#L3)   | str | `{{ (nebula_install_config_dir, 'config.yaml') ¦ ansible.builtin.path_join }}` |
| [nebula_config_pki](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/config.yml#L6)   | dict | `{}` |
| [nebula_config_pki.**ca**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/config.yml#L7)   | str | `{{ (nebula_cert_dir, 'ca.crt') ¦ ansible.builtin.path_join }}` |
| [nebula_config_pki.**key**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/config.yml#L8)   | str | `{{ (nebula_cert_dir, 'node.key') ¦ ansible.builtin.path_join }}` |
| [nebula_config_pki.**cert**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/config.yml#L9)   | str | `{{ (nebula_cert_dir, 'node.crt') ¦ ansible.builtin.path_join }}` |
#### File: vars/main/download.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [nebula_download_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/download.yml#L3)   | str | `{{ (nebula_cache_local_dir, 'download') ¦ ansible.builtin.path_join }}` |
| [nebula_download_local_file](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/download.yml#L6)   | str | `{{ (nebula_download_local_dir, 'current', ansible_facts.architecture) ¦ ansible.builtin.path_join }}` |
#### File: vars/main/install.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [nebula_install_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/install.yml#L3)   | str | `/usr/local/bin` |
| [nebula_install_config_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/install.yml#L6)   | str | `/etc/nebula` |
| [nebula_install_binary](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/install.yml#L9)   | str | `{{ (nebula_install_dir, 'nebula') ¦ ansible.builtin.path_join }}` |
#### File: vars/main/main.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [nebula_cache_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/main.yml#L3)   | str | `{{ (common_cache_local_dir, 'nebula') ¦ ansible.builtin.path_join }}` |
| [nebula_artifact_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/main.yml#L6)   | str | `{{ (common_artifact_local_dir, 'nebula') ¦ ansible.builtin.path_join }}` |


### Tasks


#### File: tasks/cert.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Create Nebula CA certificate](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/cert.yml#L13) | block | False |
| [Create local Nebula certificate directory](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/cert.yml#L7) | ansible.builtin.file | False |
| [Create Nebula CA certificate](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/cert.yml#L13) | ansible.builtin.expect | False |
| [Create Nebula node certificate](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/cert.yml#L25) | block | False |
| [Create node Nebula certificate directory](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/cert.yml#L27) | ansible.builtin.file | False |
| [Create Nebula node keychain](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/cert.yml#L35) | ansible.builtin.command | False |
| [Copy Nebula node public key](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/cert.yml#L41) | ansible.builtin.fetch | False |
| [Sign Nebula node certificate](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/cert.yml#L47) | ansible.builtin.expect | False |
| [Copy Nebula certificates](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/cert.yml#L64) | ansible.builtin.copy | False |

#### File: tasks/config.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Render Nebula config template](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/config.yml#L2) | ansible.builtin.template | False |

#### File: tasks/download.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Get latest Nebula version](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/download.yml#L2) | block | True |
| [Fetch latest Nebula release on GitHub](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/download.yml#L5) | community.general.github_release | False |
| [Set Nebula version fact](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/download.yml#L13) | ansible.builtin.set_fact | False |
| [Download Nebula archive](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/download.yml#L17) | ansible.builtin.include_role | False |

#### File: tasks/install.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Create Nebula directories](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/install.yml#L2) | ansible.builtin.file | False |
| [Extract Nebula archive](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/install.yml#L13) | ansible.builtin.unarchive | False |
| [Install Nebula service](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/install.yml#L23) | block | False |
| [Install Nebula service (systemd)](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/install.yml#L26) | ansible.builtin.template | True |

#### File: tasks/main.yml

| Name | Module | Has Conditions | Tags |
| ---- | ------ | -------------- | -----|
| [Download Nebula](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/main.yml#L2) | ansible.builtin.include_tasks | False | download,packer |
| [Install Nebula](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/main.yml#L12) | ansible.builtin.include_tasks | False | install,packer |
| [Generate Nebula certificates](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/main.yml#L19) | ansible.builtin.include_tasks | False | c,e,r,t |
| [Configure Nebula](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/main.yml#L26) | ansible.builtin.include_tasks | False | c,o,n,f,i,g |
| [Flush handlers](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/main.yml#L33) | ansible.builtin.meta | False | a,l,w,a,y,s |







## Author Information
Kasefuchs

#### License

MIT

#### Minimum Ansible Version

2.2

#### Platforms

No platforms specified.

#### Dependencies

- **kasefuchs.general.common**



<!-- DOCSIBLE END -->
