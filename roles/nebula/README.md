<!-- DOCSIBLE START -->

# 📃 Role overview

## nebula

```
Role belongs to kasefuchs/general
Namespace - kasefuchs
Collection - general
Version - 1.3.1
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
| [nebula_cert_ca_cn](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/cert.yml#L2)   | str | `Nebula CA` |
| [nebula_cert_ca_duration](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/cert.yml#L5)   | str | `87600h` |
| [nebula_cert_host_cn](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/cert.yml#L8)   | str | `{{ inventory_hostname }}` |
| [nebula_cert_host_subnets](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/cert.yml#L11)   | list | `[]` |

#### File: defaults/main/config.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [nebula_config](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L2)   | dict | `{}` |
| [nebula_config.**firewall**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L3)   | str | `{{ nebula_config_firewall }}` |
| [nebula_config.**lighthouse**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L4)   | str | `{{ nebula_config_lighthouse }}` |
| [nebula_config.**listen**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L5)   | str | `{{ nebula_config_listen }}` |
| [nebula_config.**pki**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L6)   | str | `{{ nebula_config_pki }}` |
| [nebula_config.**punchy**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L7)   | str | `{{ nebula_config_punchy }}` |
| [nebula_config.**relay**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L8)   | str | `{{ nebula_config_relay }}` |
| [nebula_config.**static_host_map**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L9)   | str | `{{ nebula_config_static_host_map }}` |
| [nebula_config.**tun**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L10)   | str | `{{ nebula_config_tun }}` |
| [nebula_config_listen](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L13)   | dict | `{}` |
| [nebula_config_listen.**host**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L14)   | str | `0.0.0.0` |
| [nebula_config_listen.**port**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L15)   | int | `4646` |
| [nebula_config_lighthouse](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L18)   | dict | `{}` |
| [nebula_config_lighthouse.**am_lighthouse**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L19)   | bool | `False` |
| [nebula_config_lighthouse.**hosts**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L20)   | str | `{{ nebula_config_lighthouse_list }}` |
| [nebula_config_lighthouse_list](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L23)   | list | `[]` |
| [nebula_config_tun](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L26)   | dict | `{}` |
| [nebula_config_tun.**dev**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L27)   | str | `nebula0` |
| [nebula_config_firewall](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L30)   | dict | `{}` |
| [nebula_config_firewall.**inbound_action**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L31)   | str | `drop` |
| [nebula_config_firewall.**outbound_action**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L32)   | str | `drop` |
| [nebula_config_firewall.**inbound**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L33)   | list | `[]` |
| [nebula_config_firewall.inbound.**0**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L34)   | dict | `{}` |
| [nebula_config_firewall.inbound.0.**host**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L34)   | str | `any` |
| [nebula_config_firewall.inbound.0.**port**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L35)   | str | `any` |
| [nebula_config_firewall.inbound.0.**proto**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L36)   | str | `any` |
| [nebula_config_firewall.**outbound**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L37)   | list | `[]` |
| [nebula_config_firewall.outbound.**0**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L38)   | dict | `{}` |
| [nebula_config_firewall.outbound.0.**host**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L38)   | str | `any` |
| [nebula_config_firewall.outbound.0.**port**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L39)   | str | `any` |
| [nebula_config_firewall.outbound.0.**proto**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L40)   | str | `any` |
| [nebula_config_punchy](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L43)   | dict | `{}` |
| [nebula_config_punchy.**punch**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L44)   | bool | `False` |
| [nebula_config_punchy.**respond**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L45)   | bool | `False` |
| [nebula_config_relay](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L48)   | dict | `{}` |
| [nebula_config_relay.**relays**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L49)   | str | `{{ nebula_config_relay_list }}` |
| [nebula_config_relay.**am_relay**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L50)   | bool | `False` |
| [nebula_config_relay.**use_relays**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L51)   | bool | `True` |
| [nebula_config_relay_list](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L54)   | list | `[]` |
| [nebula_config_static_host_map](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L57)   | dict | `{}` |

#### File: defaults/main/download.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [nebula_download_version](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/download.yml#L2)   | str | `latest` |
| [nebula_download_github_user](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/download.yml#L5)   | str | `slackhq` |
| [nebula_download_github_repository](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/download.yml#L8)   | str | `nebula` |
| [nebula_download_architecture_map](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/download.yml#L11)   | dict | `{}` |
| [nebula_download_architecture_map.**x86_64**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/download.yml#L12)   | str | `amd64` |
| [nebula_download_architecture_map.**aarch64**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/download.yml#L13)   | str | `arm64` |
| [nebula_download_url](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/download.yml#L16)   | str | `https://github.com/{{ nebula_download_github_user }}/{{ nebula_download_github_repository }}/releases/download/v{{ download_url_version }}/nebula-linux-{{ arch.value }}.tar.gz` |

#### File: defaults/main/install.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [nebula_install_extract_options](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/install.yml#L2)   | list | `[]` |
| [nebula_install_extract_include](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/install.yml#L5)   | list | `[]` |
| [nebula_install_extract_include.**0**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/install.yml#L5)   | str | `nebula` |
| [nebula_install_extract_include.**1**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/install.yml#L7)   | str | `nebula-cert` |


### Vars

**These are variables with higher priority**
#### File: vars/main/cert.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [nebula_cert_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/cert.yml#L2)   | str | `/etc/pki/nebula` |
| [nebula_cert_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/cert.yml#L5)   | str | `{{ (nebula_artifact_local_dir, 'cert') ¦ path_join }}` |
#### File: vars/main/config.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [nebula_config_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/config.yml#L2)   | str | `/etc/nebula` |
| [nebula_config_file](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/config.yml#L5)   | str | `{{ (nebula_config_dir, 'config.yaml') ¦ path_join }}` |
| [nebula_config_pki](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/config.yml#L8)   | dict | `{}` |
| [nebula_config_pki.**ca**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/config.yml#L9)   | str | `{{ (nebula_cert_dir, 'ca.crt') ¦ path_join }}` |
| [nebula_config_pki.**key**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/config.yml#L10)   | str | `{{ (nebula_cert_dir, 'node.key') ¦ path_join }}` |
| [nebula_config_pki.**cert**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/config.yml#L11)   | str | `{{ (nebula_cert_dir, 'node.crt') ¦ path_join }}` |
#### File: vars/main/download.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [nebula_download_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/download.yml#L2)   | str | `{{ (nebula_cache_local_dir, 'download') ¦ path_join }}` |
| [nebula_download_local_file](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/download.yml#L5)   | str | `{{ (nebula_download_local_dir, 'current', ansible_facts.architecture) ¦ path_join }}` |
#### File: vars/main/install.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [nebula_install_binary](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/install.yml#L2)   | str | `{{ (common_binary_dir, 'nebula') ¦ path_join }}` |
#### File: vars/main/main.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [nebula_cache_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/main.yml#L2)   | str | `{{ (common_cache_local_dir, 'nebula') ¦ path_join }}` |
| [nebula_artifact_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/main.yml#L5)   | str | `{{ (common_artifact_local_dir, 'nebula') ¦ path_join }}` |


### Tasks


#### File: tasks/cert.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Create Nebula CA certificate](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/cert.yml#L12) | block | False |
| [Create local Nebula certificate directory](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/cert.yml#L6) | ansible.builtin.file | False |
| [Create Nebula CA certificate](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/cert.yml#L12) | ansible.builtin.expect | False |
| [Create Nebula node certificate](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/cert.yml#L22) | block | False |
| [Create node Nebula certificate directory](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/cert.yml#L24) | ansible.builtin.file | False |
| [Create Nebula node keychain](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/cert.yml#L32) | ansible.builtin.command | False |
| [Copy Nebula node public key](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/cert.yml#L38) | ansible.builtin.fetch | False |
| [Sign Nebula node certificate](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/cert.yml#L44) | ansible.builtin.expect | False |
| [Copy Nebula certificates](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/cert.yml#L56) | ansible.builtin.copy | False |

#### File: tasks/config.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Render Nebula config template](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/config.yml#L1) | ansible.builtin.template | False |

#### File: tasks/download.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Get latest Nebula version](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/download.yml#L1) | block | True |
| [Fetch latest Nebula release on GitHub](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/download.yml#L4) | community.general.github_release | False |
| [Set Nebula version fact](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/download.yml#L12) | ansible.builtin.set_fact | False |
| [Download Nebula archive](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/download.yml#L16) | ansible.builtin.include_role | False |

#### File: tasks/install.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Create Nebula directories](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/install.yml#L1) | ansible.builtin.file | False |
| [Extract Nebula archive](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/install.yml#L11) | ansible.builtin.unarchive | False |
| [Install Nebula service](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/install.yml#L21) | block | False |
| [Install Nebula service (systemd)](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/install.yml#L24) | ansible.builtin.template | True |

#### File: tasks/main.yml

| Name | Module | Has Conditions | Tags |
| ---- | ------ | -------------- | -----|
| [Download Nebula](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/main.yml#L1) | ansible.builtin.include_tasks | False | download,packer |
| [Install Nebula](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/main.yml#L15) | ansible.builtin.include_tasks | False | install,packer |
| [Generate Nebula certificates](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/main.yml#L26) | ansible.builtin.include_tasks | False | c,e,r,t |
| [Configure Nebula](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/main.yml#L33) | ansible.builtin.include_tasks | False | c,o,n,f,i,g |
| [Flush handlers](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/tasks/main.yml#L40) | ansible.builtin.meta | False | a,l,w,a,y,s |







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
