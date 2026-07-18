<!-- DOCSIBLE START -->

# 📃 Role overview

## tailscale

```
Role belongs to kasefuchs/general
Namespace - kasefuchs
Collection - general
Version - 1.3.0
Repository - https://codeberg.org/kasefuchs/ansible-collection-general
```

Description: Install and configure Tailscale mesh VPN, including automated login, service setup, and runtime configuration. #magic___^_^___line


| Field                | Value           |
|--------------------- |-----------------|
| Readme update        | 2026/02/15 |








### Defaults

**These are static variables with lower priority**

#### File: defaults/main/config.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [tailscale_config_flags](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/config.yml#L2)   | list | `[]` |
| [tailscale_config_flags.**0**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/config.yml#L3)   | str | `--accept-routes` |
| [tailscale_config_flags.**1**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/config.yml#L4)   | str | `--advertise-exit-node` |
| [tailscale_config_flags.**2**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/config.yml#L5)   | str | `--webclient` |
| [tailscale_config_auth_key](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/config.yml#L8)   | str | `{{ undef('Tailscale auth key must be provided (tailscale_config_auth_key)') }}` |
| [tailscale_config_login_server](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/config.yml#L11)   | str | `https://controlplane.tailscale.com` |
| [tailscale_config_advertise_tags](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/config.yml#L14)   | list | `[]` |
| [tailscale_config_advertise_tags.**0**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/config.yml#L15)   | str | `server` |

#### File: defaults/main/download.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [tailscale_download_version](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/download.yml#L2)   | str | `latest` |
| [tailscale_download_github_user](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/download.yml#L5)   | str | `tailscale` |
| [tailscale_download_github_repository](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/download.yml#L8)   | str | `tailscale` |
| [tailscale_download_architecture_map](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/download.yml#L11)   | dict | `{}` |
| [tailscale_download_architecture_map.**x86_64**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/download.yml#L12)   | str | `amd64` |
| [tailscale_download_architecture_map.**aarch64**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/download.yml#L13)   | str | `arm64` |
| [tailscale_download_url](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/download.yml#L16)   | str | `https://pkgs.tailscale.com/stable/tailscale_{{ download_version }}_{{ download_architecture.value }}.tgz` |

#### File: defaults/main/install.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [tailscale_install_extract_options](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/install.yml#L2)   | list | `[]` |
| [tailscale_install_extract_options.**0**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/install.yml#L3)   | str | `--strip-components=1` |
| [tailscale_install_extract_options.**1**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/install.yml#L4)   | str | `--wildcards` |
| [tailscale_install_extract_include](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/install.yml#L7)   | list | `[]` |
| [tailscale_install_extract_include.**0**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/install.yml#L8)   | str | `tailscale_*/tailscale` |
| [tailscale_install_extract_include.**1**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/install.yml#L9)   | str | `tailscale_*/tailscaled` |


### Vars

**These are variables with higher priority**
#### File: vars/main/download.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [tailscale_download_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/vars/main/download.yml#L2)   | str | `{{ (tailscale_cache_local_dir, 'download') ¦ path_join }}` |
| [tailscale_download_local_file](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/vars/main/download.yml#L5)   | str | `{{ (tailscale_download_local_dir, 'current', ansible_facts.architecture) ¦ path_join }}` |
#### File: vars/main/install.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [tailscale_install_binary](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/vars/main/install.yml#L2)   | str | `{{ (common_binary_dir, 'tailscale') ¦ path_join }}` |
| [tailscale_install_daemon_binary](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/vars/main/install.yml#L5)   | str | `{{ (common_binary_dir, 'tailscaled') ¦ path_join }}` |
#### File: vars/main/main.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [tailscale_cache_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/vars/main/main.yml#L2)   | str | `{{ (common_cache_local_dir, 'tailscale') ¦ path_join }}` |
| [tailscale_artifact_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/vars/main/main.yml#L5)   | str | `{{ (common_artifact_local_dir, 'tailscale') ¦ path_join }}` |


### Tasks


#### File: tasks/config.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Get Tailscale status](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/tasks/config.yml#L1) | ansible.builtin.command | False |
| [Bring Tailscale up](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/tasks/config.yml#L8) | ansible.builtin.command | True |
| [Configure Tailscale](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/tasks/config.yml#L15) | ansible.builtin.command | True |

#### File: tasks/download.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Get latest Tailscale version](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/tasks/download.yml#L1) | block | True |
| [Fetch latest Tailscale release on GitHub](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/tasks/download.yml#L4) | community.general.github_release | False |
| [Set Tailscale version fact](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/tasks/download.yml#L12) | ansible.builtin.set_fact | False |
| [Download Tailscale archive](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/tasks/download.yml#L16) | ansible.builtin.include_role | False |

#### File: tasks/install.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Extract Tailscale archive](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/tasks/install.yml#L1) | ansible.builtin.unarchive | False |
| [Install Tailscale service](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/tasks/install.yml#L11) | block | False |
| [Install Tailscale service (systemd)](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/tasks/install.yml#L16) | ansible.builtin.template | True |

#### File: tasks/main.yml

| Name | Module | Has Conditions | Tags |
| ---- | ------ | -------------- | -----|
| [Download Tailscale](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/tasks/main.yml#L1) | ansible.builtin.include_tasks | False | download,packer |
| [Install Tailscale](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/tasks/main.yml#L15) | ansible.builtin.include_tasks | False | install,packer |
| [Configure Tailscale](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/tasks/main.yml#L26) | ansible.builtin.include_tasks | False | c,o,n,f,i,g |
| [Flush handlers](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/tasks/main.yml#L33) | ansible.builtin.meta | False | a,l,w,a,y,s |







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
