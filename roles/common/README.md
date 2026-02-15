<!-- DOCSIBLE START -->

# 📃 Role overview

## common

```
Role belongs to kasefuchs/general
Namespace - kasefuchs
Collection - general
Version - 0.1.0
Repository - https://codeberg.org/kasefuchs/ansible-collection-general
```

Description: Common helper role providing shared variables, paths, and handlers used across other roles in the collection.


| Field                | Value           |
|--------------------- |-----------------|
| Readme update        | 2026/02/15 |











### Vars

**These are variables with higher priority**
#### File: vars/main.yml

| Var          | Type         | Value       |
|--------------|--------------|-------------|
| [common_inventory_name](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/common/vars/main.yml#L3)   | str | `{{ inventory_dir ¦ ansible.builtin.basename }}` |
| [common_managed_header](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/common/vars/main.yml#L6)   | str | `Managed by Ansible ¦ Template: {{ template_path if not template_path.startswith('/') else (template_path ¦ basename) }} (last modified: {{ template_mtime.strftime('%Y-%m-%d %H:%M:%S') }})` |
| [common_cache_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/common/vars/main.yml#L9)   | str | `{{ (playbook_dir, '../cache') ¦ ansible.builtin.path_join }}` |
| [common_artifact_local_dir](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/common/vars/main.yml#L12)   | str | `{{ (playbook_dir, '../artifacts', common_inventory_name) ¦ ansible.builtin.path_join }}` |
| [common_unique_architectures](https://codeberg.org/kasefuchs/ansible-collection-general/src/branch/main/roles/common/vars/main.yml#L15)   | str | `{{ ansible_play_hosts ¦ map('ansible.builtin.extract', hostvars, ['ansible_facts', 'architecture']) ¦ unique }}` |


### Tasks








## Author Information
Kasefuchs

#### License

MIT

#### Minimum Ansible Version

2.2

#### Platforms

No platforms specified.

#### Dependencies

No dependencies specified.
<!-- DOCSIBLE END -->
