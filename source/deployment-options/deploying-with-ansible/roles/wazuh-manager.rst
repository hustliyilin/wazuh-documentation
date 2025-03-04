.. Copyright (C) 2022 Wazuh, Inc.

.. _ansible-wazuh-manager:

Wazuh Manager
-------------

This role will install and configure the Wazuh manager and Wazuh API, there are several variables you can use to customize the installation or configuration, for example:

- **wazuh_manager_config_overlay:** enables configuring the manager by overlaying sections of configs on top of defaults (default: ``true``)
- **wazuh_manager_json_output:** enabling or not JSON output (default: ``yes``)
- **wazuh_manager_email_notification:** enabling email notifications (default: ``no``)
- **wazuh_manager_mailto:** email notifications recipients (array, defaults: ``admin@example.net``)
- **wazuh_manager_email_smtp_server:** SMTP server to be used by email notifications ( defaults: ``localhost``)
- **wazuh_manager_email_from:** email notification sender ( defaults: ``wazuh@example.com``)

By creating a YAML file ``wazuh-manager.yml`` you can specify the usage of this role:

.. code-block:: yaml

  - hosts: wazuh-manager
    roles:
      - ansible-wazuh-manager
      - ansible-role-filebeat

Setting the variables in a separate YAML file is recommended when configuring the installation. For this example we used: ``vars-production.yml``:

.. code-block:: yaml

  filebeat_output_elasticsearch_hosts: '10.1.1.11:9200'

  wazuh_manager_fqdn: "wazuh-manager"

  wazuh_manager_config_overlay: true
  wazuh_manager_json_output: 'yes'
  wazuh_manager_alerts_log: 'yes'
  wazuh_manager_logall: 'no'
  wazuh_manager_log_format: 'plain'

  wazuh_manager_connection:
    - type: 'secure'
      port: '1514'
      protocol: 'tcp'

  wazuh_manager_authd:
    enable: true
    port: 1515
    use_source_ip: 'no'
    force:
      - enabled: 'yes'
        disconnected_time:
          enabled: yes
          value: '1h'
        after_registration_time: '1h'
        key_mismatch: 'yes'
    purge: 'no'
    use_password: 'no'
    ssl_agent_ca: null
    ssl_verify_host: 'no'
    ssl_manager_cert: null
    ssl_manager_key: null
    ssl_auto_negotiate: 'no'

You can configure **Wazuh API** user credentials by including them in ``htpasswd`` format in the file ``ansible-wazuh-manager/vars/wazuh_api_creds.yml`` located on your Ansible control server:

.. code-block:: yaml

  # Be sure you encrypt this file with ansible-vault
  wazuh_api_user:
  - foo:$apr1$/axqZYWQ$Xo/nz/IG3PdwV82EnfYKh/
  - bar:$apr1$hXE97ag.$8m0koHByattiGKUKPUgcZ1

Also, you can configure **agentless** host credentials via the file: ``ansible-wazuh-manager/vars/agentless_creds.yml``, set many as you need:

.. code-block:: yaml

  # Be sure you encrypt this file with ansible-vault.
  agentless_creds:
   - type: ssh_integrity_check_linux
     frequency: 3600
     host: root@example1.net
     state: periodic
     arguments: '/bin /etc/ /sbin'
     passwd: qwerty
   - type: ssh_integrity_check_bsd
     frequency: 3600
     host: user@example2.net
     state: periodic
     arguments: '/bin /etc/ /sbin'
     passwd: qwerty

And the ``authd`` service password could be set in the file ``ansible-wazuh-manager/vars/authd_pass.yml``:

.. code-block:: yaml

  # Be sure you encrypt this file with ansible-vault
  authd_pass: foobar

.. warning:: We recommend the use of `Ansible Vault <http://docs.ansible.com/ansible/playbooks_vault.html>`_ to protect Wazuh API and agentless credentials.

Next, run the playbook:

.. code-block:: console

  $ ansible-playbook wazuh-manager.yml -e@vars-production.yml

The example above will install the Wazuh manager and Filebeat, Filebeat will be configured to forward data to ``10.1.1.11:9200`` as Elasticsearch node, also it will set various ``agentless`` hosts configurations including their credentials, the Wazuh API and the ``authd`` will be configured as well.

Please review the :ref:`references <wazuh_ansible_reference_manager>` section to see all variables available for this role.
