# ansible_1
ansible -m apt -a 'update_cache=yes' web
ansible -m apt -a 'name=nginx state=latest' web
ansible -m service -a 'name=nginx state=started' web
ansible -m apt -a 'name=vsftpd state=latest' web
ansible -m service -a 'name=vsftpd state=started' web
ansible -m apt -a 'name=nano state=latest' web
ansible -m group -a 'name=students' web
ansible -m user -a 'name=student groups=students password=studentpass home=/user/student' web
ansible -m file -a 'path=/user/student/dir owner=student group=students mode=0754 state=directory' web
ansible -m setup web
s2 | SUCCESS => {
    "ansible_facts": {
        "ansible_all_ipv4_addresses": [
            "10.128.0.25"
        ],
        "ansible_all_ipv6_addresses": [
            "fe80::4001:aff:fe80:19"
        ],
        "ansible_apparmor": {
            "status": "enabled"
        },
        "ansible_architecture": "x86_64",
        "ansible_bios_date": "01/01/2011",
        "ansible_bios_version": "Google",
        "ansible_cmdline": {
            "BOOT_IMAGE": "/boot/vmlinuz-5.4.0-1036-gcp",
            "console": "ttyS0",
            "panic": "-1",
            "ro": true,
            "root": "PARTUUID=6a40708a-dbcd-4e45-8469-8ba0fce0f2fa"
        },
        "ansible_date_time": {
            "date": "2021-03-11",
            "day": "11",
            "epoch": "1615470387",
            "hour": "13",
            "iso8601": "2021-03-11T13:46:27Z",
            "iso8601_basic": "20210311T134627601037",
            "iso8601_basic_short": "20210311T134627",
            "iso8601_micro": "2021-03-11T13:46:27.601125Z",
            "minute": "46",
            "month": "03",
            "second": "27",
            "time": "13:46:27",
            "tz": "UTC",
            "tz_offset": "+0000",
            "weekday": "Thursday",
            "weekday_number": "4",
            "weeknumber": "10",
            "year": "2021"
        },
        "ansible_default_ipv4": {
            "address": "10.128.0.25",
            "alias": "ens4",
            "broadcast": "global",
            "gateway": "10.128.0.1",
            "interface": "ens4",
            "macaddress": "42:01:0a:80:00:19",
            "mtu": 1460,
            "netmask": "255.255.255.255",
            "network": "10.128.0.25",
            "type": "ether"
        },
        "ansible_default_ipv6": {},
        "ansible_device_links": {
            "ids": {
                "sda": [
                    "google-sl2",
                    "scsi-0Google_PersistentDisk_sl2"
                ],
                "sda1": [
                    "google-sl2-part1",
                    "scsi-0Google_PersistentDisk_sl2-part1"
                ],
                "sda14": [
                    "google-sl2-part14",
                    "scsi-0Google_PersistentDisk_sl2-part14"
                ],
                "sda15": [
                    "google-sl2-part15",
                    "scsi-0Google_PersistentDisk_sl2-part15"
                ]
            },
            "labels": {
                "sda1": [
                    "cloudimg-rootfs"
                ],
                "sda15": [
                    "UEFI"
                ]
            },
            "masters": {},
            "uuids": {
                "sda1": [
                    "c032eea3-a219-43e3-af6d-a1686f63e91f"
                ],
                "sda15": [
                    "945A-1D2E"
                ]
            }
        },
        "ansible_devices": {
            "loop0": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "none",
                "sectors": "113592",
                "sectorsize": "512",
                "size": "55.46 MB",
                "support_discard": "4096",
                "vendor": null,
                "virtual": 1
            },
            "loop1": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "none",
                "sectors": "311000",
                "sectorsize": "512",
                "size": "151.86 MB",
                "support_discard": "4096",
                "vendor": null,
                "virtual": 1
            },
            "loop2": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "none",
                "sectors": "143120",
                "sectorsize": "512",
                "size": "69.88 MB",
                "support_discard": "4096",
                "vendor": null,
                "virtual": 1
            },
            "loop3": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "none",
                "sectors": "63664",
                "sectorsize": "512",
                "size": "31.09 MB",
                "support_discard": "4096",
                "vendor": null,
                "virtual": 1
            },
            "loop4": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "none",
                "sectors": "66104",
                "sectorsize": "512",
                "size": "32.28 MB",
                "support_discard": "4096",
                "vendor": null,
                "virtual": 1
            },
            "loop5": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "none",
                "sectors": "385384",
                "sectorsize": "512",
                "size": "188.18 MB",
                "support_discard": "4096",
                "vendor": null,
                "virtual": 1
            },
            "loop6": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "none",
                "sectors": "0",
                "sectorsize": "512",
                "size": "0.00 Bytes",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "loop7": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "none",
                "sectors": "0",
                "sectorsize": "512",
                "size": "0.00 Bytes",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "md0": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "0",
                "sectorsize": "512",
                "size": "0.00 Bytes",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "sda": {
                "holders": [],
                "host": "Non-VGA unclassified device: Red Hat, Inc. Virtio SCSI",
                "links": {
                    "ids": [
                        "google-sl2",
                        "scsi-0Google_PersistentDisk_sl2"
                    ],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": "PersistentDisk",
                "partitions": {
                    "sda1": {
                        "holders": [],
                        "links": {
                            "ids": [
                                "google-sl2-part1",
                                "scsi-0Google_PersistentDisk_sl2-part1"
                            ],
                            "labels": [
                                "cloudimg-rootfs"
                            ],
                            "masters": [],
                            "uuids": [
                                "c032eea3-a219-43e3-af6d-a1686f63e91f"
                            ]
                        },
                        "sectors": "20744159",
                        "sectorsize": 512,
                        "size": "9.89 GB",
                        "start": "227328",
                        "uuid": "c032eea3-a219-43e3-af6d-a1686f63e91f"
                    },
                    "sda14": {
                        "holders": [],
                        "links": {
                            "ids": [
                                "google-sl2-part14",
                                "scsi-0Google_PersistentDisk_sl2-part14"
                            ],
                            "labels": [],
                            "masters": [],
                            "uuids": []
                        },
                        "sectors": "8192",
                        "sectorsize": 512,
                        "size": "4.00 MB",
                        "start": "2048",
                        "uuid": null
                    },
                    "sda15": {
                        "holders": [],
                        "links": {
                            "ids": [
                                "google-sl2-part15",
                                "scsi-0Google_PersistentDisk_sl2-part15"
                            ],
                            "labels": [
                                "UEFI"
                            ],
                            "masters": [],
                            "uuids": [
                                "945A-1D2E"
                            ]
                        },
                        "sectors": "217088",
                        "sectorsize": 512,
                        "size": "106.00 MB",
                        "start": "10240",
                        "uuid": "945A-1D2E"
                    }
                },
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "none",
                "sectors": "20971520",
                "sectorsize": "512",
                "size": "10.00 GB",
                "support_discard": "4096",
                "vendor": "Google",
                "virtual": 1
            }
        },
        "ansible_distribution": "Ubuntu",
        "ansible_distribution_file_parsed": true,
        "ansible_distribution_file_path": "/etc/os-release",
        "ansible_distribution_file_variety": "Debian",
        "ansible_distribution_major_version": "20",
        "ansible_distribution_release": "focal",
        "ansible_distribution_version": "20.04",
        "ansible_dns": {
            "nameservers": [
                "127.0.0.53"
            ],
            "options": {
                "edns0": true,
                "trust-ad": true
            },
            "search": [
                "us-central1-a.c.amazing-zephyr-304415.internal",
                "c.amazing-zephyr-304415.internal",
                "google.internal"
            ]
        },
        "ansible_domain": "us-central1-a.c.amazing-zephyr-304415.internal",
        "ansible_effective_group_id": 0,
        "ansible_effective_user_id": 0,
        "ansible_ens4": {
            "active": true,
            "device": "ens4",
            "features": {
                "esp_hw_offload": "off [fixed]",
                "esp_tx_csum_hw_offload": "off [fixed]",
                "fcoe_mtu": "off [fixed]",
                "generic_receive_offload": "on",
                "generic_segmentation_offload": "on",
                "highdma": "on [fixed]",
                "hw_tc_offload": "off [fixed]",
                "l2_fwd_offload": "off [fixed]",
                "large_receive_offload": "on",
                "loopback": "off [fixed]",
                "netns_local": "off [fixed]",
                "ntuple_filters": "off [fixed]",
                "receive_hashing": "off [fixed]",
                "rx_all": "off [fixed]",
                "rx_checksumming": "on [fixed]",
                "rx_fcs": "off [fixed]",
                "rx_gro_hw": "off [fixed]",
                "rx_udp_tunnel_port_offload": "off [fixed]",
                "rx_vlan_filter": "off [fixed]",
                "rx_vlan_offload": "off [fixed]",
                "rx_vlan_stag_filter": "off [fixed]",
                "rx_vlan_stag_hw_parse": "off [fixed]",
                "scatter_gather": "on",
                "tcp_segmentation_offload": "on",
                "tls_hw_record": "off [fixed]",
                "tls_hw_rx_offload": "off [fixed]",
                "tls_hw_tx_offload": "off [fixed]",
                "tx_checksum_fcoe_crc": "off [fixed]",
                "tx_checksum_ip_generic": "on",
                "tx_checksum_ipv4": "off [fixed]",
                "tx_checksum_ipv6": "off [fixed]",
                "tx_checksum_sctp": "off [fixed]",
                "tx_checksumming": "on",
                "tx_esp_segmentation": "off [fixed]",
                "tx_fcoe_segmentation": "off [fixed]",
                "tx_gre_csum_segmentation": "off [fixed]",
                "tx_gre_segmentation": "off [fixed]",
                "tx_gso_partial": "off [fixed]",
                "tx_gso_robust": "on [fixed]",
                "tx_ipxip4_segmentation": "off [fixed]",
                "tx_ipxip6_segmentation": "off [fixed]",
                "tx_lockless": "off [fixed]",
                "tx_nocache_copy": "off",
                "tx_scatter_gather": "on",
                "tx_scatter_gather_fraglist": "off [fixed]",
                "tx_sctp_segmentation": "off [fixed]",
                "tx_tcp6_segmentation": "on",
                "tx_tcp_ecn_segmentation": "off [fixed]",
                "tx_tcp_mangleid_segmentation": "off",
                "tx_tcp_segmentation": "on",
                "tx_udp_segmentation": "off [fixed]",
                "tx_udp_tnl_csum_segmentation": "off [fixed]",
                "tx_udp_tnl_segmentation": "off [fixed]",
                "tx_vlan_offload": "off [fixed]",
                "tx_vlan_stag_hw_insert": "off [fixed]",
                "vlan_challenged": "off [fixed]"
            },
            "hw_timestamp_filters": [],
            "ipv4": {
                "address": "10.128.0.25",
                "broadcast": "global",
                "netmask": "255.255.255.255",
                "network": "10.128.0.25"
            },
            "ipv6": [
                {
                    "address": "fe80::4001:aff:fe80:19",
                    "prefix": "64",
                    "scope": "link"
                }
            ],
            "macaddress": "42:01:0a:80:00:19",
            "module": "virtio_net",
            "mtu": 1460,
            "pciid": "virtio1",
            "promisc": false,
            "speed": -1,
            "timestamping": [
                "tx_software",
                "rx_software",
                "software"
            ],
            "type": "ether"
        },
        "ansible_env": {
            "HOME": "/root",
            "LANG": "C.UTF-8",
            "LOGNAME": "root",
            "MAIL": "/var/mail/root",
            "PATH": "/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/snap/bin",
            "PWD": "/home/ansible",
            "SHELL": "/bin/bash",
            "SUDO_COMMAND": "/bin/sh -c echo BECOME-SUCCESS-kpzsjecpoicaxjsexjezjezlrqxzhjrd ; /usr/bin/python3 /home/ansible/.ansible/tmp/ansible-tmp-1615470386.3336105-234940090488683/AnsiballZ_setup.py",
            "SUDO_GID": "1005",
            "SUDO_UID": "1004",
            "SUDO_USER": "ansible",
            "TERM": "xterm",
            "USER": "root"
        },
        "ansible_fibre_channel_wwn": [],
        "ansible_fips": false,
        "ansible_form_factor": "Other",
        "ansible_fqdn": "sl2.us-central1-a.c.amazing-zephyr-304415.internal",
        "ansible_hostname": "sl2",
        "ansible_hostnqn": "nqn.2014-08.org.nvmexpress:uuid:b4706220-4be8-46c1-9a55-5839b2e76903",
        "ansible_interfaces": [
            "ens4",
            "lo"
        ],
        "ansible_is_chroot": false,
        "ansible_iscsi_iqn": "",
        "ansible_kernel": "5.4.0-1036-gcp",
        "ansible_kernel_version": "#39-Ubuntu SMP Thu Jan 14 18:41:17 UTC 2021",
        "ansible_lo": {
            "active": true,
            "device": "lo",
            "features": {
                "esp_hw_offload": "off [fixed]",
                "esp_tx_csum_hw_offload": "off [fixed]",
                "fcoe_mtu": "off [fixed]",
                "generic_receive_offload": "on",
                "generic_segmentation_offload": "on",
                "highdma": "on [fixed]",
                "hw_tc_offload": "off [fixed]",
                "l2_fwd_offload": "off [fixed]",
                "large_receive_offload": "off [fixed]",
                "loopback": "on [fixed]",
                "netns_local": "on [fixed]",
                "ntuple_filters": "off [fixed]",
                "receive_hashing": "off [fixed]",
                "rx_all": "off [fixed]",
                "rx_checksumming": "on [fixed]",
                "rx_fcs": "off [fixed]",
                "rx_gro_hw": "off [fixed]",
                "rx_udp_tunnel_port_offload": "off [fixed]",
                "rx_vlan_filter": "off [fixed]",
                "rx_vlan_offload": "off [fixed]",
                "rx_vlan_stag_filter": "off [fixed]",
                "rx_vlan_stag_hw_parse": "off [fixed]",
                "scatter_gather": "on",
                "tcp_segmentation_offload": "on",
                "tls_hw_record": "off [fixed]",
                "tls_hw_rx_offload": "off [fixed]",
                "tls_hw_tx_offload": "off [fixed]",
                "tx_checksum_fcoe_crc": "off [fixed]",
                "tx_checksum_ip_generic": "on [fixed]",
                "tx_checksum_ipv4": "off [fixed]",
                "tx_checksum_ipv6": "off [fixed]",
                "tx_checksum_sctp": "on [fixed]",
                "tx_checksumming": "on",
                "tx_esp_segmentation": "off [fixed]",
                "tx_fcoe_segmentation": "off [fixed]",
                "tx_gre_csum_segmentation": "off [fixed]",
                "tx_gre_segmentation": "off [fixed]",
                "tx_gso_partial": "off [fixed]",
                "tx_gso_robust": "off [fixed]",
                "tx_ipxip4_segmentation": "off [fixed]",
                "tx_ipxip6_segmentation": "off [fixed]",
                "tx_lockless": "on [fixed]",
                "tx_nocache_copy": "off [fixed]",
                "tx_scatter_gather": "on [fixed]",
                "tx_scatter_gather_fraglist": "on [fixed]",
                "tx_sctp_segmentation": "on",
                "tx_tcp6_segmentation": "on",
                "tx_tcp_ecn_segmentation": "on",
                "tx_tcp_mangleid_segmentation": "on",
                "tx_tcp_segmentation": "on",
                "tx_udp_segmentation": "off [fixed]",
                "tx_udp_tnl_csum_segmentation": "off [fixed]",
                "tx_udp_tnl_segmentation": "off [fixed]",
                "tx_vlan_offload": "off [fixed]",
                "tx_vlan_stag_hw_insert": "off [fixed]",
                "vlan_challenged": "on [fixed]"
            },
            "hw_timestamp_filters": [],
            "ipv4": {
                "address": "127.0.0.1",
                "broadcast": "host",
                "netmask": "255.0.0.0",
                "network": "127.0.0.0"
            },
            "ipv6": [
                {
                    "address": "::1",
                    "prefix": "128",
                    "scope": "host"
                }
            ],
            "mtu": 65536,
            "promisc": false,
            "timestamping": [
                "tx_software",
                "rx_software",
                "software"
            ],
            "type": "loopback"
        },
        "ansible_local": {},
        "ansible_lsb": {
            "codename": "focal",
            "description": "Ubuntu 20.04.2 LTS",
            "id": "Ubuntu",
            "major_release": "20",
            "release": "20.04"
        },
        "ansible_lvm": {
            "lvs": {},
            "pvs": {},
            "vgs": {}
        },
        "ansible_machine": "x86_64",
        "ansible_machine_id": "ea43af460269721cbaf3909ac2316360",
        "ansible_memfree_mb": 2638,
        "ansible_memory_mb": {
            "nocache": {
                "free": 3622,
                "used": 313
            },
            "real": {
                "free": 2638,
                "total": 3935,
                "used": 1297
            },
            "swap": {
                "cached": 0,
                "free": 0,
                "total": 0,
                "used": 0
            }
        },
        "ansible_memtotal_mb": 3935,
        "ansible_mounts": [
            {
                "block_available": 2019054,
                "block_size": 4096,
                "block_total": 2495808,
                "block_used": 476754,
                "device": "/dev/root",
                "fstype": "ext4",
                "inode_available": 1217443,
                "inode_total": 1290240,
                "inode_used": 72797,
                "mount": "/",
                "options": "rw,relatime",
                "size_available": 8270045184,
                "size_total": 10222829568,
                "uuid": "c032eea3-a219-43e3-af6d-a1686f63e91f"
            },
            {
                "block_available": 0,
                "block_size": 131072,
                "block_total": 444,
                "block_used": 444,
                "device": "/dev/loop0",
                "fstype": "squashfs",
                "inode_available": 0,
                "inode_total": 10817,
                "inode_used": 10817,
                "mount": "/snap/core18/1988",
                "options": "ro,nodev,relatime",
                "size_available": 0,
                "size_total": 58195968,
                "uuid": "N/A"
            },
            {
                "block_available": 0,
                "block_size": 131072,
                "block_total": 1215,
                "block_used": 1215,
                "device": "/dev/loop1",
                "fstype": "squashfs",
                "inode_available": 0,
                "inode_total": 37243,
                "inode_used": 37243,
                "mount": "/snap/google-cloud-sdk/168",
                "options": "ro,nodev,relatime",
                "size_available": 0,
                "size_total": 159252480,
                "uuid": "N/A"
            },
            {
                "block_available": 0,
                "block_size": 131072,
                "block_total": 560,
                "block_used": 560,
                "device": "/dev/loop2",
                "fstype": "squashfs",
                "inode_available": 0,
                "inode_total": 1578,
                "inode_used": 1578,
                "mount": "/snap/lxd/19188",
                "options": "ro,nodev,relatime",
                "size_available": 0,
                "size_total": 73400320,
                "uuid": "N/A"
            },
            {
                "block_available": 0,
                "block_size": 131072,
                "block_total": 249,
                "block_used": 249,
                "device": "/dev/loop3",
                "fstype": "squashfs",
                "inode_available": 0,
                "inode_total": 470,
                "inode_used": 470,
                "mount": "/snap/snapd/11036",
                "options": "ro,nodev,relatime",
                "size_available": 0,
                "size_total": 32636928,
                "uuid": "N/A"
            },
            {
                "block_available": 205804,
                "block_size": 512,
                "block_total": 213716,
                "block_used": 7912,
                "device": "/dev/sda15",
                "fstype": "vfat",
                "inode_available": 0,
                "inode_total": 0,
                "inode_used": 0,
                "mount": "/boot/efi",
                "options": "rw,relatime,fmask=0022,dmask=0022,codepage=437,iocharset=iso8859-1,shortname=mixed,errors=remount-ro",
                "size_available": 105371648,
                "size_total": 109422592,
                "uuid": "945A-1D2E"
            },
            {
                "block_available": 0,
                "block_size": 131072,
                "block_total": 259,
                "block_used": 259,
                "device": "/dev/loop4",
                "fstype": "squashfs",
                "inode_available": 0,
                "inode_total": 474,
                "inode_used": 474,
                "mount": "/snap/snapd/11107",
                "options": "ro,nodev,relatime",
                "size_available": 0,
                "size_total": 33947648,
                "uuid": "N/A"
            },
            {
                "block_available": 0,
                "block_size": 131072,
                "block_total": 1506,
                "block_used": 1506,
                "device": "/dev/loop5",
                "fstype": "squashfs",
                "inode_available": 0,
                "inode_total": 37831,
                "inode_used": 37831,
                "mount": "/snap/google-cloud-sdk/172",
                "options": "ro,nodev,relatime",
                "size_available": 0,
                "size_total": 197394432,
                "uuid": "N/A"
            }
        ],
        "ansible_nodename": "sl2",
        "ansible_os_family": "Debian",
        "ansible_pkg_mgr": "apt",
        "ansible_proc_cmdline": {
            "BOOT_IMAGE": "/boot/vmlinuz-5.4.0-1036-gcp",
            "console": "ttyS0",
            "panic": "-1",
            "ro": true,
            "root": "PARTUUID=6a40708a-dbcd-4e45-8469-8ba0fce0f2fa"
        },
        "ansible_processor": [
            "0",
            "GenuineIntel",
            "Intel(R) Xeon(R) CPU @ 2.30GHz",
            "1",
            "GenuineIntel",
            "Intel(R) Xeon(R) CPU @ 2.30GHz"
        ],
        "ansible_processor_cores": 1,
        "ansible_processor_count": 1,
        "ansible_processor_threads_per_core": 2,
        "ansible_processor_vcpus": 2,
        "ansible_product_name": "Google Compute Engine",
        "ansible_product_serial": "GoogleCloud-EA43AF460269721CBAF3909AC2316360",
        "ansible_product_uuid": "ea43af46-0269-721c-baf3-909ac2316360",
        "ansible_product_version": "NA",
        "ansible_python": {
            "executable": "/usr/bin/python3",
            "has_sslcontext": true,
            "type": "cpython",
            "version": {
                "major": 3,
                "micro": 5,
                "minor": 8,
                "releaselevel": "final",
                "serial": 0
            },
            "version_info": [
                3,
                8,
                5,
                "final",
                0
            ]
        },
        "ansible_python_version": "3.8.5",
        "ansible_real_group_id": 0,
        "ansible_real_user_id": 0,
        "ansible_selinux": {
            "status": "Missing selinux Python library"
        },
        "ansible_selinux_python_present": false,
        "ansible_service_mgr": "systemd",
        "ansible_ssh_host_key_dsa_public": "AAAAB3NzaC1kc3MAAACBAO9d76FyqzdWWncMhfy9pTNvlpZMrYOsdHn2c1ic1jEh6AP0dRQxlq/I5/Ro8YqUhre73mZ9h7EiaiNG8lZhRX+GuNAtlk6GaASxM6KSAFIMcXiQMvAiJOjhcyyTUbl0R6PYo36ZiRH8tnKe6H+CzzSbEPbTj++TaW63xcyrC99HAAAAFQDHKLs+X//ftZg7eNHPAQ9ipntvPQAAAIB8nRhNdGsN5Wg3vc4AV/XmI7GFPOL5qcKQsE3rmZOx+LqG/OSbX1nIlrz9cSnnvaUeMZougVxOnBfgfyqsiwDI2KYn9sggsiYljxWGeVJuppXMPYHf+MUHHz9xcU1U3I15eSIKrRLjCfFITJIqbA1gwBCMhbdoob3MxoaujT7YFwAAAIAHWNDWCCDSFwiY6xj5SMsE9pTw4gtdmBJrZe1xQnqFXNBdAeXrlcHd6XhhT0mIrj/V6tpduxlJAQTRLhSGkra5f3eV1JvgoOMjei/XJg2uJkDWpLJQVfb8rIqAPicOMfhaPLmmk87TXc2ugYf64NIgbNLDF3dJJ7ffBNPm1wD/cw==",
        "ansible_ssh_host_key_ecdsa_public": "AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBLIHgClD4MQczxdZertuEhTZMvuxmzoJxNdGbM3csXKr6iYPS5WOQMSbQWnfU6tAED8gaLGSVzNEWIAlIaNaVnc=",
        "ansible_ssh_host_key_ed25519_public": "AAAAC3NzaC1lZDI1NTE5AAAAIHMmLuRG5cHEPfRRJqpKgjp3PUh4vBhF4eVWKSIICmVW",
        "ansible_ssh_host_key_rsa_public": "AAAAB3NzaC1yc2EAAAADAQABAAABgQCgg1ZNXsuBSnAksuW1g5Y8DoLYRof9SOdkQ3b8yNmaViU1tJ2mbEz05QGtd3+CmT3CpS6faIaX5lo7w5Nbi9wXvpVpeBLGe1NhyUBYC1EjBmuOLKqLmm9LrJrR7wCqK808JKoGC9vuqyVGf99rI9j3H+ghYFSgrkXnNLV6Ia27GTZ7WEgrDg9RsfYVUeMWLe2+lfy2szgZd+Bkxw4v3B8hL1E5dDUulBnoWQ84VbDyYb7YsStvmPJBlHIDZUpQHYArgPL5zJ/fy3FoGdHcNbTcty7X0ICpK2t81F87ZkkWcs+s8ufQvNR0htxZZ3HUuYkq41/IPIXE9HVLpVrFMqaia4uCs02d965soz1VP/+ufZkT/+BmChN+FZS67QbcR3066fLl129IGRZSl9QRegxyzRRxRpR3bevNRzULKrmN9O6Cg0YXuqBf9oSsOipqqyJFTP4C06jSTXW/zI1jdW4Q13AsFbWgNbr+1+5UmDZwiORRMJb4M8FNnN/43LTTpuc=",
        "ansible_swapfree_mb": 0,
        "ansible_swaptotal_mb": 0,
        "ansible_system": "Linux",
        "ansible_system_capabilities": [],
        "ansible_system_capabilities_enforced": "False",
        "ansible_system_vendor": "Google",
        "ansible_uptime_seconds": 5684,
        "ansible_user_dir": "/root",
        "ansible_user_gecos": "root",
        "ansible_user_gid": 0,
        "ansible_user_id": "root",
        "ansible_user_shell": "/bin/bash",
        "ansible_user_uid": 0,
        "ansible_userspace_architecture": "x86_64",
        "ansible_userspace_bits": "64",
        "ansible_virtualization_role": "guest",
        "ansible_virtualization_type": "kvm",
        "discovered_interpreter_python": "/usr/bin/python3",
        "gather_subset": [
            "all"
        ],
        "module_setup": true
    },
    "changed": false
}
s1 | SUCCESS => {
    "ansible_facts": {
        "ansible_all_ipv4_addresses": [
            "10.128.0.24"
        ],
        "ansible_all_ipv6_addresses": [
            "fe80::4001:aff:fe80:18"
        ],
        "ansible_apparmor": {
            "status": "enabled"
        },
        "ansible_architecture": "x86_64",
        "ansible_bios_date": "01/01/2011",
        "ansible_bios_version": "Google",
        "ansible_cmdline": {
            "BOOT_IMAGE": "/boot/vmlinuz-5.4.0-1036-gcp",
            "console": "ttyS0",
            "panic": "-1",
            "ro": true,
            "root": "PARTUUID=6a40708a-dbcd-4e45-8469-8ba0fce0f2fa"
        },
        "ansible_date_time": {
            "date": "2021-03-11",
            "day": "11",
            "epoch": "1615470387",
            "hour": "13",
            "iso8601": "2021-03-11T13:46:27Z",
            "iso8601_basic": "20210311T134627654662",
            "iso8601_basic_short": "20210311T134627",
            "iso8601_micro": "2021-03-11T13:46:27.654771Z",
            "minute": "46",
            "month": "03",
            "second": "27",
            "time": "13:46:27",
            "tz": "UTC",
            "tz_offset": "+0000",
            "weekday": "Thursday",
            "weekday_number": "4",
            "weeknumber": "10",
            "year": "2021"
        },
        "ansible_default_ipv4": {
            "address": "10.128.0.24",
            "alias": "ens4",
            "broadcast": "global",
            "gateway": "10.128.0.1",
            "interface": "ens4",
            "macaddress": "42:01:0a:80:00:18",
            "mtu": 1460,
            "netmask": "255.255.255.255",
            "network": "10.128.0.24",
            "type": "ether"
        },
        "ansible_default_ipv6": {},
        "ansible_device_links": {
            "ids": {
                "sda": [
                    "google-sl1",
                    "scsi-0Google_PersistentDisk_sl1"
                ],
                "sda1": [
                    "google-sl1-part1",
                    "scsi-0Google_PersistentDisk_sl1-part1"
                ],
                "sda14": [
                    "google-sl1-part14",
                    "scsi-0Google_PersistentDisk_sl1-part14"
                ],
                "sda15": [
                    "google-sl1-part15",
                    "scsi-0Google_PersistentDisk_sl1-part15"
                ]
            },
            "labels": {
                "sda1": [
                    "cloudimg-rootfs"
                ],
                "sda15": [
                    "UEFI"
                ]
            },
            "masters": {},
            "uuids": {
                "sda1": [
                    "c032eea3-a219-43e3-af6d-a1686f63e91f"
                ],
                "sda15": [
                    "945A-1D2E"
                ]
            }
        },
        "ansible_devices": {
            "loop0": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "none",
                "sectors": "113592",
                "sectorsize": "512",
                "size": "55.46 MB",
                "support_discard": "4096",
                "vendor": null,
                "virtual": 1
            },
            "loop1": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "none",
                "sectors": "311000",
                "sectorsize": "512",
                "size": "151.86 MB",
                "support_discard": "4096",
                "vendor": null,
                "virtual": 1
            },
            "loop2": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "none",
                "sectors": "143120",
                "sectorsize": "512",
                "size": "69.88 MB",
                "support_discard": "4096",
                "vendor": null,
                "virtual": 1
            },
            "loop3": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "none",
                "sectors": "63664",
                "sectorsize": "512",
                "size": "31.09 MB",
                "support_discard": "4096",
                "vendor": null,
                "virtual": 1
            },
            "loop4": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "none",
                "sectors": "66104",
                "sectorsize": "512",
                "size": "32.28 MB",
                "support_discard": "4096",
                "vendor": null,
                "virtual": 1
            },
            "loop5": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "none",
                "sectors": "385384",
                "sectorsize": "512",
                "size": "188.18 MB",
                "support_discard": "4096",
                "vendor": null,
                "virtual": 1
            },
            "loop6": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "none",
                "sectors": "0",
                "sectorsize": "512",
                "size": "0.00 Bytes",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "loop7": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "none",
                "sectors": "0",
                "sectorsize": "512",
                "size": "0.00 Bytes",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "md0": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "0",
                "sectorsize": "512",
                "size": "0.00 Bytes",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "sda": {
                "holders": [],
                "host": "Non-VGA unclassified device: Red Hat, Inc. Virtio SCSI",
                "links": {
                    "ids": [
                        "google-sl1",
                        "scsi-0Google_PersistentDisk_sl1"
                    ],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": "PersistentDisk",
                "partitions": {
                    "sda1": {
                        "holders": [],
                        "links": {
                            "ids": [
                                "google-sl1-part1",
                                "scsi-0Google_PersistentDisk_sl1-part1"
                            ],
                            "labels": [
                                "cloudimg-rootfs"
                            ],
                            "masters": [],
                            "uuids": [
                                "c032eea3-a219-43e3-af6d-a1686f63e91f"
                            ]
                        },
                        "sectors": "20744159",
                        "sectorsize": 512,
                        "size": "9.89 GB",
                        "start": "227328",
                        "uuid": "c032eea3-a219-43e3-af6d-a1686f63e91f"
                    },
                    "sda14": {
                        "holders": [],
                        "links": {
                            "ids": [
                                "google-sl1-part14",
                                "scsi-0Google_PersistentDisk_sl1-part14"
                            ],
                            "labels": [],
                            "masters": [],
                            "uuids": []
                        },
                        "sectors": "8192",
                        "sectorsize": 512,
                        "size": "4.00 MB",
                        "start": "2048",
                        "uuid": null
                    },
                    "sda15": {
                        "holders": [],
                        "links": {
                            "ids": [
                                "google-sl1-part15",
                                "scsi-0Google_PersistentDisk_sl1-part15"
                            ],
                            "labels": [
                                "UEFI"
                            ],
                            "masters": [],
                            "uuids": [
                                "945A-1D2E"
                            ]
                        },
                        "sectors": "217088",
                        "sectorsize": 512,
                        "size": "106.00 MB",
                        "start": "10240",
                        "uuid": "945A-1D2E"
                    }
                },
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "none",
                "sectors": "20971520",
                "sectorsize": "512",
                "size": "10.00 GB",
                "support_discard": "4096",
                "vendor": "Google",
                "virtual": 1
            }
        },
        "ansible_distribution": "Ubuntu",
        "ansible_distribution_file_parsed": true,
        "ansible_distribution_file_path": "/etc/os-release",
        "ansible_distribution_file_variety": "Debian",
        "ansible_distribution_major_version": "20",
        "ansible_distribution_release": "focal",
        "ansible_distribution_version": "20.04",
        "ansible_dns": {
            "nameservers": [
                "127.0.0.53"
            ],
            "options": {
                "edns0": true,
                "trust-ad": true
            },
            "search": [
                "us-central1-a.c.amazing-zephyr-304415.internal",
                "c.amazing-zephyr-304415.internal",
                "google.internal"
            ]
        },
        "ansible_domain": "us-central1-a.c.amazing-zephyr-304415.internal",
        "ansible_effective_group_id": 0,
        "ansible_effective_user_id": 0,
        "ansible_ens4": {
            "active": true,
            "device": "ens4",
            "features": {
                "esp_hw_offload": "off [fixed]",
                "esp_tx_csum_hw_offload": "off [fixed]",
                "fcoe_mtu": "off [fixed]",
                "generic_receive_offload": "on",
                "generic_segmentation_offload": "on",
                "highdma": "on [fixed]",
                "hw_tc_offload": "off [fixed]",
                "l2_fwd_offload": "off [fixed]",
                "large_receive_offload": "on",
                "loopback": "off [fixed]",
                "netns_local": "off [fixed]",
                "ntuple_filters": "off [fixed]",
                "receive_hashing": "off [fixed]",
                "rx_all": "off [fixed]",
                "rx_checksumming": "on [fixed]",
                "rx_fcs": "off [fixed]",
                "rx_gro_hw": "off [fixed]",
                "rx_udp_tunnel_port_offload": "off [fixed]",
                "rx_vlan_filter": "off [fixed]",
                "rx_vlan_offload": "off [fixed]",
                "rx_vlan_stag_filter": "off [fixed]",
                "rx_vlan_stag_hw_parse": "off [fixed]",
                "scatter_gather": "on",
                "tcp_segmentation_offload": "on",
                "tls_hw_record": "off [fixed]",
                "tls_hw_rx_offload": "off [fixed]",
                "tls_hw_tx_offload": "off [fixed]",
                "tx_checksum_fcoe_crc": "off [fixed]",
                "tx_checksum_ip_generic": "on",
                "tx_checksum_ipv4": "off [fixed]",
                "tx_checksum_ipv6": "off [fixed]",
                "tx_checksum_sctp": "off [fixed]",
                "tx_checksumming": "on",
                "tx_esp_segmentation": "off [fixed]",
                "tx_fcoe_segmentation": "off [fixed]",
                "tx_gre_csum_segmentation": "off [fixed]",
                "tx_gre_segmentation": "off [fixed]",
                "tx_gso_partial": "off [fixed]",
                "tx_gso_robust": "on [fixed]",
                "tx_ipxip4_segmentation": "off [fixed]",
                "tx_ipxip6_segmentation": "off [fixed]",
                "tx_lockless": "off [fixed]",
                "tx_nocache_copy": "off",
                "tx_scatter_gather": "on",
                "tx_scatter_gather_fraglist": "off [fixed]",
                "tx_sctp_segmentation": "off [fixed]",
                "tx_tcp6_segmentation": "on",
                "tx_tcp_ecn_segmentation": "off [fixed]",
                "tx_tcp_mangleid_segmentation": "off",
                "tx_tcp_segmentation": "on",
                "tx_udp_segmentation": "off [fixed]",
                "tx_udp_tnl_csum_segmentation": "off [fixed]",
                "tx_udp_tnl_segmentation": "off [fixed]",
                "tx_vlan_offload": "off [fixed]",
                "tx_vlan_stag_hw_insert": "off [fixed]",
                "vlan_challenged": "off [fixed]"
            },
            "hw_timestamp_filters": [],
            "ipv4": {
                "address": "10.128.0.24",
                "broadcast": "global",
                "netmask": "255.255.255.255",
                "network": "10.128.0.24"
            },
            "ipv6": [
                {
                    "address": "fe80::4001:aff:fe80:18",
                    "prefix": "64",
                    "scope": "link"
                }
            ],
            "macaddress": "42:01:0a:80:00:18",
            "module": "virtio_net",
            "mtu": 1460,
            "pciid": "virtio1",
            "promisc": false,
            "speed": -1,
            "timestamping": [
                "tx_software",
                "rx_software",
                "software"
            ],
            "type": "ether"
        },
        "ansible_env": {
            "HOME": "/root",
            "LANG": "C",
            "LC_ALL": "C",
            "LC_NUMERIC": "C",
            "LOGNAME": "root",
            "MAIL": "/var/mail/root",
            "PATH": "/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/snap/bin",
            "PWD": "/home/ansible",
            "SHELL": "/bin/bash",
            "SUDO_COMMAND": "/bin/sh -c echo BECOME-SUCCESS-qxaugrbafosrcyslxnriyymfegikboaq ; /usr/bin/python3 /home/ansible/.ansible/tmp/ansible-tmp-1615470386.3188732-126997672264691/AnsiballZ_setup.py",
            "SUDO_GID": "1005",
            "SUDO_UID": "1004",
            "SUDO_USER": "ansible",
            "TERM": "xterm",
            "USER": "root"
        },
        "ansible_fibre_channel_wwn": [],
        "ansible_fips": false,
        "ansible_form_factor": "Other",
        "ansible_fqdn": "sl1.us-central1-a.c.amazing-zephyr-304415.internal",
        "ansible_hostname": "sl1",
        "ansible_hostnqn": "nqn.2014-08.org.nvmexpress:uuid:b4706220-4be8-46c1-9a55-5839b2e76903",
        "ansible_interfaces": [
            "lo",
            "ens4"
        ],
        "ansible_is_chroot": false,
        "ansible_iscsi_iqn": "",
        "ansible_kernel": "5.4.0-1036-gcp",
        "ansible_kernel_version": "#39-Ubuntu SMP Thu Jan 14 18:41:17 UTC 2021",
        "ansible_lo": {
            "active": true,
            "device": "lo",
            "features": {
                "esp_hw_offload": "off [fixed]",
                "esp_tx_csum_hw_offload": "off [fixed]",
                "fcoe_mtu": "off [fixed]",
                "generic_receive_offload": "on",
                "generic_segmentation_offload": "on",
                "highdma": "on [fixed]",
                "hw_tc_offload": "off [fixed]",
                "l2_fwd_offload": "off [fixed]",
                "large_receive_offload": "off [fixed]",
                "loopback": "on [fixed]",
                "netns_local": "on [fixed]",
                "ntuple_filters": "off [fixed]",
                "receive_hashing": "off [fixed]",
                "rx_all": "off [fixed]",
                "rx_checksumming": "on [fixed]",
                "rx_fcs": "off [fixed]",
                "rx_gro_hw": "off [fixed]",
                "rx_udp_tunnel_port_offload": "off [fixed]",
                "rx_vlan_filter": "off [fixed]",
                "rx_vlan_offload": "off [fixed]",
                "rx_vlan_stag_filter": "off [fixed]",
                "rx_vlan_stag_hw_parse": "off [fixed]",
                "scatter_gather": "on",
                "tcp_segmentation_offload": "on",
                "tls_hw_record": "off [fixed]",
                "tls_hw_rx_offload": "off [fixed]",
                "tls_hw_tx_offload": "off [fixed]",
                "tx_checksum_fcoe_crc": "off [fixed]",
                "tx_checksum_ip_generic": "on [fixed]",
                "tx_checksum_ipv4": "off [fixed]",
                "tx_checksum_ipv6": "off [fixed]",
                "tx_checksum_sctp": "on [fixed]",
                "tx_checksumming": "on",
                "tx_esp_segmentation": "off [fixed]",
                "tx_fcoe_segmentation": "off [fixed]",
                "tx_gre_csum_segmentation": "off [fixed]",
                "tx_gre_segmentation": "off [fixed]",
                "tx_gso_partial": "off [fixed]",
                "tx_gso_robust": "off [fixed]",
                "tx_ipxip4_segmentation": "off [fixed]",
                "tx_ipxip6_segmentation": "off [fixed]",
                "tx_lockless": "on [fixed]",
                "tx_nocache_copy": "off [fixed]",
                "tx_scatter_gather": "on [fixed]",
                "tx_scatter_gather_fraglist": "on [fixed]",
                "tx_sctp_segmentation": "on",
                "tx_tcp6_segmentation": "on",
                "tx_tcp_ecn_segmentation": "on",
                "tx_tcp_mangleid_segmentation": "on",
                "tx_tcp_segmentation": "on",
                "tx_udp_segmentation": "off [fixed]",
                "tx_udp_tnl_csum_segmentation": "off [fixed]",
                "tx_udp_tnl_segmentation": "off [fixed]",
                "tx_vlan_offload": "off [fixed]",
                "tx_vlan_stag_hw_insert": "off [fixed]",
                "vlan_challenged": "on [fixed]"
            },
            "hw_timestamp_filters": [],
            "ipv4": {
                "address": "127.0.0.1",
                "broadcast": "host",
                "netmask": "255.0.0.0",
                "network": "127.0.0.0"
            },
            "ipv6": [
                {
                    "address": "::1",
                    "prefix": "128",
                    "scope": "host"
                }
            ],
            "mtu": 65536,
            "promisc": false,
            "timestamping": [
                "tx_software",
                "rx_software",
                "software"
            ],
            "type": "loopback"
        },
        "ansible_local": {},
        "ansible_lsb": {
            "codename": "focal",
            "description": "Ubuntu 20.04.2 LTS",
            "id": "Ubuntu",
            "major_release": "20",
            "release": "20.04"
        },
        "ansible_lvm": {
            "lvs": {},
            "pvs": {},
            "vgs": {}
        },
        "ansible_machine": "x86_64",
        "ansible_machine_id": "16b9a90f1fef6b0425c0748c2bcc601d",
        "ansible_memfree_mb": 2648,
        "ansible_memory_mb": {
            "nocache": {
                "free": 3620,
                "used": 315
            },
            "real": {
                "free": 2648,
                "total": 3935,
                "used": 1287
            },
            "swap": {
                "cached": 0,
                "free": 0,
                "total": 0,
                "used": 0
            }
        },
        "ansible_memtotal_mb": 3935,
        "ansible_mounts": [
            {
                "block_available": 2019105,
                "block_size": 4096,
                "block_total": 2495808,
                "block_used": 476703,
                "device": "/dev/root",
                "fstype": "ext4",
                "inode_available": 1217443,
                "inode_total": 1290240,
                "inode_used": 72797,
                "mount": "/",
                "options": "rw,relatime",
                "size_available": 8270254080,
                "size_total": 10222829568,
                "uuid": "c032eea3-a219-43e3-af6d-a1686f63e91f"
            },
            {
                "block_available": 0,
                "block_size": 131072,
                "block_total": 444,
                "block_used": 444,
                "device": "/dev/loop0",
                "fstype": "squashfs",
                "inode_available": 0,
                "inode_total": 10817,
                "inode_used": 10817,
                "mount": "/snap/core18/1988",
                "options": "ro,nodev,relatime",
                "size_available": 0,
                "size_total": 58195968,
                "uuid": "N/A"
            },
            {
                "block_available": 0,
                "block_size": 131072,
                "block_total": 1215,
                "block_used": 1215,
                "device": "/dev/loop1",
                "fstype": "squashfs",
                "inode_available": 0,
                "inode_total": 37243,
                "inode_used": 37243,
                "mount": "/snap/google-cloud-sdk/168",
                "options": "ro,nodev,relatime",
                "size_available": 0,
                "size_total": 159252480,
                "uuid": "N/A"
            },
            {
                "block_available": 0,
                "block_size": 131072,
                "block_total": 560,
                "block_used": 560,
                "device": "/dev/loop2",
                "fstype": "squashfs",
                "inode_available": 0,
                "inode_total": 1578,
                "inode_used": 1578,
                "mount": "/snap/lxd/19188",
                "options": "ro,nodev,relatime",
                "size_available": 0,
                "size_total": 73400320,
                "uuid": "N/A"
            },
            {
                "block_available": 0,
                "block_size": 131072,
                "block_total": 249,
                "block_used": 249,
                "device": "/dev/loop3",
                "fstype": "squashfs",
                "inode_available": 0,
                "inode_total": 470,
                "inode_used": 470,
                "mount": "/snap/snapd/11036",
                "options": "ro,nodev,relatime",
                "size_available": 0,
                "size_total": 32636928,
                "uuid": "N/A"
            },
            {
                "block_available": 205804,
                "block_size": 512,
                "block_total": 213716,
                "block_used": 7912,
                "device": "/dev/sda15",
                "fstype": "vfat",
                "inode_available": 0,
                "inode_total": 0,
                "inode_used": 0,
                "mount": "/boot/efi",
                "options": "rw,relatime,fmask=0022,dmask=0022,codepage=437,iocharset=iso8859-1,shortname=mixed,errors=remount-ro",
                "size_available": 105371648,
                "size_total": 109422592,
                "uuid": "945A-1D2E"
            },
            {
                "block_available": 0,
                "block_size": 131072,
                "block_total": 259,
                "block_used": 259,
                "device": "/dev/loop4",
                "fstype": "squashfs",
                "inode_available": 0,
                "inode_total": 474,
                "inode_used": 474,
                "mount": "/snap/snapd/11107",
                "options": "ro,nodev,relatime",
                "size_available": 0,
                "size_total": 33947648,
                "uuid": "N/A"
            },
            {
                "block_available": 0,
                "block_size": 131072,
                "block_total": 1506,
                "block_used": 1506,
                "device": "/dev/loop5",
                "fstype": "squashfs",
                "inode_available": 0,
                "inode_total": 37831,
                "inode_used": 37831,
                "mount": "/snap/google-cloud-sdk/172",
                "options": "ro,nodev,relatime",
                "size_available": 0,
                "size_total": 197394432,
                "uuid": "N/A"
            }
        ],
        "ansible_nodename": "sl1",
        "ansible_os_family": "Debian",
        "ansible_pkg_mgr": "apt",
        "ansible_proc_cmdline": {
            "BOOT_IMAGE": "/boot/vmlinuz-5.4.0-1036-gcp",
            "console": "ttyS0",
            "panic": "-1",
            "ro": true,
            "root": "PARTUUID=6a40708a-dbcd-4e45-8469-8ba0fce0f2fa"
        },
        "ansible_processor": [
            "0",
            "AuthenticAMD",
            "AMD EPYC 7B12",
            "1",
            "AuthenticAMD",
            "AMD EPYC 7B12"
        ],
        "ansible_processor_cores": 1,
        "ansible_processor_count": 1,
        "ansible_processor_threads_per_core": 2,
        "ansible_processor_vcpus": 2,
        "ansible_product_name": "Google Compute Engine",
        "ansible_product_serial": "GoogleCloud-16B9A90F1FEF6B0425C0748C2BCC601D",
        "ansible_product_uuid": "16b9a90f-1fef-6b04-25c0-748c2bcc601d",
        "ansible_product_version": "NA",
        "ansible_python": {
            "executable": "/usr/bin/python3",
            "has_sslcontext": true,
            "type": "cpython",
            "version": {
                "major": 3,
                "micro": 5,
                "minor": 8,
                "releaselevel": "final",
                "serial": 0
            },
            "version_info": [
                3,
                8,
                5,
                "final",
                0
            ]
        },
        "ansible_python_version": "3.8.5",
        "ansible_real_group_id": 0,
        "ansible_real_user_id": 0,
        "ansible_selinux": {
            "status": "Missing selinux Python library"
        },
        "ansible_selinux_python_present": false,
        "ansible_service_mgr": "systemd",
        "ansible_ssh_host_key_dsa_public": "AAAAB3NzaC1kc3MAAACBALbHLjMHXnQWZf24USk67OtSljWJY8A3iB+t1C+gC4qt7bUDr4SO5S71iZj9vMoT+QZhmD1odpD55OMk02rf8UhwZRbGjXW5CyZ1qNdXWhw10q1w1b0DFTWIfjPR6/8X2NK1NZLgCrV4WajxLvFnAqqDBjrckEoI3i/1LkD27JrXAAAAFQCgTqZQr6GkQWydRkxXtO8y8XAKOwAAAIAB3WgLjON5cKH5W7bKI/F17LZe0h+ydm6KJXeJPFIW/94F+h3xDJIvi1IB295k3UxuxqsSbaIdR1FN001DchvjDaSe/0x0glkmdB3k4Mw6ACqK5nj7lH3IPy95LuyL1xRiDvz/Mo42WEp1QeDZSdn7P3X1IDqFkeMcHcZRt0rOAAAAAIEArLSsARbjknhR+MWdVrr7ItHLnYowwaWeFHgWjGw6JSx/0aQIj313DikZm9eygC3fBexJzYAJzqaAYeruFCe2OEEl/iLuzaakGLaDNTx26Y9qfOtUUK6c3pVzMZYYRltSNCzsCD4YufXtZkXWqQq38HhH72wk2jjmjmDH+pLFqBk=",
        "ansible_ssh_host_key_ecdsa_public": "AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBCMoLpRPjaVeUmLFVCAMxXmcFpcn2yGPmllOKvh5CZWeRpqWiZ6ZZi5sjljN2ObLZr1T5A8fjCNpl1298jLqjlo=",
        "ansible_ssh_host_key_ed25519_public": "AAAAC3NzaC1lZDI1NTE5AAAAIA1lwHL2N5arAurk6ydVH8D7wWu28nWkgQbwRZH21gK/",
        "ansible_ssh_host_key_rsa_public": "AAAAB3NzaC1yc2EAAAADAQABAAABgQDBhCciPkNBieWSf4s95tCjQKxEXUyi9txxm1w/6AM2RNC7/EnK/qAHJeR242BQ2D81Qem1k5coHCTyg2cj0mIUsqFuW5xfvDcdRmKd9Qp20WaYbx4I4tQjPXal4bLskTTGSRdPMGK8YdR7NttNAewDo0hwvBdtKrYq91pWUegyWO5mkVIKaGZ/tgaedAS67R8hY5qtzsmuzrHBm8XzZhEB3lfrG8FRDI2La1nYsTL6ENshlUaUMar+yham9hZJQ4S/rXP0KrRaDLIByF+4lf6NC3D1wEUNHKwagKyq5ZMKB4NS3V/XN9y9nx3E7J2vHuuBrrTgQJDvSoy3ui5kW8PSLz44HhVvrtvpJ77uE9jxfHNt5icUgF5LcdYZ2uPv3B8fWL3zsHpHIGrA0x/JiERiaPsPV7uE2fFsDrq8IR0bTpLZXZCSVtdZy9c4NTptgH8fWV7DNWB+vfsThCFCZ1H9FpdQAuYFpUe87XmVhpHxl37/Tt2ky7CYV9cmZckSB2k=",
        "ansible_swapfree_mb": 0,
        "ansible_swaptotal_mb": 0,
        "ansible_system": "Linux",
        "ansible_system_capabilities": [],
        "ansible_system_capabilities_enforced": "False",
        "ansible_system_vendor": "Google",
        "ansible_uptime_seconds": 5687,
        "ansible_user_dir": "/root",
        "ansible_user_gecos": "root",
        "ansible_user_gid": 0,
        "ansible_user_id": "root",
        "ansible_user_shell": "/bin/bash",
        "ansible_user_uid": 0,
        "ansible_userspace_architecture": "x86_64",
        "ansible_userspace_bits": "64",
        "ansible_virtualization_role": "guest",
        "ansible_virtualization_type": "kvm",
        "discovered_interpreter_python": "/usr/bin/python3",
        "gather_subset": [
            "all"
        ],
        "module_setup": true
    },
    "changed": false
}
