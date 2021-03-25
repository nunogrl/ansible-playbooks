README
######

Pre-flight
==========

.. code-block:: TEXT

    git submodule update --init --recursive


Simplified Schematic
====================

.. code-block:: TEXT

       Dev        Prod
      .---.      .---.
     /   /|     /   /|          .-,(  ),-.
    .---. |    .---. |       .-(          )-.
    |   |-'--->|   | '      (    Dropbox     )
    |   |/     |   |/        '-(          ).-'
    '---'      '---'             '-.( ).-'

         Test
        .---.                   .-,(  ),-.
       /   /|                .-(          )-.
      .---. |               (     Pcloud     )
      |   | '                '-(          ).-'
      |   |/                     '-.( ).-'
      '---'


Dev
  A server with a VPN connection to perform some evaluation prior to make the
  changes on the production server.

Prod
  Public facing server.

Test
  A server to run some playbooks and test some configurations.

Dropbox / Pcloud
  Intermediate space to store some media, such backups or assets


.. code-block:: TEXT

    ├── hosts
    ├── host_vars
    ├── playbooks
    │   ├── roles -> ../roles
    │   └── (...)
    └── roles
        └── (...)

Workflow
========

The playbooks live at `playbooks/` and roles live at `roles/`

Calling a playbook should be as easy as:


.. code-block:: TEXT


    ansible-playbook playbooks/playbook.yaml


Testing Locally
---------------

There's a Vagrant file that can be used to test an incoming playbook


Host Configuration
==================

bootstrap
---------

The first connection to the server.

- Connects as root with a given password
- Performs the hardening.
- Configures MTA

security-firewall.yaml
----------------------

- Configure users
- Setup dropbox connection
- Updates Firewall

Playbooks
=========

datadog-monitoring.yaml
dev-bc.yaml
docs-bc.yaml
dropbox.yaml
git-server.yaml
import-key.yaml
keyring
moodledb.yaml
moodle.yaml
nci-ansible-ui.yml
password-store.yaml
shaarli.yaml
