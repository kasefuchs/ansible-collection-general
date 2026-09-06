<!-- DOCSIBLE START -->

# 📃 Role overview

## amneziawg

```
Role belongs to kasefuchs/general
Namespace - kasefuchs
Collection - general
Version - 1.3.1
Repository - https://codeberg.org/kasefuchs/ansible-collection-general
```

Description: Install and configure AmneziaWG using amneziawg-go and amneziawg-tools with systemd integration.


| Field                | Value           |
|--------------------- |-----------------|
| Readme update        | 2026/02/15 |








### Defaults

**These are static variables with lower priority**

#### File: defaults/main/config.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [amneziawg_config_instance](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/config.yml#L2)   | str | `awg0` |
| [amneziawg_config_interface](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/config.yml#L5)   | str | `{{ undef('AmneziaWG interface configuration must be provided (amneziawg_config_interface)') }}` |
| [amneziawg_config_peers](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/config.yml#L8)   | list | `[]` |
| [amneziawg_config_junk](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/config.yml#L11)   | dict | `{}` |
| [amneziawg_config_paddings](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/config.yml#L14)   | list | `[]` |
| [amneziawg_config_headers](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/config.yml#L17)   | list | `[]` |
| [amneziawg_config_signatures](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/config.yml#L20)   | list | `[]` |

#### File: defaults/main/download.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [amneziawg_download_go_version](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/download.yml#L2)   | str | `0.2.16` |
| [amneziawg_download_go_architecture_map](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/download.yml#L5)   | dict | `{}` |
| [amneziawg_download_go_architecture_map.**x86_64**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/download.yml#L6)   | str | `amd64` |
| [amneziawg_download_go_architecture_map.**aarch64**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/download.yml#L7)   | str | `arm64` |
| [amneziawg_download_go_url](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/download.yml#L10)   | str | `https://dl.kasefuchs.net/amneziawg-go/amneziawg-go_{{ download_url_version }}_linux_{{ arch.value }}.tar.gz` |
| [amneziawg_download_tools_version](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/download.yml#L13)   | str | `1.0.20250903` |
| [amneziawg_download_tools_architecture_map](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/download.yml#L16)   | dict | `{}` |
| [amneziawg_download_tools_architecture_map.**x86_64**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/download.yml#L17)   | str | `x86_64` |
| [amneziawg_download_tools_architecture_map.**aarch64**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/download.yml#L18)   | str | `aarch64` |
| [amneziawg_download_tools_url](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/download.yml#L21)   | str | `https://dl.kasefuchs.net/amneziawg-tools/awg-v{{ download_url_version }}-{{ arch.value }}-linux-musl.tar.gz` |

#### File: defaults/main/install.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [amneziawg_install_go_extract_options](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/install.yml#L2)   | list | `[]` |
| [amneziawg_install_go_extract_include](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/install.yml#L5)   | list | `[]` |
| [amneziawg_install_go_extract_include.**0**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/install.yml#L6)   | str | `amneziawg-go` |
| [amneziawg_install_tools_extract_options](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/install.yml#L9)   | list | `[]` |
| [amneziawg_install_tools_extract_include](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/install.yml#L12)   | list | `[]` |
| [amneziawg_install_tools_extract_include.**0**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/install.yml#L12)   | str | `awg` |
| [amneziawg_install_tools_extract_include.**1**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/install.yml#L14)   | str | `awg-quick` |


### Vars

**These are variables with higher priority**
#### File: vars/main/config.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [amneziawg_config_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/config.yml#L2)   | str | `/etc/amnezia/amneziawg` |
| [amneziawg_config_file](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/config.yml#L5)   | str | `{{ (amneziawg_config_dir, amneziawg_config_instance ~ '.conf') ¦ path_join }}` |
#### File: vars/main/download.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [amneziawg_download_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/download.yml#L2)   | str | `{{ (amneziawg_cache_local_dir, 'download') ¦ path_join }}` |
| [amneziawg_download_go_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/download.yml#L5)   | str | `{{ (amneziawg_download_local_dir, 'go') ¦ path_join }}` |
| [amneziawg_download_go_local_file](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/download.yml#L8)   | str | `{{ (amneziawg_download_go_local_dir, 'current', ansible_facts.architecture) ¦ path_join }}` |
| [amneziawg_download_tools_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/download.yml#L11)   | str | `{{ (amneziawg_download_local_dir, 'tools') ¦ path_join }}` |
| [amneziawg_download_tools_local_file](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/download.yml#L14)   | str | `{{ (amneziawg_download_tools_local_dir, 'current', ansible_facts.architecture) ¦ path_join }}` |
#### File: vars/main/install.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [amneziawg_install_binary](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/install.yml#L2)   | str | `{{ (common_binary_dir, 'awg') ¦ path_join }}` |
| [amneziawg_install_script](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/install.yml#L5)   | str | `{{ (common_binary_dir, 'awg-quick') ¦ path_join }}` |
#### File: vars/main/main.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [amneziawg_cache_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/main.yml#L2)   | str | `{{ (common_cache_local_dir, 'amneziawg') ¦ path_join }}` |
| [amneziawg_artifact_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/main.yml#L5)   | str | `{{ (common_artifact_local_dir, 'amneziawg') ¦ path_join }}` |


### Tasks


#### File: tasks/config.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Render AmneziaWG config template](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/tasks/config.yml#L1) | ansible.builtin.template | False |

#### File: tasks/download.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Download AmneziaWG go](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/tasks/download.yml#L1) | ansible.builtin.include_role | False |
| [Download AmneziaWG tools](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/tasks/download.yml#L10) | ansible.builtin.include_role | False |

#### File: tasks/install.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Create AmneziaWG directories](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/tasks/install.yml#L1) | ansible.builtin.file | False |
| [Extract AmneziaWG go archive](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/tasks/install.yml#L11) | ansible.builtin.unarchive | False |
| [Install AmneziaWG tools](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/tasks/install.yml#L21) | block | False |
| [Extract AmneziaWG tools archive](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/tasks/install.yml#L23) | ansible.builtin.unarchive | False |
| [Install AmneziaWG service](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/tasks/install.yml#L33) | block | False |
| [Install AmneziaWG service (systemd)](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/tasks/install.yml#L36) | ansible.builtin.template | True |

#### File: tasks/main.yml

| Name | Module | Has Conditions | Tags |
| ---- | ------ | -------------- | -----|
| [Download AmneziaWG](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/tasks/main.yml#L1) | ansible.builtin.include_tasks | False | download,packer |
| [Install AmneziaWG](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/tasks/main.yml#L15) | ansible.builtin.include_tasks | False | install,packer |
| [Configure AmneziaWG](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/tasks/main.yml#L26) | ansible.builtin.include_tasks | False | c,o,n,f,i,g |
| [Flush handlers](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/tasks/main.yml#L33) | ansible.builtin.meta | False | a,l,w,a,y,s |







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
