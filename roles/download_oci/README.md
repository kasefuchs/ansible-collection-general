<!-- DOCSIBLE START -->

# 📃 Role overview

## download_oci

```
Role belongs to kasefuchs/general
Namespace - kasefuchs
Collection - general
Version - 1.3.1
Repository - https://codeberg.org/kasefuchs/ansible-collection-general
```

Description: Generic reusable download role that fetches and manages versioned OCI container images as tar archives with multi-architecture support.


| Field                | Value           |
|--------------------- |-----------------|
| Readme update        | 2026/02/15 |








### Defaults

**These are static variables with lower priority**

#### File: defaults/main.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [download_oci_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_oci/defaults/main.yml#L2)   | str | `{{ undef('Download directory must be provided (download_oci_dir)') }}` |
| [download_oci_source](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_oci/defaults/main.yml#L5)   | str | `{{ undef('Download url must be provided (download_oci_source)') }}` |
| [download_oci_version](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_oci/defaults/main.yml#L8)   | str | `{{ undef('Download version must be provided (download_oci_version)') }}` |


### Vars

**These are variables with higher priority**
#### File: vars/main.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [download_oci_current_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_oci/vars/main.yml#L2)   | str | `{{ (download_oci_dir, download_oci_version) ¦ path_join }}` |
| [download_oci_current_dir_link](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_oci/vars/main.yml#L5)   | str | `{{ (download_oci_dir, 'current') ¦ path_join }}` |
| [download_oci_architecture_map](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_oci/vars/main.yml#L8)   | dict | `{}` |
| [download_oci_architecture_map.**x86_64**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_oci/vars/main.yml#L9)   | str | `amd64` |
| [download_oci_architecture_map.**aarch64**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_oci/vars/main.yml#L10)   | str | `arm64` |
| [download_oci_architecture_map.**armv7l**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_oci/vars/main.yml#L11)   | str | `arm` |
| [download_oci_architecture_map.**armv6l**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_oci/vars/main.yml#L12)   | str | `arm` |
| [download_oci_architecture_map.**riscv64**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_oci/vars/main.yml#L13)   | str | `riscv64` |
| [download_oci_architecture_map.**ppc64le**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_oci/vars/main.yml#L14)   | str | `ppc64le` |
| [download_oci_architecture_map.**s390x**](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_oci/vars/main.yml#L15)   | str | `s390x` |


### Tasks


#### File: tasks/main.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| [Link current version directory](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_oci/tasks/main.yml#L9) | block | False |
| [Create version directory](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_oci/tasks/main.yml#L3) | ansible.builtin.file | False |
| [Link current version directory](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_oci/tasks/main.yml#L9) | ansible.builtin.file | False |
| [Download files](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_oci/tasks/main.yml#L26) | block | False |
| [Check if files already downloaded](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_oci/tasks/main.yml#L17) | ansible.builtin.stat | False |
| [Download files](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/download_oci/tasks/main.yml#L26) | ansible.builtin.command | True |







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
