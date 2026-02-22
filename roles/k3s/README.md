<!-- DOCSIBLE START -->

# 📃 Role overview

## k3s

```
Role belongs to kasefuchs/general
Namespace - kasefuchs
Collection - general
Version - 1.1.0
Repository - https://codeberg.org/kasefuchs/ansible-collection-general
```

Description: Install and configure K3s Kubernetes distribution, including server and agent modes with download, installation and configuration management.


| Field                | Value           |
|--------------------- |-----------------|
| Readme update        | 2026/02/15 |








### Defaults

**These are static variables with lower priority**

#### File: defaults/main/agent/config.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [k3s_agent_config_token](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/agent/config.yml#L3)   | str | `{{ undef('K3s agent token must be provided (k3s_agent_config_token)') }}` |
| [k3s_agent_config](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/agent/config.yml#L6)   | dict | `{}` |
| [k3s_agent_config.**token**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/agent/config.yml#L7)   | str | `{{ k3s_agent_config_token }}` |

#### File: defaults/main/agent/main.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [k3s_agent_group](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/agent/main.yml#L3)   | str | `k3s_agent` |

#### File: defaults/main/download.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [k3s_download_version](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml#L3)   | str | `latest` |
| [k3s_download_github_user](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml#L6)   | str | `k3s-io` |
| [k3s_download_github_repository](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml#L9)   | str | `k3s` |
| [k3s_download_architecture_map](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml#L12)   | dict | `{}` |
| [k3s_download_architecture_map.**x86_64**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml#L13)   | str | `amd64` |
| [k3s_download_architecture_map.**aarch64**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml#L14)   | str | `arm64` |
| [k3s_download_binary_url](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml#L17)   | str | `<multiline value: folded>` |
| [k3s_download_script_url](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml#L26)   | str | `https://raw.githubusercontent.com/{{ k3s_download_github_user }}/{{ k3s_download_github_repository }}/refs/tags/v{{ download_version }}/install.sh` |

#### File: defaults/main/server/config.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [k3s_server_config](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/server/config.yml#L3)   | dict | `{}` |

#### File: defaults/main/server/main.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [k3s_server_group](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/server/main.yml#L3)   | str | `k3s_server` |


### Vars

**These are variables with higher priority**
#### File: vars/main/config.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [k3s_config_file](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/config.yml#L3)   | str | `{{ (k3s_install_config_dir, 'config.yaml') ¦ ansible.builtin.path_join }}` |
#### File: vars/main/download.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [k3s_download_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/download.yml#L3)   | str | `{{ (k3s_cache_local_dir, 'download') ¦ ansible.builtin.path_join }}` |
| [k3s_download_binary_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/download.yml#L6)   | str | `{{ (k3s_download_local_dir, 'binary') ¦ ansible.builtin.path_join }}` |
| [k3s_download_binary_local_file](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/download.yml#L9)   | str | `{{ (k3s_download_binary_local_dir, 'current', ansible_facts.architecture) ¦ ansible.builtin.path_join }}` |
| [k3s_download_script_local_file](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/download.yml#L12)   | str | `{{ (k3s_download_script_local_dir, 'current', ansible_facts.architecture) ¦ ansible.builtin.path_join }}` |
| [k3s_download_script_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/download.yml#L15)   | str | `{{ (k3s_download_local_dir, 'script') ¦ ansible.builtin.path_join }}` |
#### File: vars/main/install.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [k3s_install_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/install.yml#L3)   | str | `/usr/local/bin` |
| [k3s_install_config_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/install.yml#L6)   | str | `/etc/rancher/k3s` |
| [k3s_install_binary](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/install.yml#L9)   | str | `{{ (k3s_install_dir, 'k3s') ¦ ansible.builtin.path_join }}` |
| [k3s_install_script](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/install.yml#L12)   | str | `{{ (k3s_install_dir, 'k3s-install.sh') ¦ ansible.builtin.path_join }}` |
#### File: vars/main/main.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [k3s_cache_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/main.yml#L3)   | str | `{{ (common_cache_local_dir, 'k3s') ¦ ansible.builtin.path_join }}` |
| [k3s_artifact_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/main.yml#L6)   | str | `{{ (common_artifact_local_dir, 'k3s') ¦ ansible.builtin.path_join }}` |


### Tasks


#### File: tasks/agent/config.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Render K3s agent template](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/agent/config.yml#L2) | ansible.builtin.template | False |

#### File: tasks/agent/install.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Install K3s agent](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/agent/install.yml#L2) | ansible.builtin.script | False |

#### File: tasks/download.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Get latest K3s version](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/download.yml#L2) | block | True |
| [Fetch latest K3s release on GitHub](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/download.yml#L5) | community.general.github_release | False |
| [Set K3s version fact](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/download.yml#L13) | ansible.builtin.set_fact | False |
| [Download K3s binary](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/download.yml#L17) | ansible.builtin.include_role | False |
| [Download K3s script](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/download.yml#L26) | ansible.builtin.include_role | False |

#### File: tasks/install.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Create K3s directories](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/install.yml#L2) | ansible.builtin.file | False |
| [Copy K3s binary](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/install.yml#L13) | ansible.builtin.copy | False |

#### File: tasks/main.yml

| Name | Module | Has Conditions | Tags |
| ---- | ------ | -------------- | -----|
| [Download K3s](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/main.yml#L2) | ansible.builtin.include_tasks | False | download,packer |
| [Install K3s](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/main.yml#L12) | ansible.builtin.include_tasks | False | install,packer |
| [Setup K3s server](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/main.yml#L19) | block | True | s,e,r,v,e,r |
| [Install K3s server](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/main.yml#L23) | ansible.builtin.include_tasks | False |  |
| [Configure K3s server](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/main.yml#L30) | ansible.builtin.include_tasks | False |  |
| [Setup K3s agent](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/main.yml#L37) | block | True | a,g,e,n,t |
| [Install K3s agent](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/main.yml#L41) | ansible.builtin.include_tasks | False |  |
| [Configure K3s agent](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/main.yml#L48) | ansible.builtin.include_tasks | False |  |
| [Flush handlers](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/main.yml#L55) | ansible.builtin.meta | False | a,l,w,a,y,s |

#### File: tasks/server/config.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Render K3s server template](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/server/config.yml#L2) | ansible.builtin.template | False |

#### File: tasks/server/install.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Install K3s server](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/server/install.yml#L2) | ansible.builtin.script | False |







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
