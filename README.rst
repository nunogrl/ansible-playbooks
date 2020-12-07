README
######


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


