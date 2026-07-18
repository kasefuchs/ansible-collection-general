===============================
Kasefuchs.General Release Notes
===============================

.. contents:: Topics

v1.3.1
======

Release Summary
---------------

Added custom registries and auto-deploy manifests support to the k3s role.

Minor Changes
-------------

- Added support for auto-deploying Kubernetes manifests in the `k3s` server role via `k3s_server_config_manifests`.
- Added support for configuring custom containerd registries in the `k3s` role via `k3s_config_registries`.

v1.3.0
======

Release Summary
---------------

Codebase cleanup, YAML formatting overhaul, and minor bugfixes.

Minor Changes
-------------

- Reformatted YAML files (removed document start markers `---`, converted inline arrays to block lists).
- Removed unnecessary `ansible.builtin.` prefixes from standard Jinja2 filters and lookups across all roles to improve readability.
- Replaced Prettier with `yamlfmt` for YAML code formatting.

Bugfixes
--------

- Added explicit boolean casting (`| bool`) to conditionals in the `amneziawg` role to prevent evaluation errors.

v1.2.2
======

Release Summary
---------------

Improved config variable structure and naming.

Minor Changes
-------------

- Refactored sing-box configuration variables.
- Renamed `amneziawg_config_name` to `amneziawg_config_instance`.
- Renamed `singbox_config_name` to `singbox_config_instance`.

v1.2.1
======

Release Summary
---------------

Added new singbox role.

Minor Changes
-------------

- Added new `singbox` role.

v1.2.0
======

Release Summary
---------------

Maintenance release improving development tooling and linting.

Major Changes
-------------

- Increased the minimum supported Ansible version to 2.15.0.

Minor Changes
-------------

- Added ansible-lint configuration.
- Added antsibull changelogs.
- Added prettier formatting configuration.

Bugfixes
--------

- Fixed change detection in several command tasks.
