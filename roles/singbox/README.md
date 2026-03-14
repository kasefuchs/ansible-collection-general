<!-- DOCSIBLE START -->

# 📃 Role overview

## singbox

```
Role belongs to kasefuchs/general
Namespace - kasefuchs
Collection - general
Version - 1.2.2
Repository - https://codeberg.org/kasefuchs/ansible-collection-general
```

Description: Install and configure sing-box proxy platform, including service setup and configuration management.

| Field         | Value      |
| ------------- | ---------- |
| Readme update | 2026/03/13 |

### Defaults

**These are static variables with lower priority**

#### File: defaults/main/config.yml

| Var                                                                                                                                                                             | Type | Value                                  |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | -------------------------------------- |
| [singbox_config_instance](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L3)                                  | str  | `default`                              |
| [singbox_config](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L6)                                           | dict | `{}`                                   |
| [singbox_config.**log**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L7)                                   | str  | `{{ singbox_config_log }}`             |
| [singbox_config.**dns**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L8)                                   | str  | `{{ singbox_config_dns }}`             |
| [singbox_config.**inbounds**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L9)                              | str  | `{{ singbox_config_inbounds }}`        |
| [singbox_config.**outbounds**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L10)                            | str  | `{{ singbox_config_outbounds }}`       |
| [singbox_config.**route**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L11)                                | str  | `{{ singbox_config_route }}`           |
| [singbox_config.**experimental**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L12)                         | str  | `{{ singbox_config_experimental }}`    |
| [singbox_config_log](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L15)                                      | dict | `{}`                                   |
| [singbox_config_log.**level**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L16)                            | str  | `error`                                |
| [singbox_config_log.**timestamp**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L17)                        | bool | `True`                                 |
| [singbox_config_dns](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L20)                                      | dict | `{}`                                   |
| [singbox_config_dns.**final**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L21)                            | str  | `https`                                |
| [singbox_config_dns.**servers**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L22)                          | str  | `{{ singbox_config_dns_servers }}`     |
| [singbox_config_dns.**rules**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L23)                            | str  | `{{ singbox_config_dns_rules }}`       |
| [singbox_config_dns_servers](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L26)                              | list | `[]`                                   |
| [singbox_config_dns_servers.**0**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L27)                        | dict | `{}`                                   |
| [singbox_config_dns_servers.0.**tag**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L27)                    | str  | `tcp`                                  |
| [singbox_config_dns_servers.0.**type**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L28)                   | str  | `tcp`                                  |
| [singbox_config_dns_servers.0.**server**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L29)                 | str  | `8.8.8.8`                              |
| [singbox_config_dns_servers.**1**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L30)                        | dict | `{}`                                   |
| [singbox_config_dns_servers.1.**tag**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L30)                    | str  | `https`                                |
| [singbox_config_dns_servers.1.**type**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L31)                   | str  | `https`                                |
| [singbox_config_dns_servers.1.**server**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L32)                 | str  | `dns.quad9.net`                        |
| [singbox_config_dns_servers.1.**domain_resolver**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L33)        | str  | `tcp`                                  |
| [singbox_config_dns_rules](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L36)                                | list | `[]`                                   |
| [singbox_config_dns_rules.**0**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L37)                          | dict | `{}`                                   |
| [singbox_config_dns_rules.0.**query_type**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L37)               | str  | `HTTPS`                                |
| [singbox_config_dns_rules.0.**action**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L38)                   | str  | `predefined`                           |
| [singbox_config_dns_rules.0.**rcode**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L39)                    | str  | `NOERROR`                              |
| [singbox_config_inbounds](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L42)                                 | list | `[]`                                   |
| [singbox_config_inbounds.**0**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L43)                           | dict | `{}`                                   |
| [singbox_config_inbounds.0.**tag**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L43)                       | str  | `tun`                                  |
| [singbox_config_inbounds.0.**type**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L44)                      | str  | `tun`                                  |
| [singbox_config_inbounds.0.**stack**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L45)                     | str  | `mixed`                                |
| [singbox_config_inbounds.0.**address**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L46)                   | str  | `172.19.0.1/30`                        |
| [singbox_config_inbounds.0.**auto_route**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L47)                | bool | `True`                                 |
| [singbox_config_inbounds.0.**strict_route**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L48)              | bool | `True`                                 |
| [singbox_config_inbounds.0.**auto_redirect**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L49)             | bool | `True`                                 |
| [singbox_config_inbounds.0.**auto_redirect_input_mark**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L50)  | str  | `0x2023`                               |
| [singbox_config_inbounds.0.**auto_redirect_output_mark**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L51) | str  | `0x2024`                               |
| [singbox_config_inbounds.0.**endpoint_independent_nat**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L52)  | bool | `False`                                |
| [singbox_config_inbounds.0.**interface_name**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L53)            | str  | `sb0`                                  |
| [singbox_config_outbounds](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L56)                                | list | `[]`                                   |
| [singbox_config_outbounds.**0**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L57)                          | dict | `{}`                                   |
| [singbox_config_outbounds.0.**tag**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L57)                      | str  | `direct`                               |
| [singbox_config_outbounds.0.**type**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L58)                     | str  | `direct`                               |
| [singbox_config_route](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L61)                                    | dict | `{}`                                   |
| [singbox_config_route.**final**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L62)                          | str  | `direct`                               |
| [singbox_config_route.**auto_detect_interface**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L63)          | bool | `True`                                 |
| [singbox_config_route.**default_domain_resolver**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L64)        | dict | `{}`                                   |
| [singbox_config_route.default_domain_resolver.**server**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L65) | str  | `https`                                |
| [singbox_config_route.**rules**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L66)                          | str  | `{{ singbox_config_route_rules }}`     |
| [singbox_config_route.**rule_set**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L67)                       | str  | `{{ singbox_config_route_rule_sets }}` |
| [singbox_config_route_rules](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L70)                              | list | `[]`                                   |
| [singbox_config_route_rules.**0**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L71)                        | dict | `{}`                                   |
| [singbox_config_route_rules.0.**action**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L71)                 | str  | `sniff`                                |
| [singbox_config_route_rules.**1**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L72)                        | dict | `{}`                                   |
| [singbox_config_route_rules.1.**action**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L72)                 | str  | `hijack-dns`                           |
| [singbox_config_route_rules.1.**protocol**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L73)               | str  | `dns`                                  |
| [singbox_config_route_rule_sets](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L76)                          | list | `[]`                                   |
| [singbox_config_experimental](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L79)                             | dict | `{}`                                   |
| [singbox_config_experimental.**cache_file**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L80)              | dict | `{}`                                   |
| [singbox_config_experimental.cache_file.**enabled**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/config.yml#L81)      | bool | `True`                                 |

#### File: defaults/main/download.yml

| Var                                                                                                                                                                     | Type | Value                                                                                                                                                                                                                     |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [singbox_download_version](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/download.yml#L3)                       | str  | `latest`                                                                                                                                                                                                                  |
| [singbox_download_github_user](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/download.yml#L6)                   | str  | `SagerNet`                                                                                                                                                                                                                |
| [singbox_download_github_repository](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/download.yml#L9)             | str  | `sing-box`                                                                                                                                                                                                                |
| [singbox_download_architecture_map](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/download.yml#L12)             | dict | `{}`                                                                                                                                                                                                                      |
| [singbox_download_architecture_map.**x86_64**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/download.yml#L13)  | str  | `amd64`                                                                                                                                                                                                                   |
| [singbox_download_architecture_map.**aarch64**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/download.yml#L14) | str  | `arm64`                                                                                                                                                                                                                   |
| [singbox_download_url](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/download.yml#L17)                          | str  | `https://github.com/{{ singbox_download_github_user }}/{{ singbox_download_github_repository }}/releases/download/v{{ download_version }}/sing-box-{{ download_version }}-linux-{{ download_architecture.value }}.tar.gz` |

#### File: defaults/main/install.yml

| Var                                                                                                                                                           | Type | Value                  |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ---------------------- |
| [singbox_install_extract_options](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/install.yml#L3)       | list | `[]`                   |
| [singbox_install_extract_options.**0**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/install.yml#L3) | str  | `--wildcards`          |
| [singbox_install_extract_options.**1**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/install.yml#L3) | str  | `--strip-components=1` |
| [singbox_install_extract_include](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/install.yml#L6)       | list | `[]`                   |
| [singbox_install_extract_include.**0**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/defaults/main/install.yml#L6) | str  | `*/sing-box`           |

### Vars

**These are variables with higher priority**

#### File: vars/main/config.yml

| Var                                                                                                                                    | Type | Value                                                                                       |
| -------------------------------------------------------------------------------------------------------------------------------------- | ---- | ------------------------------------------------------------------------------------------- |
| [singbox_config_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/vars/main/config.yml#L3)  | str  | `/etc/sing-box`                                                                             |
| [singbox_config_file](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/vars/main/config.yml#L6) | str  | `{{ (singbox_config_dir, singbox_config_instance ~ '.json') ¦ ansible.builtin.path_join }}` |

#### File: vars/main/download.yml

| Var                                                                                                                                              | Type | Value                                                                                                   |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | ---- | ------------------------------------------------------------------------------------------------------- |
| [singbox_download_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/vars/main/download.yml#L3)  | str  | `{{ (singbox_cache_local_dir, 'download') ¦ ansible.builtin.path_join }}`                               |
| [singbox_download_local_file](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/vars/main/download.yml#L6) | str  | `{{ (singbox_download_local_dir, 'current', ansible_facts.architecture) ¦ ansible.builtin.path_join }}` |

#### File: vars/main/install.yml

| Var                                                                                                                                        | Type | Value                                                               |
| ------------------------------------------------------------------------------------------------------------------------------------------ | ---- | ------------------------------------------------------------------- |
| [singbox_install_binary](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/vars/main/install.yml#L3) | str  | `{{ (common_binary_dir, 'sing-box') ¦ ansible.builtin.path_join }}` |

#### File: vars/main/main.yml

| Var                                                                                                                                         | Type | Value                                                                      |
| ------------------------------------------------------------------------------------------------------------------------------------------- | ---- | -------------------------------------------------------------------------- |
| [singbox_cache_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/vars/main/main.yml#L3)    | str  | `{{ (common_cache_local_dir, 'singbox') ¦ ansible.builtin.path_join }}`    |
| [singbox_artifact_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/vars/main/main.yml#L6) | str  | `{{ (common_artifact_local_dir, 'singbox') ¦ ansible.builtin.path_join }}` |

### Tasks

#### File: tasks/config.yml

| Name                                                                                                                                           | Module                   | Has Conditions |
| ---------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------ | -------------- |
| [Render sing-box config template](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/tasks/config.yml#L2) | ansible.builtin.template | False          |

#### File: tasks/download.yml

| Name                                                                                                                                                     | Module                           | Has Conditions |
| -------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------- | -------------- |
| [Get latest sing-box version](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/tasks/download.yml#L2)             | block                            | True           |
| [Fetch latest sing-box release on GitHub](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/tasks/download.yml#L5) | community.general.github_release | False          |
| [Set sing-box version fact](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/tasks/download.yml#L13)              | ansible.builtin.set_fact         | False          |
| [Download sing-box archive](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/tasks/download.yml#L17)              | ansible.builtin.include_role     | False          |

#### File: tasks/install.yml

| Name                                                                                                                                                | Module                    | Has Conditions |
| --------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------- | -------------- |
| [Create sing-box directories](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/tasks/install.yml#L2)         | ansible.builtin.file      | False          |
| [Extract sing-box archive](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/tasks/install.yml#L12)           | ansible.builtin.unarchive | False          |
| [Install sing-box service](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/tasks/install.yml#L22)           | block                     | False          |
| [Install sing-box service (systemd)](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/tasks/install.yml#L25) | ansible.builtin.template  | True           |

#### File: tasks/main.yml

| Name                                                                                                                             | Module                        | Has Conditions | Tags            |
| -------------------------------------------------------------------------------------------------------------------------------- | ----------------------------- | -------------- | --------------- |
| [Download sing-box](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/tasks/main.yml#L2)   | ansible.builtin.include_tasks | False          | download,packer |
| [Install sing-box](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/tasks/main.yml#L12)   | ansible.builtin.include_tasks | False          | install,packer  |
| [Configure sing-box](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/tasks/main.yml#L19) | ansible.builtin.include_tasks | False          | c,o,n,f,i,g     |
| [Flush handlers](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/singbox/tasks/main.yml#L26)     | ansible.builtin.meta          | False          | a,l,w,a,y,s     |

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
