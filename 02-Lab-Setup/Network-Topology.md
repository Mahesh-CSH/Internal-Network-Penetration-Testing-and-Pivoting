# Network Topology

The assessment environment was built using VMware virtual machines
with separate NAT and isolated internal networking.

## Architecture

                     Kali Linux
                  192.168.88.129
                         |
                       NAT
                         |
                  Windows 10 Client
                  192.168.88.136
                   10.10.10.128
                         |
                    Internal LAN
                    10.10.10.0/24
                         |
                         |
                 Metasploitable 2
                   10.10.10.130
