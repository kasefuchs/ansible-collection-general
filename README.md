<!-- DOCSIBLE START -->

# 📃 Collection overview

**Namespace**: kasefuchs

**Name**: general

**Version**: 1.1.3

**Authors**:

- kasefuchs

## Description

A collection of common Ansible roles used across my own projects.

## Roles

### [amneziawg](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg)

### [common](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/common)

### [download](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download)

### [k3s](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s)

### [nebula](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula)

### [tailscale](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale)

## Roles vars

# [amneziawg](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg)

## amneziawg Description:

Install and configure AmneziaWG using amneziawg-go and amneziawg-tools with systemd integration.

### amneziawg Defaults

**These are static variables with lower priority**

#### amneziawg File: [defaults/main/config.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/config.yml)

| Var                                                                                                                                                   | Type | Value                                                                                            |
| ----------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ------------------------------------------------------------------------------------------------ |
| [amneziawg_config_name](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/config.yml#L2)        | str  | `awg0`                                                                                           |
| [amneziawg_config_interface](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/config.yml#L5)   | str  | `{{ undef('AmneziaWG interface configuration must be provided (amneziawg_config_interface)') }}` |
| [amneziawg_config_peers](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/config.yml#L8)       | list | `[]`                                                                                             |
| [amneziawg_config_junk](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/config.yml#L11)       | dict | `{}`                                                                                             |
| [amneziawg_config_paddings](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/config.yml#L14)   | list | `[]`                                                                                             |
| [amneziawg_config_headers](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/config.yml#L17)    | list | `[]`                                                                                             |
| [amneziawg_config_signatures](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/config.yml#L20) | list | `[]`                                                                                             |

#### amneziawg File: [defaults/main/download.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/download.yml)

| Var                                                                                                                                                                           | Type | Value                                                                                                                      |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | -------------------------------------------------------------------------------------------------------------------------- |
| [amneziawg_download_go_version](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/download.yml#L3)                      | str  | `0.2.16`                                                                                                                   |
| [amneziawg_download_go_architecture_map](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/download.yml#L6)             | dict | `{}`                                                                                                                       |
| [amneziawg_download_go_architecture_map.x86_64](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/download.yml#L7)      | str  | `amd64`                                                                                                                    |
| [amneziawg_download_go_architecture_map.aarch64](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/download.yml#L8)     | str  | `arm64`                                                                                                                    |
| [amneziawg_download_go_url](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/download.yml#L11)                         | str  | `https://dl.kasefuchs.net/amneziawg-go/amneziawg-go_{{ download_version }}_linux_{{ download_architecture.value }}.tar.gz` |
| [amneziawg_download_tools_version](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/download.yml#L14)                  | str  | `1.0.20250903`                                                                                                             |
| [amneziawg_download_tools_architecture_map](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/download.yml#L17)         | dict | `{}`                                                                                                                       |
| [amneziawg_download_tools_architecture_map.x86_64](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/download.yml#L18)  | str  | `x86_64`                                                                                                                   |
| [amneziawg_download_tools_architecture_map.aarch64](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/download.yml#L19) | str  | `aarch64`                                                                                                                  |
| [amneziawg_download_tools_url](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/download.yml#L22)                      | str  | `https://dl.kasefuchs.net/amneziawg-tools/awg-v{{ download_version }}-{{ download_architecture.value }}-linux-musl.tar.gz` |

#### amneziawg File: [defaults/main/install.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/install.yml)

| Var                                                                                                                                                                  | Type | Value          |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | -------------- |
| [amneziawg_install_go_extract_options](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/install.yml#L3)       | list | `[]`           |
| [amneziawg_install_go_extract_include](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/install.yml#L6)       | list | `[]`           |
| [amneziawg_install_go_extract_include.0](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/install.yml#L6)     | str  | `amneziawg-go` |
| [amneziawg_install_tools_extract_options](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/install.yml#L9)    | list | `[]`           |
| [amneziawg_install_tools_extract_include](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/install.yml#L12)   | list | `[]`           |
| [amneziawg_install_tools_extract_include.0](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/install.yml#L12) | str  | `awg`          |
| [amneziawg_install_tools_extract_include.1](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/defaults/main/install.yml#L12) | str  | `awg-quick`    |

### amneziawg Vars

**These are variables with higher priority**

#### amneziawg File: [vars/main/config.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/config.yml)

| Var                                                                                                                                        | Type | Value                                                                                               |
| ------------------------------------------------------------------------------------------------------------------------------------------ | ---- | --------------------------------------------------------------------------------------------------- |
| [amneziawg_config_file](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/config.yml#L3) | str  | `{{ (amneziawg_install_config_dir, amneziawg_config_name ~ '.conf') ¦ ansible.builtin.path_join }}` |

#### amneziawg File: [vars/main/download.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/download.yml)

| Var                                                                                                                                                         | Type | Value                                                                                                           |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | --------------------------------------------------------------------------------------------------------------- |
| [amneziawg_download_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/download.yml#L3)         | str  | `{{ (amneziawg_cache_local_dir, 'download') ¦ ansible.builtin.path_join }}`                                     |
| [amneziawg_download_go_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/download.yml#L6)      | str  | `{{ (amneziawg_download_local_dir, 'go') ¦ ansible.builtin.path_join }}`                                        |
| [amneziawg_download_go_local_file](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/download.yml#L9)     | str  | `{{ (amneziawg_download_go_local_dir, 'current', ansible_facts.architecture) ¦ ansible.builtin.path_join }}`    |
| [amneziawg_download_tools_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/download.yml#L12)  | str  | `{{ (amneziawg_download_local_dir, 'tools') ¦ ansible.builtin.path_join }}`                                     |
| [amneziawg_download_tools_local_file](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/download.yml#L15) | str  | `{{ (amneziawg_download_tools_local_dir, 'current', ansible_facts.architecture) ¦ ansible.builtin.path_join }}` |

#### amneziawg File: [vars/main/install.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/install.yml)

| Var                                                                                                                                                | Type | Value                                                                    |
| -------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ------------------------------------------------------------------------ |
| [amneziawg_install_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/install.yml#L3)        | str  | `/usr/local/bin`                                                         |
| [amneziawg_install_config_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/install.yml#L6) | str  | `/etc/amnezia/amneziawg`                                                 |
| [amneziawg_install_binary](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/install.yml#L9)     | str  | `{{ (amneziawg_install_dir, 'awg') ¦ ansible.builtin.path_join }}`       |
| [amneziawg_install_script](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/install.yml#L12)    | str  | `{{ (amneziawg_install_dir, 'awg-quick') ¦ ansible.builtin.path_join }}` |

#### amneziawg File: [vars/main/main.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/main.yml)

| Var                                                                                                                                             | Type | Value                                                                        |
| ----------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ---------------------------------------------------------------------------- |
| [amneziawg_cache_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/main.yml#L3)    | str  | `{{ (common_cache_local_dir, 'amneziawg') ¦ ansible.builtin.path_join }}`    |
| [amneziawg_artifact_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/amneziawg/vars/main/main.yml#L6) | str  | `{{ (common_artifact_local_dir, 'amneziawg') ¦ ansible.builtin.path_join }}` |

# [common](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/common)

## common Description:

Common helper role providing shared variables, paths, and handlers used across other roles in the collection.

### common Vars

**These are variables with higher priority**

#### common File: [vars/main.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/common/vars/main.yml)

| Var                                                                                                                                     | Type | Value                                                                                                                                                                                         |
| --------------------------------------------------------------------------------------------------------------------------------------- | ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [common_inventory_name](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/common/vars/main.yml#L3)        | str  | `{{ inventory_dir ¦ ansible.builtin.basename }}`                                                                                                                                              |
| [common_managed_header](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/common/vars/main.yml#L6)        | str  | `Managed by Ansible ¦ Template: {{ template_path if not template_path.startswith('/') else (template_path ¦ basename) }} (last modified: {{ template_mtime.strftime('%Y-%m-%d %H:%M:%S') }})` |
| [common_cache_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/common/vars/main.yml#L9)       | str  | `{{ (playbook_dir, '../cache') ¦ ansible.builtin.path_join }}`                                                                                                                                |
| [common_artifact_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/common/vars/main.yml#L12)   | str  | `{{ (inventory_dir, '../artifacts', common_inventory_name) ¦ ansible.builtin.path_join }}`                                                                                                    |
| [common_unique_architectures](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/common/vars/main.yml#L15) | str  | `{{ ansible_play_hosts ¦ map('ansible.builtin.extract', hostvars, ['ansible_facts', 'architecture']) ¦ unique }}`                                                                             |

# [download](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download)

## download Description:

Generic reusable download role that fetches and manages versioned binaries and archives with multi-architecture support.

### download Defaults

**These are static variables with lower priority**

#### download File: [defaults/main.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download/defaults/main.yml)

| Var                                                                                                                                                 | Type | Value                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ------------------------------------------------------------------- |
| [download_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download/defaults/main.yml#L3)                       | str  | `{{ undef('Download directory must be provided (download_dir)') }}` |
| [download_url](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download/defaults/main.yml#L6)                       | str  | `{{ undef('Download url must be provided (download_url)') }}`       |
| [download_version](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download/defaults/main.yml#L9)                   | str  | `{{ undef('Download version be provided (download_version)') }}`    |
| [download_architecture_map](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download/defaults/main.yml#L12)         | dict | `{}`                                                                |
| [download_architecture_map.x86_64](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download/defaults/main.yml#L13)  | str  | `amd64`                                                             |
| [download_architecture_map.aarch64](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download/defaults/main.yml#L14) | str  | `arm64`                                                             |

### download Vars

**These are variables with higher priority**

#### download File: [vars/main.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download/vars/main.yml)

| Var                                                                                                                                    | Type | Value                                                                |
| -------------------------------------------------------------------------------------------------------------------------------------- | ---- | -------------------------------------------------------------------- |
| [download_current_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download/vars/main.yml#L3)      | str  | `{{ (download_dir, download_version) ¦ ansible.builtin.path_join }}` |
| [download_current_dir_link](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download/vars/main.yml#L6) | str  | `{{ (download_dir, 'current') ¦ ansible.builtin.path_join }}`        |

# [k3s](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s)

## k3s Description:

Install and configure K3s Kubernetes distribution, including server and agent modes with download, installation and configuration management.

### k3s Defaults

**These are static variables with lower priority**

#### k3s File: [defaults/main/agent/config.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/agent/config.yml)

| Var                                                                                                                                             | Type | Value                                                                      |
| ----------------------------------------------------------------------------------------------------------------------------------------------- | ---- | -------------------------------------------------------------------------- |
| [k3s_agent_config_token](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/agent/config.yml#L3) | str  | `{{ undef('K3s agent token must be provided (k3s_agent_config_token)') }}` |
| [k3s_agent_config](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/agent/config.yml#L6)       | dict | `{}`                                                                       |
| [k3s_agent_config.token](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/agent/config.yml#L7) | str  | `{{ k3s_agent_config_token }}`                                             |

#### k3s File: [defaults/main/agent/main.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/agent/main.yml)

| Var                                                                                                                                    | Type | Value       |
| -------------------------------------------------------------------------------------------------------------------------------------- | ---- | ----------- |
| [k3s_agent_group](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/agent/main.yml#L3) | str  | `k3s_agent` |

#### k3s File: [defaults/main/download.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml)

| Var                                                                                                                                                         | Type | Value                                                                                                                                                |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| [k3s_download_version](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml#L3)                   | str  | `latest`                                                                                                                                             |
| [k3s_download_github_user](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml#L6)               | str  | `k3s-io`                                                                                                                                             |
| [k3s_download_github_repository](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml#L9)         | str  | `k3s`                                                                                                                                                |
| [k3s_download_architecture_map](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml#L12)         | dict | `{}`                                                                                                                                                 |
| [k3s_download_architecture_map.x86_64](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml#L13)  | str  | `amd64`                                                                                                                                              |
| [k3s_download_architecture_map.aarch64](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml#L14) | str  | `arm64`                                                                                                                                              |
| [k3s_download_binary_url](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml#L17)               | str  | `<multiline value: folded>`                                                                                                                          |
| [k3s_download_script_url](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/download.yml#L26)               | str  | `https://raw.githubusercontent.com/{{ k3s_download_github_user }}/{{ k3s_download_github_repository }}/refs/tags/v{{ download_version }}/install.sh` |

#### k3s File: [defaults/main/server/config.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/server/config.yml)

| Var                                                                                                                                         | Type | Value |
| ------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ----- |
| [k3s_server_config](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/server/config.yml#L3) | dict | `{}`  |

#### k3s File: [defaults/main/server/main.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/server/main.yml)

| Var                                                                                                                                      | Type | Value        |
| ---------------------------------------------------------------------------------------------------------------------------------------- | ---- | ------------ |
| [k3s_server_group](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/defaults/main/server/main.yml#L3) | str  | `k3s_server` |

### k3s Vars

**These are variables with higher priority**

#### k3s File: [vars/main/config.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/config.yml)

| Var                                                                                                                            | Type | Value                                                                       |
| ------------------------------------------------------------------------------------------------------------------------------ | ---- | --------------------------------------------------------------------------- |
| [k3s_config_file](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/config.yml#L3) | str  | `{{ (k3s_install_config_dir, 'config.yaml') ¦ ansible.builtin.path_join }}` |

#### k3s File: [vars/main/download.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/download.yml)

| Var                                                                                                                                              | Type | Value                                                                                                      |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | ---- | ---------------------------------------------------------------------------------------------------------- |
| [k3s_download_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/download.yml#L3)          | str  | `{{ (k3s_cache_local_dir, 'download') ¦ ansible.builtin.path_join }}`                                      |
| [k3s_download_binary_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/download.yml#L6)   | str  | `{{ (k3s_download_local_dir, 'binary') ¦ ansible.builtin.path_join }}`                                     |
| [k3s_download_binary_local_file](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/download.yml#L9)  | str  | `{{ (k3s_download_binary_local_dir, 'current', ansible_facts.architecture) ¦ ansible.builtin.path_join }}` |
| [k3s_download_script_local_file](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/download.yml#L12) | str  | `{{ (k3s_download_script_local_dir, 'current', ansible_facts.architecture) ¦ ansible.builtin.path_join }}` |
| [k3s_download_script_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/download.yml#L15)  | str  | `{{ (k3s_download_local_dir, 'script') ¦ ansible.builtin.path_join }}`                                     |

#### k3s File: [vars/main/install.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/install.yml)

| Var                                                                                                                                    | Type | Value                                                                   |
| -------------------------------------------------------------------------------------------------------------------------------------- | ---- | ----------------------------------------------------------------------- |
| [k3s_install_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/install.yml#L3)        | str  | `/usr/local/bin`                                                        |
| [k3s_install_config_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/install.yml#L6) | str  | `/etc/rancher/k3s`                                                      |
| [k3s_install_binary](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/install.yml#L9)     | str  | `{{ (k3s_install_dir, 'k3s') ¦ ansible.builtin.path_join }}`            |
| [k3s_install_script](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/install.yml#L12)    | str  | `{{ (k3s_install_dir, 'k3s-install.sh') ¦ ansible.builtin.path_join }}` |

#### k3s File: [vars/main/main.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/main.yml)

| Var                                                                                                                                 | Type | Value                                                                  |
| ----------------------------------------------------------------------------------------------------------------------------------- | ---- | ---------------------------------------------------------------------- |
| [k3s_cache_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/main.yml#L3)    | str  | `{{ (common_cache_local_dir, 'k3s') ¦ ansible.builtin.path_join }}`    |
| [k3s_artifact_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/k3s/vars/main/main.yml#L6) | str  | `{{ (common_artifact_local_dir, 'k3s') ¦ ansible.builtin.path_join }}` |

# [nebula](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula)

## nebula Description:

Install and configure Nebula overlay networking, including certificate generation, service setup, and configuration management.

### nebula Defaults

**These are static variables with lower priority**

#### nebula File: [defaults/main/cert.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/cert.yml)

| Var                                                                                                                                           | Type | Value                      |
| --------------------------------------------------------------------------------------------------------------------------------------------- | ---- | -------------------------- |
| [nebula_cert_ca_cn](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/cert.yml#L3)         | str  | `Nebula CA`                |
| [nebula_cert_ca_duration](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/cert.yml#L6)   | str  | `87600h`                   |
| [nebula_cert_host_cn](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/cert.yml#L9)       | str  | `{{ inventory_hostname }}` |
| [nebula_cert_host_subnets](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/cert.yml#L12) | list | `[]`                       |

#### nebula File: [defaults/main/config.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml)

| Var                                                                                                                                                            | Type | Value                                 |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ------------------------------------- |
| [nebula_config](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L3)                            | dict | `{}`                                  |
| [nebula_config.firewall](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L4)                   | str  | `{{ nebula_config_firewall }}`        |
| [nebula_config.lighthouse](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L5)                 | str  | `{{ nebula_config_lighthouse }}`      |
| [nebula_config.listen](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L6)                     | str  | `{{ nebula_config_listen }}`          |
| [nebula_config.pki](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L7)                        | str  | `{{ nebula_config_pki }}`             |
| [nebula_config.punchy](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L8)                     | str  | `{{ nebula_config_punchy }}`          |
| [nebula_config.relay](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L9)                      | str  | `{{ nebula_config_relay }}`           |
| [nebula_config.static_host_map](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L10)           | str  | `{{ nebula_config_static_host_map }}` |
| [nebula_config.tun](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L11)                       | str  | `{{ nebula_config_tun }}`             |
| [nebula_config_listen](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L14)                    | dict | `{}`                                  |
| [nebula_config_listen.host](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L15)               | str  | `0.0.0.0`                             |
| [nebula_config_listen.port](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L16)               | int  | `4646`                                |
| [nebula_config_lighthouse](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L19)                | dict | `{}`                                  |
| [nebula_config_lighthouse.am_lighthouse](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L20)  | bool | `False`                               |
| [nebula_config_lighthouse.hosts](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L21)          | str  | `{{ nebula_config_lighthouse_list }}` |
| [nebula_config_lighthouse_list](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L24)           | list | `[]`                                  |
| [nebula_config_tun](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L27)                       | dict | `{}`                                  |
| [nebula_config_tun.dev](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L28)                   | str  | `nebula0`                             |
| [nebula_config_firewall](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L31)                  | dict | `{}`                                  |
| [nebula_config_firewall.inbound_action](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L32)   | str  | `drop`                                |
| [nebula_config_firewall.outbound_action](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L33)  | str  | `drop`                                |
| [nebula_config_firewall.inbound](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L34)          | list | `[]`                                  |
| [nebula_config_firewall.inbound.0](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L34)        | dict | `{}`                                  |
| [nebula_config_firewall.inbound.0.host](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L35)   | str  | `any`                                 |
| [nebula_config_firewall.inbound.0.port](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L35)   | str  | `any`                                 |
| [nebula_config_firewall.inbound.0.proto](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L35)  | str  | `any`                                 |
| [nebula_config_firewall.outbound](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L36)         | list | `[]`                                  |
| [nebula_config_firewall.outbound.0](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L36)       | dict | `{}`                                  |
| [nebula_config_firewall.outbound.0.host](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L37)  | str  | `any`                                 |
| [nebula_config_firewall.outbound.0.port](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L37)  | str  | `any`                                 |
| [nebula_config_firewall.outbound.0.proto](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L37) | str  | `any`                                 |
| [nebula_config_punchy](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L40)                    | dict | `{}`                                  |
| [nebula_config_punchy.punch](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L41)              | bool | `False`                               |
| [nebula_config_punchy.respond](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L42)            | bool | `False`                               |
| [nebula_config_relay](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L45)                     | dict | `{}`                                  |
| [nebula_config_relay.relays](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L46)              | str  | `{{ nebula_config_relay_list }}`      |
| [nebula_config_relay.am_relay](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L47)            | bool | `False`                               |
| [nebula_config_relay.use_relays](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L48)          | bool | `True`                                |
| [nebula_config_relay_list](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L51)                | list | `[]`                                  |
| [nebula_config_static_host_map](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/config.yml#L54)           | dict | `{}`                                  |

#### nebula File: [defaults/main/download.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/download.yml)

| Var                                                                                                                                                               | Type | Value                                                                                                                                                                                          |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [nebula_download_version](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/download.yml#L3)                   | str  | `latest`                                                                                                                                                                                       |
| [nebula_download_github_user](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/download.yml#L6)               | str  | `slackhq`                                                                                                                                                                                      |
| [nebula_download_github_repository](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/download.yml#L9)         | str  | `nebula`                                                                                                                                                                                       |
| [nebula_download_architecture_map](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/download.yml#L12)         | dict | `{}`                                                                                                                                                                                           |
| [nebula_download_architecture_map.x86_64](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/download.yml#L13)  | str  | `amd64`                                                                                                                                                                                        |
| [nebula_download_architecture_map.aarch64](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/download.yml#L14) | str  | `arm64`                                                                                                                                                                                        |
| [nebula_download_url](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/download.yml#L17)                      | str  | `https://github.com/{{ nebula_download_github_user }}/{{ nebula_download_github_repository }}/releases/download/v{{ download_version }}/nebula-linux-{{ download_architecture.value }}.tar.gz` |

#### nebula File: [defaults/main/install.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/install.yml)

| Var                                                                                                                                                     | Type | Value         |
| ------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ------------- |
| [nebula_install_extract_options](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/install.yml#L3)   | list | `[]`          |
| [nebula_install_extract_include](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/install.yml#L6)   | list | `[]`          |
| [nebula_install_extract_include.0](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/install.yml#L6) | str  | `nebula`      |
| [nebula_install_extract_include.1](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/defaults/main/install.yml#L6) | str  | `nebula-cert` |

### nebula Vars

**These are variables with higher priority**

#### nebula File: [vars/main/cert.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/cert.yml)

| Var                                                                                                                                   | Type | Value                                                                   |
| ------------------------------------------------------------------------------------------------------------------------------------- | ---- | ----------------------------------------------------------------------- |
| [nebula_cert_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/cert.yml#L3)       | str  | `/etc/pki/nebula`                                                       |
| [nebula_cert_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/cert.yml#L6) | str  | `{{ (nebula_artifact_local_dir, 'cert') ¦ ansible.builtin.path_join }}` |

#### nebula File: [vars/main/config.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/config.yml)

| Var                                                                                                                                      | Type | Value                                                                          |
| ---------------------------------------------------------------------------------------------------------------------------------------- | ---- | ------------------------------------------------------------------------------ |
| [nebula_config_file](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/config.yml#L3)     | str  | `{{ (nebula_install_config_dir, 'config.yaml') ¦ ansible.builtin.path_join }}` |
| [nebula_config_pki](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/config.yml#L6)      | dict | `{}`                                                                           |
| [nebula_config_pki.ca](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/config.yml#L7)   | str  | `{{ (nebula_cert_dir, 'ca.crt') ¦ ansible.builtin.path_join }}`                |
| [nebula_config_pki.key](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/config.yml#L8)  | str  | `{{ (nebula_cert_dir, 'node.key') ¦ ansible.builtin.path_join }}`              |
| [nebula_config_pki.cert](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/config.yml#L9) | str  | `{{ (nebula_cert_dir, 'node.crt') ¦ ansible.builtin.path_join }}`              |

#### nebula File: [vars/main/download.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/download.yml)

| Var                                                                                                                                            | Type | Value                                                                                                  |
| ---------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ------------------------------------------------------------------------------------------------------ |
| [nebula_download_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/download.yml#L3)  | str  | `{{ (nebula_cache_local_dir, 'download') ¦ ansible.builtin.path_join }}`                               |
| [nebula_download_local_file](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/download.yml#L6) | str  | `{{ (nebula_download_local_dir, 'current', ansible_facts.architecture) ¦ ansible.builtin.path_join }}` |

#### nebula File: [vars/main/install.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/install.yml)

| Var                                                                                                                                          | Type | Value                                                              |
| -------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ------------------------------------------------------------------ |
| [nebula_install_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/install.yml#L3)        | str  | `/usr/local/bin`                                                   |
| [nebula_install_config_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/install.yml#L6) | str  | `/etc/nebula`                                                      |
| [nebula_install_binary](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/install.yml#L9)     | str  | `{{ (nebula_install_dir, 'nebula') ¦ ansible.builtin.path_join }}` |

#### nebula File: [vars/main/main.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/main.yml)

| Var                                                                                                                                       | Type | Value                                                                     |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ---- | ------------------------------------------------------------------------- |
| [nebula_cache_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/main.yml#L3)    | str  | `{{ (common_cache_local_dir, 'nebula') ¦ ansible.builtin.path_join }}`    |
| [nebula_artifact_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/nebula/vars/main/main.yml#L6) | str  | `{{ (common_artifact_local_dir, 'nebula') ¦ ansible.builtin.path_join }}` |

# [tailscale](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale)

## tailscale Description:

Install and configure Tailscale mesh VPN, including automated login, service setup, and runtime configuration.

### tailscale Defaults

**These are static variables with lower priority**

#### tailscale File: [defaults/main/config.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/config.yml)

| Var                                                                                                                                                         | Type | Value                                                                            |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | -------------------------------------------------------------------------------- |
| [tailscale_config_flags](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/config.yml#L3)             | list | `[]`                                                                             |
| [tailscale_config_flags.0](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/config.yml#L4)           | str  | `--accept-routes`                                                                |
| [tailscale_config_flags.1](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/config.yml#L5)           | str  | `--advertise-exit-node`                                                          |
| [tailscale_config_flags.2](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/config.yml#L6)           | str  | `--webclient`                                                                    |
| [tailscale_config_auth_key](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/config.yml#L9)          | str  | `{{ undef('Tailscale auth key must be provided (tailscale_config_auth_key)') }}` |
| [tailscale_config_login_server](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/config.yml#L12)     | str  | `https://controlplane.tailscale.com`                                             |
| [tailscale_config_advertise_tags](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/config.yml#L15)   | list | `[]`                                                                             |
| [tailscale_config_advertise_tags.0](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/config.yml#L16) | str  | `server`                                                                         |

#### tailscale File: [defaults/main/download.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/download.yml)

| Var                                                                                                                                                                     | Type | Value                                                                                                      |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ---------------------------------------------------------------------------------------------------------- |
| [tailscale_download_version](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/download.yml#L3)                   | str  | `latest`                                                                                                   |
| [tailscale_download_github_user](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/download.yml#L6)               | str  | `tailscale`                                                                                                |
| [tailscale_download_github_repository](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/download.yml#L9)         | str  | `tailscale`                                                                                                |
| [tailscale_download_architecture_map](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/download.yml#L12)         | dict | `{}`                                                                                                       |
| [tailscale_download_architecture_map.x86_64](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/download.yml#L13)  | str  | `amd64`                                                                                                    |
| [tailscale_download_architecture_map.aarch64](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/download.yml#L14) | str  | `arm64`                                                                                                    |
| [tailscale_download_url](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/download.yml#L17)                      | str  | `https://pkgs.tailscale.com/stable/tailscale_{{ download_version }}_{{ download_architecture.value }}.tgz` |

#### tailscale File: [defaults/main/install.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/install.yml)

| Var                                                                                                                                                           | Type | Value                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ------------------------ |
| [tailscale_install_extract_options](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/install.yml#L3)   | list | `[]`                     |
| [tailscale_install_extract_options.0](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/install.yml#L3) | str  | `--strip-components=1`   |
| [tailscale_install_extract_options.1](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/install.yml#L3) | str  | `--wildcards`            |
| [tailscale_install_extract_include](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/install.yml#L6)   | list | `[]`                     |
| [tailscale_install_extract_include.0](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/install.yml#L7) | str  | `tailscale_*/tailscale`  |
| [tailscale_install_extract_include.1](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/defaults/main/install.yml#L7) | str  | `tailscale_*/tailscaled` |

### tailscale Vars

**These are variables with higher priority**

#### tailscale File: [vars/main/download.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/vars/main/download.yml)

| Var                                                                                                                                                  | Type | Value                                                                                                     |
| ---------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | --------------------------------------------------------------------------------------------------------- |
| [tailscale_download_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/vars/main/download.yml#L3)  | str  | `{{ (tailscale_cache_local_dir, 'download') ¦ ansible.builtin.path_join }}`                               |
| [tailscale_download_local_file](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/vars/main/download.yml#L6) | str  | `{{ (tailscale_download_local_dir, 'current', ansible_facts.architecture) ¦ ansible.builtin.path_join }}` |

#### tailscale File: [vars/main/install.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/vars/main/install.yml)

| Var                                                                                                                                                   | Type | Value                                                                     |
| ----------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ------------------------------------------------------------------------- |
| [tailscale_install_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/vars/main/install.yml#L3)           | str  | `/usr/local/bin`                                                          |
| [tailscale_install_binary](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/vars/main/install.yml#L6)        | str  | `{{ (tailscale_install_dir, 'tailscale') ¦ ansible.builtin.path_join }}`  |
| [tailscale_install_daemon_binary](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/vars/main/install.yml#L9) | str  | `{{ (tailscale_install_dir, 'tailscaled') ¦ ansible.builtin.path_join }}` |

#### tailscale File: [vars/main/main.yml](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/vars/main/main.yml)

| Var                                                                                                                                             | Type | Value                                                                        |
| ----------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ---------------------------------------------------------------------------- |
| [tailscale_cache_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/vars/main/main.yml#L3)    | str  | `{{ (common_cache_local_dir, 'tailscale') ¦ ansible.builtin.path_join }}`    |
| [tailscale_artifact_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/tailscale/vars/main/main.yml#L6) | str  | `{{ (common_artifact_local_dir, 'tailscale') ¦ ansible.builtin.path_join }}` |

## Metadata

- **Repository**: [Repository](https://codeberg.org/kasefuchs/ansible-collection-general)

- **Documentation**: [Documentation](https://codeberg.org/kasefuchs/ansible-collection-general)

- **Homepage**: [Homepage](https://codeberg.org/kasefuchs/ansible-collection-general)

- **Issues**: [Issues](https://codeberg.org/kasefuchs/ansible-collection-general/issues)

<!-- DOCSIBLE END -->
