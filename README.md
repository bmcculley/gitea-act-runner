Role Name
=========

An Ansible role that will install and configure Docker, Gitea, Act runner, and Nginx on an Ubuntu server.

**Note:** This runs Docker as root.

Requirements
------------

Everything is covered by Ansible itself.

Role Variables
--------------

```yaml
gitea_version: "1.22"
gitea_schema: https
web_server_port: 80
gitea_backend_port: 3000
gitea_ssh_port: 22
web_server_name: git.example.com
web_server_config_name: gitexamplecom
nginx_version: 1.22.0-1ubuntu3
gitea_admin_username: user0
gitea_admin_password: password
gitea_admin_email: admin@example.com
gitea_act_version: "0.2.10"
gitea_act_runner_name: act-runner
```

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      become: true
      roles:
        - role: gitea-act-runner
          vars:
            web_server_name: demo.example.com
            web_server_config_name: demoexample


License
-------

BSD

Author Information
------------------

Check out the accompanying [blog post on hakk.dev](https://hakk.dev/blog/posts/streamlining-deployment-installing-docker-gitea-act-runner-nginx-ubuntu/)
