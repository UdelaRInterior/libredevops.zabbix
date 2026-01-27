# community.zabbix.zabbix_crud role

# Overview

This role performs several CRUD actions vía Zabbix API. Takes most common modules, wrap in to variables and configure it.

Supported modules:
- [zabbix_mediatype](https://docs.ansible.com/ansible/latest/collections/community/zabbix/zabbix_mediatype_module.html#ansible-collections-community-zabbix-zabbix-mediatype-module)
- [zabbix_usergroup](https://docs.ansible.com/ansible/latest/collections/community/zabbix/zabbix_usergroup_module.html#ansible-collections-community-zabbix-zabbix-usergroup-module)
- [zabbix_user_role](https://docs.ansible.com/ansible/latest/collections/community/zabbix/zabbix_user_role_module.html#ansible-collections-community-zabbix-zabbix-user-role-module)
- [zabbix_user](https://docs.ansible.com/ansible/latest/collections/community/zabbix/zabbix_user_module.html#ansible-collections-community-zabbix-zabbix-user-module)
- [zabbix_group](https://docs.ansible.com/ansible/latest/collections/community/zabbix/zabbix_group_module.html#ansible-collections-community-zabbix-zabbix-group-module)
- [zabbix_template](https://docs.ansible.com/ansible/latest/collections/community/zabbix/zabbix_template_module.html#ansible-collections-community-zabbix-zabbix-template-module)
- [zabbix_host](https://docs.ansible.com/ansible/latest/collections/community/zabbix/zabbix_host_module.html#ansible-collections-community-zabbix-zabbix-host-module)
- [zabbix_script](https://docs.ansible.com/ansible/latest/collections/community/zabbix/zabbix_script_module.html#ansible-collections-community-zabbix-zabbix-script-module)
- [zabbix_action](https://docs.ansible.com/ansible/latest/collections/community/zabbix/zabbix_action_module.html#ansible-collections-community-zabbix-zabbix-action-module)

# Requirements

## Ansible 2.10 and higher

# Role Variables

## Main variables

See `defaults/main.yml` for more details.

## Zabbix API connection variables

`zabbix_api_server_port`: connection httpapi port, `80` by default.
`zabbix_api_use_ssl`: use SSL for httpapi connection, `false` by default.
`zabbix_api_validate_certs`: validate certs for httpapi connection, `false` by default.
`zabbix_api_zabbix_url_path`: path to web directory or alias, `zabbix` by default.
`zabbix_api_login_user`: Username of user which has API access.
`zabbix_api_login_pass`: Password for the user which has API access.
`zabbix_api_http_user`: The http user to access zabbix url with Basic Auth (if your Zabbix is behind a proxy with HTTP Basic Auth).
`zabbix_api_http_password`: The http password to access zabbix url with Basic Auth (if your Zabbix is behind a proxy with HTTP Basic Auth).
`zabbix_api_auth_key`: API token for access. Not set by default.

# Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
  - hosts: zabbix-server
    roles:
      - role: community.zabbix.zabbix_crud
```

# License

GNU General Public License v3.0 or later

See LICENCE to see the full text.

# Author Information

Please send suggestion or pull requests to make this role better. Also let us know if you encounter any issues installing or using this role.

Github: https://github.com/ansible-collections/community.zabbix

