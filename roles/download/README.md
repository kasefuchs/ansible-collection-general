<!-- DOCSIBLE START -->

# 📃 Role overview

## download

```
Role belongs to kasefuchs/general
Namespace - kasefuchs
Collection - general
Version - 1.1.2
Repository - https://codeberg.org/kasefuchs/ansible-collection-general
```

Description: Generic reusable download role that fetches and manages versioned binaries and archives with multi-architecture support.

| Field         | Value      |
| ------------- | ---------- |
| Readme update | 2026/02/15 |

### Defaults

**These are static variables with lower priority**

#### File: defaults/main.yml

| Var                                                                                                                                                     | Type | Value                                                               |
| ------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ------------------------------------------------------------------- |
| [download_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download/defaults/main.yml#L3)                           | str  | `{{ undef('Download directory must be provided (download_dir)') }}` |
| [download_url](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download/defaults/main.yml#L6)                           | str  | `{{ undef('Download url must be provided (download_url)') }}`       |
| [download_version](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download/defaults/main.yml#L9)                       | str  | `{{ undef('Download version be provided (download_version)') }}`    |
| [download_architecture_map](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download/defaults/main.yml#L12)             | dict | `{}`                                                                |
| [download_architecture_map.**x86_64**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download/defaults/main.yml#L13)  | str  | `amd64`                                                             |
| [download_architecture_map.**aarch64**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download/defaults/main.yml#L14) | str  | `arm64`                                                             |

### Vars

**These are variables with higher priority**

#### File: vars/main.yml

| Var                                                                                                                                    | Type | Value                                                                |
| -------------------------------------------------------------------------------------------------------------------------------------- | ---- | -------------------------------------------------------------------- |
| [download_current_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download/vars/main.yml#L3)      | str  | `{{ (download_dir, download_version) ¦ ansible.builtin.path_join }}` |
| [download_current_dir_link](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download/vars/main.yml#L6) | str  | `{{ (download_dir, 'current') ¦ ansible.builtin.path_join }}`        |

### Tasks

#### File: tasks/main.yml

| Name                                                                                                                                             | Module                  | Has Conditions |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------- | -------------- |
| [Link current version directory](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download/tasks/main.yml#L10)    | block                   | False          |
| [Create version directory](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download/tasks/main.yml#L4)           | ansible.builtin.file    | False          |
| [Link current version directory](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download/tasks/main.yml#L10)    | ansible.builtin.file    | False          |
| [Download files](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download/tasks/main.yml#L27)                    | block                   | False          |
| [Check if files already downloaded](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download/tasks/main.yml#L18) | ansible.builtin.stat    | False          |
| [Download files](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download/tasks/main.yml#L27)                    | ansible.builtin.get_url | True           |

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
