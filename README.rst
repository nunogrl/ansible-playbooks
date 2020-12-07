README
######

.. code-block:: TEXT

    ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░
    ░░░░░┌───────┐░░░░░░░░░░░░░░░░░░░
    ░░░░░│░░░░░░░│░░░░░░░░░░░░░░░░░░░
    ░░░░░│░Test░░│░░░░░░░░░░░░░░░░░░░
    ░░░░░│░░░░░░░│░░░░░░░░░░░░░░░░░░░
    ░░░░░└───────┘░░░░░░░░░░░░░░░░░░░
    ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░
    ░░░░░╔═══════╗░░░░░░░╔═══════╗░░░
    ░░░░░║░░░░░░░║░░░░░░░║░░░░░░░║░░░
    ░░░░░║░░Dev░░║══════>║░Prod░░║░░░
    ░░░░░║░░░░░░░║░░░░░░░║░░░░░░░║░░░
    ░░░░░╚═══════╝░░░░░░░╚═══════╝░░░
    ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░


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
===============

There's a Vagrant file that can be used to test an incoming playbook


Host Configuration
==================

bootstrap
---------

The first connection to the server.

Connects as root with a given password and performs the hardening.


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
roles
shaarli.yaml
vars
