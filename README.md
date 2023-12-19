ansible.pkg_mirror
===

[![](https://img.shields.io/github/license/adfinis/ansible-role-pkg_mirror.svg?style=flat-square)](https://github.com/adfinis/ansible-role-pkg_mirror/blob/master/LICENSE)
[![image](https://img.shields.io/github/actions/workflow/status/adfinis/ansible-role-pkg_mirror/ansible-ci.yml?style=flat-square)](https://github.com/adfinis/ansible-role-pkg_mirror/actions)
[![](https://img.shields.io/badge/galaxy-adfinis.pkg_mirror-660198.svg?style=flat-square)](https://galaxy.ansible.com/adfinis/pkg_mirror)

Manage system package source


## Requirements

-


## Role Variables

```yaml
pkg_mirror_gpgkey_url: '<gpg url>'
pkg_mirror_sources_file: /etc/apt/sources.list.d/<filename>.list
pkg_mirror_url_list_debian:
 - 'deb <repo url>/{{ ansible_distribution | lower }}/ {{ ansible_distribution_release }} main'

pkg_mirror_url_list_redhat:
 - name: '<repo name>'
   description: '<repo description>'
   baseurl: '<repo url>'
   gpgcheck: yes
   gpgkey: '<gpg url>'
   username: '<basic auth user>'
   password: '<basic auth pass>'

pkg_mirror_url_list_suse:
 - name: '<repo name>'
   description: '<repo description>'
   repo: '<repo url>'
```



## Dependencies

-


## Example Playbook

Including an example of how to use your role (for instance, with variables
passed in as parameters) is always nice for users too:

```yaml
  - hosts: servers
    roles:
       - { role: adfinis.pkg_mirror }
```

## License

[GPL-3.0](https://github.com/adfinis/ansible-role-pkg_mirror/blob/master/LICENSE)


## Author Information

pkg_mirror role was written by:

* Adfinis AG | [Website](https://www.adfinis.com/) | [Twitter](https://twitter.com/adfinis) | [GitHub](https://github.com/adfinis)

