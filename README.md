Nginx
=========
Designed to only install nginx and give you full controll over the configuration.

Only tested on Ubuntu 18.04.

Role Variables
--------------

    nginx_config (Default False)

Will give the ability to set the nginx config using a config placed in the templates/ directory.

    nginx_delete_default_virtual_host (Default True)

Will delete the default virtual host if set to true. Set to false to keep it.

    nginx_verify_virtual_host_configs (Default True)

Will verify the virtual host configs. Set to false if this is not required.

Virtual Hosts
-------------

This role will loop over any virtual hosts placed inside of the templates/nginx/ directory.

Example Playbook
----------------

    - hosts: servers
      roles:
         - entanet-devops.nginx