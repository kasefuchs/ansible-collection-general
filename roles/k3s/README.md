<!-- DOCSIBLE START -->

# 📃 Role overview

## k3s

```
Role belongs to kasefuchs/general
Namespace - kasefuchs
Collection - general
Version - 1.3.1
Repository - https://codeberg.org/kasefuchs/ansible-collection-general
```

Description: Install and configure K3s Kubernetes distribution, including server and agent modes with download, installation and configuration management. #magic___^_^___line


| Field                | Value           |
|--------------------- |-----------------|
| Readme update        | 2026/02/15 |








### Defaults

**These are static variables with lower priority**

#### File: defaults/main/agent/config.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [k3s_agent_config_token](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/agent/config.yml#L2)   | str | `{{ undef('K3s agent token must be provided (k3s_agent_config_token)') }}` |
| [k3s_agent_config](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/agent/config.yml#L5)   | dict | `{}` |
| [k3s_agent_config.**token**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/agent/config.yml#L6)   | str | `{{ k3s_agent_config_token }}` |

#### File: defaults/main/agent/main.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [k3s_agent_group](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/agent/main.yml#L2)   | str | `k3s_agent` |

#### File: defaults/main/config.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [k3s_config_registries](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/config.yml#L2)   | dict | `{}` |

#### File: defaults/main/download.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [k3s_download_version](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml#L2)   | str | `latest` |
| [k3s_download_github_user](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml#L5)   | str | `k3s-io` |
| [k3s_download_github_repository](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml#L8)   | str | `k3s` |
| [k3s_download_binary_architecture_map](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml#L11)   | dict | `{}` |
| [k3s_download_binary_architecture_map.**x86_64**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml#L12)   | str | `amd64` |
| [k3s_download_binary_architecture_map.**aarch64**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml#L13)   | str | `arm64` |
| [k3s_download_binary_url](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml#L16)   | str | `<multiline value: literal_strip>` |
| [k3s_download_script_url](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml#L25)   | str | `https://raw.githubusercontent.com/{{ k3s_download_github_user }}/{{ k3s_download_github_repository }}/refs/tags/v{{ download_url_version }}/install.sh` |
| [k3s_download_script_architecture_map](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml#L28)   | dict | `{}` |
| [k3s_download_script_architecture_map.**noarch**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml#L29)   | str |  |

#### File: defaults/main/server/config.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [k3s_server_config](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/server/config.yml#L2)   | dict | `{}` |
| [k3s_server_config_manifests](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/server/config.yml#L5)   | dict | `{}` |

#### File: defaults/main/server/main.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [k3s_server_group](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/server/main.yml#L2)   | str | `k3s_server` |


### Vars

**These are variables with higher priority**
#### File: vars/main/config.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [k3s_config_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/config.yml#L2)   | str | `/etc/rancher/k3s` |
| [k3s_config_file](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/config.yml#L5)   | str | `{{ (k3s_config_dir, 'config.yaml') ¦ path_join }}` |
| [k3s_config_registries_file](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/config.yml#L8)   | str | `{{ (k3s_config_dir, 'registries.yaml') ¦ path_join }}` |
#### File: vars/main/download.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [k3s_download_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/download.yml#L2)   | str | `{{ (k3s_cache_local_dir, 'download') ¦ path_join }}` |
| [k3s_download_binary_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/download.yml#L5)   | str | `{{ (k3s_download_local_dir, 'binary') ¦ path_join }}` |
| [k3s_download_binary_local_file](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/download.yml#L8)   | str | `{{ (k3s_download_binary_local_dir, 'current', ansible_facts.architecture) ¦ path_join }}` |
| [k3s_download_script_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/download.yml#L11)   | str | `{{ (k3s_download_local_dir, 'script') ¦ path_join }}` |
| [k3s_download_script_local_file](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/download.yml#L14)   | str | `{{ (k3s_download_script_local_dir, 'current/noarch') ¦ path_join }}` |
#### File: vars/main/install.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [k3s_install_binary](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/install.yml#L2)   | str | `{{ (common_binary_dir, 'k3s') ¦ path_join }}` |
| [k3s_install_script](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/install.yml#L5)   | str | `{{ (common_binary_dir, 'k3s-install.sh') ¦ path_join }}` |
#### File: vars/main/main.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [k3s_cache_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/main.yml#L2)   | str | `{{ (common_cache_local_dir, 'k3s') ¦ path_join }}` |
| [k3s_artifact_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/main.yml#L5)   | str | `{{ (common_artifact_local_dir, 'k3s') ¦ path_join }}` |
#### File: vars/main/server/config.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [k3s_server_config_manifests_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/server/config.yml#L2)   | str | `/var/lib/rancher/k3s/server/manifests` |


### Tasks


#### File: tasks/agent/config.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Render K3s agent template](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/agent/config.yml#L1) | ansible.builtin.template | False |

#### File: tasks/agent/install.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Install K3s agent](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/agent/install.yml#L1) | ansible.builtin.script | False |

#### File: tasks/config.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Configure K3s registries](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/config.yml#L1) | ansible.builtin.template | True |
| [Remove K3s registries config](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/config.yml#L13) | ansible.builtin.file | True |

#### File: tasks/download.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Get latest K3s version](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/download.yml#L1) | block | True |
| [Fetch latest K3s release on GitHub](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/download.yml#L4) | community.general.github_release | False |
| [Set K3s version fact](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/download.yml#L12) | ansible.builtin.set_fact | False |
| [Download K3s binary](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/download.yml#L16) | ansible.builtin.include_role | False |
| [Download K3s script](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/download.yml#L25) | ansible.builtin.include_role | False |

#### File: tasks/install.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Create K3s directories](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/install.yml#L1) | ansible.builtin.file | False |
| [Copy K3s binary](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/install.yml#L11) | ansible.builtin.copy | False |

#### File: tasks/main.yml

| Name | Module | Has Conditions | Tags |
| ---- | ------ | -------------- | -----|
| [Download K3s](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/main.yml#L1) | ansible.builtin.include_tasks | False | download,packer |
| [Install K3s](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/main.yml#L15) | ansible.builtin.include_tasks | False | install,packer |
| [Configure K3s](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/main.yml#L26) | ansible.builtin.include_tasks | False | c,o,n,f,i,g |
| [Setup K3s server](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/main.yml#L33) | block | True | s,e,r,v,e,r |
| [Install K3s server](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/main.yml#L37) | ansible.builtin.include_tasks | False |  |
| [Configure K3s server](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/main.yml#L48) | ansible.builtin.include_tasks | False |  |
| [Setup K3s agent](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/main.yml#L59) | block | True | a,g,e,n,t |
| [Install K3s agent](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/main.yml#L63) | ansible.builtin.include_tasks | False |  |
| [Configure K3s agent](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/main.yml#L74) | ansible.builtin.include_tasks | False |  |
| [Flush handlers](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/main.yml#L85) | ansible.builtin.meta | False | a,l,w,a,y,s |

#### File: tasks/server/config.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Render K3s server template](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/server/config.yml#L1) | ansible.builtin.template | False |
| [Create K3s manifests directory](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/server/config.yml#L14) | ansible.builtin.file | False |
| [Deploy K3s server manifests](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/server/config.yml#L22) | ansible.builtin.copy | False |

#### File: tasks/server/install.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Install K3s server](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/tasks/server/install.yml#L1) | ansible.builtin.script | False |







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
