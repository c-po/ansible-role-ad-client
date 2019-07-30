# Ansible role ``

Ansible role for installing and joining a Linux (Ubuntu/Debian) Linux machine to
an Active Directory environment.

## Dependencies

* https://github.com/bertvv/ansible-role-samba.git

## Role Variables

| Variable                | Default        | Comments (type)                                  |
| :---                    | :---           | :---                                             |
| `tftp_root_directory`   | /tftpboot      | The path to the root directory served by tftp.   |

## License

BSD

## Author Information

Christian Poessinger (christian@poessinger.com)

## Contibutions

WELCOME !

## Example Playbook

```
$ cat ad_clients.yml
- hosts: ad-clients
  remote_user: root
  become_method: sudo
  become_user: root
  roles:
   - ansible-role-samba
   - ansible-active-directory-client
```
