correcthorse.common
=========

This role contains some basic common tasks/handlers. This includes some tasks for installing the EPEL and IUS repositories as well as some handlers for systemd and firewalld. You can optionally install the correcthorse packagecloud repo. This may be enabled by other roles that depend on it.

Role Variables
--------------
| Variable                              | Default                       | Notes                                         |
| :---                                  | :---                          | :---                                          |
| common_install_epel			| true				| install epel repo				|
| common_install_remi			| false				| install Remi's repo - only safe repo enabled	|
| common_install_webtatic		| false				| install webtatic repo				|
| common_install_correcthorse           | false                         | install correcthorse packagecloud repo	|
| common_epel_exclude			| ''				| exclude epel pkgs - useful if using upstream repos |
| common_development_tools		| false				| yum groupinstall "Development Tools"	       |
| common_extra_packages			| []				| add extra packages to install		       |

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: correcthorse.common }

License
-------

MIT

Author Information
------------------

* [Joshua Rusch](https://correct.horse/)
