<!-- DOCSIBLE START -->

# 📃 Role overview

## download_url

```
Role belongs to kasefuchs/general
Namespace - kasefuchs
Collection - general
Version - 1.3.1
Repository - https://codeberg.org/kasefuchs/ansible-collection-general
```

Description: Generic reusable download role that fetches and manages versioned binaries and archives with multi-architecture support.


| Field                | Value           |
|--------------------- |-----------------|
| Readme update        | 2026/02/15 |








### Defaults

**These are static variables with lower priority**

#### File: defaults/main.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [download_url_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_url/defaults/main.yml#L2)   | str | `{{ undef('Download directory must be provided (download_url_dir)') }}` |
| [download_url_source](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_url/defaults/main.yml#L5)   | str | `{{ undef('Download url must be provided (download_url_source)') }}` |
| [download_url_version](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_url/defaults/main.yml#L8)   | str | `{{ undef('Download version must be provided (download_url_version)') }}` |
| [download_url_architecture_map](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_url/defaults/main.yml#L11)   | str | `{{ undef('Download architecture mapping must be provided (download_url_architecture_map)') }}` |


### Vars

**These are variables with higher priority**
#### File: vars/main.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [download_url_current_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_url/vars/main.yml#L2)   | str | `{{ (download_url_dir, download_url_version) ¦ path_join }}` |
| [download_url_current_dir_link](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_url/vars/main.yml#L5)   | str | `{{ (download_url_dir, 'current') ¦ path_join }}` |
| [download_url_unique_architectures](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_url/vars/main.yml#L8)   | str | `{{ common_unique_architectures + ['noarch'] }}` |


### Tasks


#### File: tasks/main.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Link current version directory](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_url/tasks/main.yml#L9) | block | False |
| [Create version directory](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_url/tasks/main.yml#L3) | ansible.builtin.file | False |
| [Link current version directory](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_url/tasks/main.yml#L9) | ansible.builtin.file | False |
| [Download files](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_url/tasks/main.yml#L26) | block | False |
| [Check if files already downloaded](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_url/tasks/main.yml#L17) | ansible.builtin.stat | False |
| [Download files](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_url/tasks/main.yml#L26) | ansible.builtin.get_url | True |







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
