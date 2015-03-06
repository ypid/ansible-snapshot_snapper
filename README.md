## snapshot_snapper

[![Ansible Galaxy](http://img.shields.io/badge/galaxy-ypid.snapshot_snapper-660198.svg?style=flat)](https://galaxy.ansible.com/list#/roles/3042)
[![Platforms](http://img.shields.io/badge/platforms-debian%20/%20ubuntu-lightgrey.svg?style=flat)](#)


Configure snapshots with snapper.

Snapper can manage snapshots for the following filesystems vlume manges:

* btrfs
* ext4
* lvm2

This role allows to setup and configure snapper with Ansible.

### Installation

This role requires at least Ansible `v1.3`. To install it, run:

    ansible-galaxy install ypid.snapshot_snapper

To install via git, run either:

    git clone https://github.com/ypid/ansible-snapshot_snapper ypid.snapshot_snapper
    git submodule add https://github.com/ypid/ansible-snapshot_snapper roles/ypid.snapshot_snapper




### Role variables

List of default variables available in the inventory:

    ---
    
    # "Global" sub volume snapshots
    btrfs_snapper_snapshot_subvols_list:
    
    # "Host group" sub volume snapshots
    btrfs_snapper_snapshot_subvols_group_list:
    
    # "Host" sub volume snapshots
    btrfs_snapper_snapshot_subvols_host_list:
      # - path: "/home/btrfs-testings"
        # name: "btrfs-tests"
    
    # Sets the default timeline limit for snapper. If empty, the default of snapper
    # will be left unchanged.
    btrfs_snapper_defaults:
      TIMELINE_LIMIT_HOURLY:
      TIMELINE_LIMIT_DAILY:
      TIMELINE_LIMIT_MONTHLY:
      TIMELINE_LIMIT_YEARLY: 2
    
    btrfs_snapper_snapshot_directory: ".snapshots"
    btrfs_snapper_config_templates_dir: "/etc/snapper/config-templates"
    btrfs_snapper_updatedb_coniguration_files:
      - "/etc/updatedb.conf"




### Authors and license

`snapshot_snapper` role was written by:

- [Robin Schneider](https://github.com/ypid) | [e-mail](mailto:ypid@riseup.net)

License: [AGPLv3](https://tldrlegal.com/license/gnu-affero-general-public-license-v3-%28agpl-3.0%29)

***

README generated by [Ansigenome](https://github.com/nickjj/ansigenome/).