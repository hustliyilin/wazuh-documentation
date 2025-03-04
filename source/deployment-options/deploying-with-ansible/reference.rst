.. Copyright (C) 2022 Wazuh, Inc.

.. meta::
  :description: Ansible is an open source platform designed for automating tasks. Learn more about the variable references in this section of the Wazuh documentation.
  
.. _wazuh_ansible_reference:

Variables references
--------------------

.. _wazuh_ansible_reference_elasticsearch:

Elasticsearch / Opendistro
==========================

**elasticsearch_cluster_name**

  Name of the Elasticsearch cluster

  *Default wazuh*

**elasticsearch_node_name**

  Name of the Elasticsearch node

  *Default node-1*

**elasticsearch_http_port**

  ElasticSearch listening port

  *Default 9200*

**elasticsearch_network_host**

  ElasticSearch, listening IP address

  *Default 127.0.0.1*

**elasticsearch_jvm_xms**

  JVM heap size

  *Default null*

**elastic_stack_version**

  Version of Elasticsearch to install

  *Default |ELASTICSEARCH_LATEST_ANSIBLE|*

**elasticsearch_shards**

  Set number of shards for indices

  *Default 5*

**elasticsearch_replicas**

  Set number of shards for indices

  *Default 1*

**elasticsearch_install_java**

  When it's present will install Oracle Java.

  *Default yes*

.. _wazuh_ansible_reference_kibana:

Kibana
======

**elasticsearch_http_port**

  Elasticsearch node port.

  *Default 9200*

**elasticsearch_network_host**

  IP address or hostname of Elasticsearch node.

  *Default 127.0.0.1*

**kibana_server_host**

  Listening IP address of Kibana.

  *Default 0.0.0.0*

**kibana_server_port**

  Listening port of Kibana.

  *Default 5601*

**elastic_stack_version**

  Version of Kibana to install

  *Default |ELASTICSEARCH_LATEST_ANSIBLE|*

**wazuh_version**

  Wazuh APP compatible version to install

  *Default |WAZUH_LATEST_ANSIBLE|*

**elasticsearch_network_host**

  IP address or hostname of Elasticsearch node.

  *Default 127.0.0.1*

**elasticsearch_http_port**

  Port of Elasticsearch node.

  *Default 9200*

**elasticsearch_shards**

  Set number of shards for indices

  *Default 5*

**elasticsearch_replicas**

  Set number of shards for indices

  *Default 1*

.. _wazuh_ansible_reference_filebeat:

Filebeat
========

**filebeat_version:**

  Filebeat version to install.

  *Default |ELASTICSEARCH_LATEST_ANSIBLE|*

**filebeat_create_config:**

  Generate or not Filebeat config.

  *Default true*

**filebeat_output_elasticsearch_enabled:**

  Send output to Elasticsearch node(s).

  *Default false*

**filebeat_output_elasticsearch_hosts:**

  Elasticsearch node(s) to send output.

  *Example:* ::

    filebeat_output_elasticsearch_hosts:
    - "localhost:9200"
    - "10.1.1.10:9200"

**filebeat_ssl_dir:**

  Set the folder containing SSL certs.

  *Default /etc/pki/root*


**filebeat_ssl_key_file:**

  Set certificate key filename.

  *Default null*

.. _wazuh_ansible_reference_manager:

Wazuh Manager
=============

**wazuh_manager_fqdn:**

  Set Wazuh Manager fqdn hostname.

  *Default wazuh-manager*

**wazuh_manager_config_overlay**

  Indicates if role should perform a `hash_behaviour=merge` at role runtime, similar to role-distributed ansible.cfg.
  This provides support for a partially defined *wazuh_manager_config* while also moving on from `deprecated hash_behaviour <https://docs.ansible.com/ansible/latest/reference_appendices/config.html#default-hash-behaviour>`_

  *Default true*

**wazuh_manager_json_output**

  Configures the :ref:`jsonout_output<reference_ossec_global>` section from ``ossec.conf``. This is a string, not a bool.

  *Default yes*

**wazuh_manager_alerts_log**

  Configures the :ref:`alerts_log<reference_ossec_global>` section from ``ossec.conf``. This is a string, not a bool.

  *Default yes*

**wazuh_manager_logall**

  Configures the :ref:`logall<reference_ossec_global>` section from ``ossec.conf``. This is a string, not a bool.

  *Default yes*

**wazuh_manager_email_notification**

  Configures the :ref:`email_notification<reference_ossec_global>` section from ``ossec.conf``. This is a string, not a bool.

  *Default yes*

**wazuh_manager_mailto**

  Configures the :ref:`email_to<reference_ossec_global>` items from ``ossec.conf``.

  *Default ['admin@example.net']*


**wazuh_manager_email_smtp_server**

  Configures the :ref:`smtp_server<reference_ossec_global>` section from ``ossec.conf``.

  *Default smtp.example.wazuh.com*


**wazuh_manager_email_from**

  Configures the :ref:`email_from<reference_ossec_global>` section from ``ossec.conf``.

  *Default wazuh@example.wazuh.com*


**wazuh_manager_email_maxperhour**

  Configures the :ref:`email_maxperhour<reference_ossec_global>` section from ``ossec.conf``.

  *Default 12*

**wazuh_manager_email_queue_size**

  Configures the :ref:`queue_size<reference_ossec_remote>` section from ``ossec.conf``.

  *Default 131072*

**wazuh_manager_email_log_source**

  Configures the :ref:`email_log_source<reference_ossec_global>` section from ``ossec.conf``.

  *Default alerts.log*

**wazuh_manager_globals**

  Configures the :ref:`white_list<reference_ossec_global>` section from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_manager_globals:
      - '127.0.0.1'
      - '^localhost.localdomain$'
      - '127.0.0.53'


**wazuh_manager_log_level**

  Configures the :ref:`log_alert_level<reference_ossec_alerts>` section from ``ossec.conf``.

  *Default 3*


**wazuh_manager_email_level**

  Configures the :ref:`email_alert_level<reference_ossec_alerts>` section from ``ossec.conf``.

  *Default 12*


**wazuh_manager_log_format**

  Configures :ref:`log_format<reference_ossec_logging>` inside logging section from ``ossec.conf``.

  *Default plain*


**wazuh_manager_extra_emails**

  Configures one or more :ref:`email_alerts<reference_ossec_email_alerts>` sections from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_manager_extra_emails:
      - enable: false
        mail_to: 'recipient@example.wazuh.com'
        format: full
        level: 7
        event_location: null
        group: null
        do_not_delay: false
        do_not_group: false
        rule_id: null


**wazuh_manager_connection**

  Configures one or more :ref:`remote<reference_ossec_remote>` sections from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_manager_connection:
      - type: 'secure'
        port: '1514'
        protocol: 'tcp'
        queue_size: 131072

**wazuh_manager_reports**

  Configures one or more :ref:`reports<reference_ossec_reports>` sections from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_manager_reports:
      - enable: false
        category: 'syscheck'
        title: 'Daily report: File changes'
        email_to: 'recipient@example.wazuh.com'
        location: null
        group: null
        rule: null
        level: null
        srcip: null
        user: null
        showlogs: null

**wazuh_manager_rootcheck**

  Configures the :ref:`rootcheck<reference_ossec_rootcheck>` section from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_manager_rootcheck:
      frequency: 43200

**wazuh_manager_openscap**

  Configures the :ref:`wodle<wodle_openscap>` item named ``open-scap`` from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_manager_openscap:
      disable: 'yes'
      timeout: 1800
      interval: '1d'
      scan_on_start: 'yes'


**wazuh_manager_ciscat**

  Configures the :ref:`wodle<wodle_ciscat>` item named ``cis-cat`` from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

     wazuh_manager_ciscat:
       disable: 'yes'
       install_java: 'yes'
       timeout: 1800
       interval: '1d'
       scan_on_start: 'yes'
       java_path: '/usr/lib/jvm/java-1.8.0-openjdk-amd64/jre/bin'
       ciscat_path: 'wodles/ciscat'

**wazuh_manager_osquery**

  Configures the :ref:`wodle<wodle-osquery>` item named ``osquery`` from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_manager_osquery:
      disable: 'yes'
      run_daemon: 'yes'
      log_path: '/var/log/osquery/osqueryd.results.log'
      config_path: '/etc/osquery/osquery.conf'
      ad_labels: 'yes'

**wazuh_manager_syscollector**

  Configures the :ref:`wodle<wodle-syscollector>` item named ``syscollector`` from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_manager_syscollector:
      disable: 'no'
      interval: '1h'
      scan_on_start: 'yes'
      hardware: 'yes'
      os: 'yes'
      network: 'yes'
      packages: 'yes'
      ports_no: 'yes'
      processes: 'yes'

**wazuh_manager_monitor_aws**

  Configures the :ref:`wodle<wodle_s3>` item named ``aws-s3`` from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_manager_monitor_aws:
      disabled: 'yes'
      interval: '10m'
      run_on_start: 'yes'
      skip_on_error: 'yes'
      s3:
        - name: null
          bucket_type: null
          path: null
          only_logs_after: null
          access_key: null
          secret_key: null

**wazuh_manager_sca**

  Configures the :ref:`sca<reference_sec_config_assessment>` section from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_manager_sca:
      enabled: 'yes'
      scan_on_start: 'yes'
      interval: '12h'
      skip_nfs: 'yes'
      day: ''
      wday: ''
      time: ''

**wazuh_manager_vulnerability_detector**

  Configures the :ref:`vulnerability-detector<vuln_detector>` section from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_manager_vulnerability_detector:
      enabled: 'no'
      interval: '5m'
      min_full_scan_interval: '6h'
      run_on_start: 'yes'
      providers:
        - enabled: 'no'
          os:
            - 'trusty'
            - 'xenial'
            - 'bionic'
          update_interval: '1h'
          name: '"canonical"'
        - enabled: 'no'
          os:
            - 'wheezy'
            - 'stretch'
            - 'jessie'
            - 'buster'
          update_interval: '1h'
          name: '"debian"'
        - enabled: 'no'
          update_from_year: '2010'
          update_interval: '1h'
          name: '"redhat"'
        - enabled: 'no'
          update_from_year: '2010'
          update_interval: '1h'
          name: '"nvd"'

**wazuh_manager_syscheck**

  Configures the :ref:`syscheck<reference_ossec_syscheck>` section from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_manager_syscheck:
      disable: 'no'
      frequency: 43200
      scan_on_start: 'yes'
      auto_ignore: 'no'
      ignore:
        - /etc/mtab
        - /etc/hosts.deny
        - /etc/mail/statistics
        - /etc/random-seed
        - /etc/random.seed
        - /etc/adjtime
        - /etc/httpd/logs
        - /etc/utmpx
        - /etc/wtmpx
        - /etc/cups/certs
        - /etc/dumpdates
        - /etc/svc/volatile
      ignore_linux_type:
        - '.log$|.swp$'
      no_diff:
        - /etc/ssl/private.key
      directories:
        - dirs: /etc,/usr/bin,/usr/sbin
          checks: ''
        - dirs: /bin,/sbin,/boot
          checks: ''
      auto_ignore_frequency:
        frequency: 'frequency="10"'
        timeframe: 'timeframe="3600"'
        value: 'no'
      skip_nfs: 'yes'
      skip_dev: 'yes'
      skip_proc: 'yes'
      skip_sys: 'yes'
      process_priority: 10
      max_eps: 100
      sync_enabled: 'yes'
      sync_interval: '5m'
      sync_max_interval: '1h'
      sync_max_eps: 10

**wazuh_manager_commands**

  Configures the :ref:`command<reference_ossec_commands>` section from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_manager_commands:
      - name: 'disable-account'
        executable: 'disable-account'
        timeout_allowed: 'yes'
      - name: 'restart-wazuh'
        executable: 'restart-wazuh'
      - name: 'firewall-drop'
        executable: 'firewall-drop'
        timeout_allowed: 'yes'
      - name: 'host-deny'
        executable: 'host-deny'
        timeout_allowed: 'yes'
      - name: 'route-null'
        executable: 'route-null'
        timeout_allowed: 'yes'
      - name: 'win_route-null'
        executable: 'route-null.exe'
        timeout_allowed: 'yes'
      - name: 'netsh'
        executable: 'netsh.exe'
        timeout_allowed: 'yes'
      - name: 'netsh-win-2016'
        executable: 'netsh-win-2016.cmd'
        timeout_allowed: 'yes'

**wazuh_manager_localfiles**

  Configures the :ref:`localfile<reference_ossec_localfile>` section from ``ossec.conf`` for each platform.

  *Default:*

  .. code-block:: yaml

    wazuh_manager_localfiles:
      common:
        - format: 'command'
          command: df -P
          frequency: '360'
        - format: 'full_command'
          command: netstat -tulpn | sed 's/\([[:alnum:]]\+\)\ \+[[:digit:]]\+\ \+[[:digit:]]\+\ \+\(.*\):\([[:digit:]]*\)\ \+\([0-9\.\:\*]\+\).\+\ \([[:digit:]]*\/[[:alnum:]\-]*\).*/\1 \2 == \3 == \4 \5/' | sort -k 4 -g | sed 's/ == \(.*\) ==/:\1/' | sed 1,2d
          alias: 'netstat listening ports'
          frequency: '360'
        - format: 'full_command'
          command: 'last -n 20'
          frequency: '360'
        - format: 'syslog'
          location: '/var/ossec/logs/active-responses.log'
      debian:
        - format: 'syslog'
          location: '/var/log/auth.log'
        - format: 'syslog'
          location: '/var/log/syslog'
        - format: 'syslog'
          location: '/var/log/dpkg.log'
        - format: 'syslog'
          location: '/var/log/kern.log'
      centos:
        - format: 'syslog'
          location: '/var/log/messages'
        - format: 'syslog'
          location: '/var/log/secure'
        - format: 'syslog'
          location: '/var/log/maillog'
        - format: 'audit'
          location: '/var/log/audit/audit.log'

**wazuh_manager_syslog_outputs**

  Configures the :ref:`syslog_output<reference_ossec_syslog_output>` section from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_manager_syslog_outputs:
      - server: null
        port: null
        format: null

**wazuh_manager_integrations**

  Configures the :ref:`integration<reference_ossec_integration>` section from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_manager_integrations:
      # slack
      - name: null
        hook_url: '<hook_url>'
        alert_level: 10
        alert_format: 'json'
        rule_id: null
      # pagerduty
      - name: null
        api_key: '<api_key>'
        alert_level: 12

**wazuh_manager_labels**

  Configures the :ref:`labels<reference_ossec_labels>` section from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_manager_labels:
      enable: false
      list:
        - key: Env
          value: Production

**wazuh_manager_ruleset**

  Configures the :ref:`ruleset<reference_ossec_rules>` section from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_manager_ruleset:
      rules_path: 'custom_ruleset/rules/'
      decoders_path: 'custom_ruleset/decoders/'
      cdb_lists:
        - 'audit-keys'
        - 'security-eventchannel'
        - 'amazon/aws-eventnames'

**wazuh_manager_rule_exclude**

  Configures the :ref:`rule_exclude<reference_ossec_rules>` section from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_manager_rule_exclude:
      - '0215-policy_rules.xml'


**wazuh_manager_authd**

  Configures the :ref:`auth<reference_ossec_auth>` section from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_manager_authd:
      enable: true
      port: 1515
      use_source_ip: 'no'
      force_insert: 'yes'
      force_time: 0
      purge: 'yes'
      use_password: 'no'
      limit_maxagents: 'yes'
      ciphers: 'HIGH:!ADH:!EXP:!MD5:!RC4:!3DES:!CAMELLIA:@STRENGTH'
      ssl_agent_ca: null
      ssl_verify_host: 'no'
      ssl_manager_cert: 'sslmanager.cert'
      ssl_manager_key: 'sslmanager.key'
      ssl_auto_negotiate: 'no'

**wazuh_manager_cluster**

  Configures the :ref:`cluster<reference_ossec_cluster>` section from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_manager_cluster:
      disable: 'yes'
      name: 'wazuh'
      node_name: 'manager_01'
      node_type: 'master'
      key: 'ugdtAnd7Pi9myP7CVts4qZaZQEQcRYZa'
      port: '1516'
      bind_addr: '0.0.0.0'
      nodes:
        - 'manager'
      hidden: 'no'

**wazuh_manager_api**

  Configures the :ref:`Wazuh API<api_configuration>` file called ``api.yaml``.

  *Default:*

  .. code-block:: yaml

    wazuh_manager_api:
      bind_addr: 0.0.0.0
      port: 55000
      https: yes
      https_key: "server.key"
      https_cert: "server.crt"
      https_use_ca: False
      https_ca: "ca.crt"
      logging_level: "info"
      cors: no
      cors_source_route: "*"
      cors_expose_headers: "*"
      cors_allow_headers: "*"
      cors_allow_credentials: no
      cache: yes
      cache_time: 0.750
      access_max_login_attempts: 5
      access_block_time: 300
      access_max_request_per_minute: 300
      drop_privileges: yes
      experimental_features: no

**wazuh_api_user:**

  Wazuh API credentials.

  *Example:*

  .. code-block:: yaml

    wazuh_api_user:
    - foo:$apr1$/axqZYWQ$Xo/nz/IG3PdwV82EnfYKh/
    - bar:$apr1$hXE97ag.$8m0koHByattiGKUKPUgcZ1

.. warning:: We recommend the use of `Ansible Vault <https://docs.ansible.com/ansible/latest/user_guide/vault.html>`_ to protect Wazuh, agentless and authd credentials.


**wazuh_manager_config:**

  Stores the Wazuh Manager configuration. This variable is provided for backwards compatibility.
  Newer deployments should use the newly introduced variables described above.

  *Example:*

  .. code-block:: yaml

    wazuh_manager_config:
      json_output: 'yes'
      alerts_log: 'yes'
      logall: 'no'
      log_format: 'plain'
      cluster:
        disable: 'yes'
        name: 'wazuh'
        node_name: 'manager_01'
        node_type: 'master'
        key: 'ugdtAnd7Pi9myP7CVts4qZaZQEQcRYZa'
        interval: '2m'
        port: '1516'
        bind_addr: '0.0.0.0'
        nodes:
          - '172.17.0.2'
          - '172.17.0.3'
          - '172.17.0.4'
        hidden: 'no'
      connection:
        - type: 'secure'
          port: '1514'
          protocol: 'tcp'
      authd:
        enable: true
        port: 1515
        use_source_ip: 'no'
        force_insert: 'yes'
        force_time: 0
        purge: 'no'
        use_password: 'no'
        ssl_agent_ca: null
        ssl_verify_host: 'no'
        ssl_manager_cert: 'etc/sslmanager.cert'
        ssl_manager_key: 'etc/sslmanager.key'
        ssl_auto_negotiate: 'no'
      email_notification: 'no'
      mail_to:
        - 'admin@example.net'
      mail_smtp_server: localhost
      mail_from: wazuh-manager@example.com
      extra_emails:
        - enable: false
          mail_to: 'admin@example.net'
          format: full
          level: 7
          event_location: null
          group: null
          do_not_delay: false
          do_not_group: false
          rule_id: null
      reports:
        - enable: false
          category: 'syscheck'
          title: 'Daily report: File changes'
          email_to: 'admin@example.net'
          location: null
          group: null
          rule: null
          level: null
          srcip: null
          user: null
          showlogs: null
      syscheck:
        frequency: 43200
        scan_on_start: 'yes'
        auto_ignore: 'no'
        alert_new_files: 'yes'
        ignore:
          - /etc/mtab
          - /etc/mnttab
          - /etc/hosts.deny
          - /etc/mail/statistics
          - /etc/random-seed
          - /etc/random.seed
          - /etc/adjtime
          - /etc/httpd/logs
          - /etc/utmpx
          - /etc/wtmpx
          - /etc/cups/certs
          - /etc/dumpdates
          - /etc/svc/volatile
        no_diff:
          - /etc/ssl/private.key
        directories:
          - dirs: /etc,/usr/bin,/usr/sbin
            checks: 'check_all="yes"'
          - dirs: /bin,/sbin
            checks: 'check_all="yes"'
      rootcheck:
        frequency: 43200
      openscap:
        disable: 'no'
        timeout: 1800
        interval: '1d'
        scan_on_start: 'yes'
      cis_cat:
        disable: 'yes'
        install_java: 'yes'
        timeout: 1800
        interval: '1d'
        scan_on_start: 'yes'
        java_path: '/usr/lib/jvm/java-1.8.0-openjdk-amd64/jre/bin'
        ciscat_path: '/var/ossec/wodles/ciscat'
        content:
          - type: 'xccdf'
            path: 'benchmarks/CIS_Ubuntu_Linux_16.04_LTS_Benchmark_v1.0.0-xccdf.xml'
            profile: 'xccdf_org.cisecurity.benchmarks_profile_Level_1_-_Server'
      log_level: 1
      email_level: 12
      localfiles:
        - format: 'syslog'
          location: '/var/log/messages'
        - format: 'syslog'
          location: '/var/log/secure'
        - format: 'command'
          command: 'df -P'
          frequency: '360'
        - format: 'full_command'
          command: 'netstat -tln | grep -v 127.0.0.1 | sort'
          frequency: '360'
        - format: 'full_command'
          command: 'last -n 20'
          frequency: '360'
      globals:
        - '127.0.0.1'
        - '192.168.2.1'
      commands:
        - name: 'disable-account'
          executable: 'disable-account'
          timeout_allowed: 'yes'
        - name: 'restart-wazuh'
          executable: 'restart-wazuh'
          timeout_allowed: 'no'
        - name: 'win_restart-wazuh'
          executable: 'restart-wazuh.exe'
          timeout_allowed: 'no'
        - name: 'firewall-drop'
          executable: 'firewall-drop'
          timeout_allowed: 'yes'
        - name: 'host-deny'
          executable: 'host-deny'
          timeout_allowed: 'yes'
        - name: 'route-null'
          executable: 'route-null'
          timeout_allowed: 'yes'
        - name: 'win_route-null'
          executable: 'route-null.exe'
          timeout_allowed: 'yes'
      active_responses:
        - command: 'restart-wazuh'
          location: 'local'
          rules_id: '100002'
        - command: 'win_restart-wazuh'
          location: 'local'
          rules_id: '100003'
        - command: 'host-deny'
          location: 'local'
          level: 6
          timeout: 600
      syslog_outputs:
        - server: null
          port: null
          format: null

**wazuh_agent_configs:**

  This store the different settings and profiles for centralized agent configuration via the Wazuh manager.

  *Example:*

  .. code-block:: yaml

      - type: os
        type_value: Linux
        syscheck:
          frequency: 43200
          scan_on_start: 'yes'
          auto_ignore: 'no'
          alert_new_files: 'yes'
          ignore:
          - /etc/mtab
          - /etc/mnttab
          - /etc/hosts.deny
          - /etc/mail/statistics
          - /etc/svc/volatile
          no_diff:
            - /etc/ssl/private.key
          directories:
            - dirs: /etc,/usr/bin,/usr/sbin
              checks: 'check_all="yes"'
            - dirs: /bin,/sbin
              checks: 'check_all="yes"'
        rootcheck:
          frequency: 43200
          cis_distribution_filename: null
        localfiles:
          - format: 'syslog'
            location: '/var/log/messages'
          - format: 'syslog'
            location: '/var/log/secure'
          - format: 'syslog'
            location: '/var/log/maillog'
          - format: 'apache'
            location: '/var/log/httpd/error_log'
          - format: 'apache'
            location: '/var/log/httpd/access_log'
          - format: 'apache'
            location: '/var/ossec/logs/active-responses.log'
      - type: os
        type_value: Windows
        syscheck:
          frequency: 43200
          scan_on_start: 'yes'
          auto_ignore: 'no'
          alert_new_files: 'yes'
          windows_registry:
            - key: 'HKEY_LOCAL_MACHINE\Software\Classes\batfile'
              arch: 'both'
            - key: 'HKEY_LOCAL_MACHINE\Software\Classes\Folder'
        localfiles:
          - format: 'Security'
            location: 'eventchannel'
          - format: 'System'
            location: 'eventlog'

**cdb_lists:**

  Configure CDB lists used by the Wazuh Manager (located at ``ansible-wazuh-manager/vars/cdb_lists.yml``).

  *Example:*

  .. code-block:: yaml

    cdb_lists:
    - name: 'audit-keys'
      content: |
        audit-wazuh-w:write
        audit-wazuh-r:read
        audit-wazuh-a:attribute
        audit-wazuh-x:execute
        audit-wazuh-c:command

.. warning:: We recommend the use of `Ansible Vault <https://docs.ansible.com/ansible/latest/user_guide/vault.html>`_ to protect Wazuh, agentless and authd credentials.

**agentless_creeds:**

  Credentials and host(s) to be used by agentless feature.

  *Example:*

  .. code-block:: yaml

    agentless_creeds:
      - type: ssh_integrity_check_linux
        frequency: 3600
        host: root@example.net
        state: periodic
        arguments: '/bin /etc/ /sbin'
        passwd: qwerty

.. warning:: We recommend the use of `Ansible Vault <https://docs.ansible.com/ansible/latest/user_guide/vault.html>`_ to protect Wazuh, agentless and authd credentials.


**authd_pass:**

  Wazuh authd service password.

  *Example:*

  .. code-block:: yaml

    authd_pass: foobar

.. _wazuh_ansible_reference_agent:

Wazuh Agent
===========

**wazuh_managers:**

  Set Wazuh Manager servers IP address, protocol, and port to be used by the agent.
  Regarding which Manager is used for registration, we can optionally indicate which one to use for registration by adding `register` set to `true`.
  If the `register` option is missing, first Manager on the list will be used for registration.

  *Example:*

  .. code-block:: yaml

      wazuh_managers:
      - address: 172.16.24.56
        protocol: udp
      - address: 192.168.10.15
        port: 1514
        protocol: tcp
        register: yes

**wazuh_agent_nolog_sensible:**

  This variable indicates if we should add `nolog option <https://docs.ansible.com/ansible/latest/reference_appendices/logging.html>`_ to tasks which output sensible information (like tokens).

  *Default true*


**wazuh_agent_api_validate:**

  After registering the agent through the REST API, validate that registration is correct.

  *Default true*

  Multiple profiles can be included, separated by a comma and a space, for example:


**wazuh_agent_address:**

  Establish which IP address we want to associate with this agent. It can be an address or "any"
  This variable will supersede `wazuh_agent_nat`.

  *Default ansible_default_ipv4.address*


**wazuh_profile:**

  Configure what profiles this agent will have.

  *Default null*

  Multiple profiles can be included, separated by a comma and a space, for example:

  .. code-block:: yaml

      wazuh_profile: "centos7, centos7-web"

**wazuh_agent_authd:**

  Set the agent-authd facility. This will enable or not the automatic agent registration, you could set various options in accordance of the authd service configured in the Wazuh Manager. This Ansible role will use the address defined on ``registration_address`` as the authd registration server.

  .. code-block:: yaml

    wazuh_agent_authd:
      registration_address: 10.1.1.12
      enable: false
      port: 1515
      ssl_agent_ca: null
      ssl_agent_cert: null
      ssl_agent_key: null
      ssl_auto_negotiate: 'no'

**wazuh_notify_time**

  Set the <notify_time> option in the agent.

  *Default null*

**wazuh_time_reconnect**

  Set <time-reconnect> option in the agent.

  *Default null*

**wazuh_winagent_config**

  Set the Wazuh Agent installation regarding Windows hosts.

  .. code-block:: yaml

    install_dir: 'C:\wazuh-agent\'
    version: '2.1.1'
    revision: '2'
    repo: https://packages.wazuh.com/windows/
    md5: fd9a3ce30cd6f9f553a1bc71e74a6c9f

**wazuh_agent_enrollment**

  Configures the :ref:`enrollment<reference_ossec_client>` section from agent ``ossec.conf``.

  *Example:*

  .. code-block:: yaml

    wazuh_agent_enrollment:
      enabled: ''
      manager_address: ''
      port: 1515
      agent_name: 'testname'
      groups: ''
      agent_address: ''
      ssl_cipher: HIGH:!ADH:!EXP:!MD5:!RC4:!3DES:!CAMELLIA:@STRENGTH
      server_ca_path: ''
      agent_certificate_path: ''
      agent_key_path: ''
      authorization_pass_path: /var/ossec/etc/authd.pass
      auto_method: 'no'
      delay_after_enrollment: 20
      use_source_ip: 'no'

**wazuh_agent_client_buffer**

  Configures the :ref:`client_buffer<reference_client_buffer>` section from agent ``ossec.conf``.

  .. code-block:: yaml

    wazuh_agent_client_buffer:
      disable: 'no'
      queue_size: '5000'
      events_per_sec: '500'

**wazuh_agent_rootcheck**

  Configures the :ref:`rootcheck<reference_ossec_rootcheck>` section from agent ``ossec.conf``.

  .. code-block:: yaml

    wazuh_agent_rootcheck:
      frequency: 43200

**wazuh_agent_openscap**

  Configures the :ref:`wodle<wodle_openscap>` item named ``open-scap`` from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_agent_openscap:
      disable: 'yes'
      timeout: 1800
      interval: '1d'
      scan_on_start: 'yes'


**wazuh_agent_cis_cat**

  Configures the :ref:`wodle<wodle_ciscat>` item named ``cis-cat`` from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_agent_cis_cat:
      disable: 'yes'
      install_java: 'no'
      timeout: 1800
      interval: '1d'
      scan_on_start: 'yes'
      java_path: 'wodles/java'
      java_path_win: '\\server\jre\bin\java.exe'
      ciscat_path: 'wodles/ciscat'
      ciscat_path_win: 'C:\cis-cat'


**wazuh_agent_osquery**

  Configures the :ref:`wodle<wodle-osquery>` item named ``osquery`` from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_agent_osquery:
      disable: 'yes'
      run_daemon: 'yes'
      bin_path_win: 'C:\Program Files\osquery\osqueryd'
      log_path: '/var/log/osquery/osqueryd.results.log'
      log_path_win: 'C:\Program Files\osquery\log\osqueryd.results.log'
      config_path: '/etc/osquery/osquery.conf'
      config_path_win: 'C:\Program Files\osquery\osquery.conf'
      add_labels: 'yes'


**wazuh_agent_syscollector**

  Configures the :ref:`wodle<wodle-syscollector>` item named ``syscollector`` from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_agent_syscollector:
      disable: 'no'
      interval: '1h'
      scan_on_start: 'yes'
      hardware: 'yes'
      os: 'yes'
      network: 'yes'
      packages: 'yes'
      ports_no: 'yes'
      processes: 'yes'

**wazuh_agent_sca**

  Configures the :ref:`sca<reference_sec_config_assessment>` section from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_agent_sca:
      enabled: 'yes'
      scan_on_start: 'yes'
      interval: '12h'
      skip_nfs: 'yes'
      day: ''
      wday: ''
      time: ''

**wazuh_agent_syscheck**

  Configures the :ref:`syscheck<reference_ossec_syscheck>` section from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_agent_syscheck:
      frequency: 43200
      scan_on_start: 'yes'
      auto_ignore: 'no'
      win_audit_interval: 60
      skip_nfs: 'yes'
      skip_dev: 'yes'
      skip_proc: 'yes'
      skip_sys: 'yes'
      process_priority: 10
      max_eps: 100
      sync_enabled: 'yes'
      sync_interval: '5m'
      sync_max_interval: '1h'
      sync_max_eps: 10
      ignore:
        - /etc/mtab
        - /etc/hosts.deny
        - /etc/mail/statistics
        - /etc/random-seed
        - /etc/random.seed
        - /etc/adjtime
        - /etc/httpd/logs
        - /etc/utmpx
        - /etc/wtmpx
        - /etc/cups/certs
        - /etc/dumpdates
        - /etc/svc/volatile
      ignore_linux_type:
        - '.log$|.swp$'
      ignore_win:
        - '.log$|.htm$|.jpg$|.png$|.chm$|.pnf$|.evtx$'
      no_diff:
        - /etc/ssl/private.key
      directories:
        - dirs: /etc,/usr/bin,/usr/sbin
          checks: ''
        - dirs: /bin,/sbin,/boot
          checks: ''
      win_directories:
        - dirs: '%WINDIR%'
          checks: 'recursion_level="0" restrict="regedit.exe$|system.ini$|win.ini$"'
        - dirs: '%WINDIR%\SysNative'
          checks: >-
            recursion_level="0" restrict="at.exe$|attrib.exe$|cacls.exe$|cmd.exe$|eventcreate.exe$|ftp.exe$|lsass.exe$|
            net.exe$|net1.exe$|netsh.exe$|reg.exe$|regedt32.exe|regsvr32.exe|runas.exe|sc.exe|schtasks.exe|sethc.exe|subst.exe$"
        - dirs: '%WINDIR%\SysNative\drivers\etc%'
          checks: 'recursion_level="0"'
        - dirs: '%WINDIR%\SysNative\wbem'
          checks: 'recursion_level="0" restrict="WMIC.exe$"'
        - dirs: '%WINDIR%\SysNative\WindowsPowerShell\v1.0'
          checks: 'recursion_level="0" restrict="powershell.exe$"'
        - dirs: '%WINDIR%\SysNative'
          checks: 'recursion_level="0" restrict="winrm.vbs$"'
        - dirs: '%WINDIR%\System32'
          checks: >-
            recursion_level="0" restrict="at.exe$|attrib.exe$|cacls.exe$|cmd.exe$|eventcreate.exe$|ftp.exe$|lsass.exe$|net.exe$|net1.exe$|
            netsh.exe$|reg.exe$|regedit.exe$|regedt32.exe$|regsvr32.exe$|runas.exe$|sc.exe$|schtasks.exe$|sethc.exe$|subst.exe$"
        - dirs: '%WINDIR%\System32\drivers\etc'
          checks: 'recursion_level="0"'
        - dirs: '%WINDIR%\System32\wbem'
          checks: 'recursion_level="0" restrict="WMIC.exe$"'
        - dirs: '%WINDIR%\System32\WindowsPowerShell\v1.0'
          checks: 'recursion_level="0" restrict="powershell.exe$"'
        - dirs: '%WINDIR%\System32'
          checks: 'recursion_level="0" restrict="winrm.vbs$"'
        - dirs: '%PROGRAMDATA%\Microsoft\Windows\Start Menu\Programs\Startup'
          checks: 'realtime="yes"'
      windows_registry:
        - key: 'HKEY_LOCAL_MACHINE\Software\Classes\batfile'
        - key: 'HKEY_LOCAL_MACHINE\Software\Classes\cmdfile'
        - key: 'HKEY_LOCAL_MACHINE\Software\Classes\comfile'
        - key: 'HKEY_LOCAL_MACHINE\Software\Classes\exefile'
        - key: 'HKEY_LOCAL_MACHINE\Software\Classes\piffile'
        - key: 'HKEY_LOCAL_MACHINE\Software\Classes\AllFilesystemObjects'
        - key: 'HKEY_LOCAL_MACHINE\Software\Classes\Directory'
        - key: 'HKEY_LOCAL_MACHINE\Software\Classes\Folder'
        - key: 'HKEY_LOCAL_MACHINE\Software\Classes\Protocols'
          arch: "both"
        - key: 'HKEY_LOCAL_MACHINE\Software\Policies'
          arch: "both"
        - key: 'HKEY_LOCAL_MACHINE\Security'
        - key: 'HKEY_LOCAL_MACHINE\Software\Microsoft\Internet Explorer'
          arch: "both"
        - key: 'HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services'
        - key: 'HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Session Manager\KnownDLLs'
        - key: 'HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\SecurePipeServers\winreg'
        - key: 'HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\Run'
          arch: "both"
        - key: 'HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\RunOnce'
          arch: "both"
        - key: 'HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\RunOnceEx'
        - key: 'HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\URL'
          arch: "both"
        - key: 'HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\Policies'
          arch: "both"
        - key: 'HKEY_LOCAL_MACHINE\Software\Microsoft\Windows NT\CurrentVersion\Windows'
          arch: "both"
        - key: 'HKEY_LOCAL_MACHINE\Software\Microsoft\Windows NT\CurrentVersion\Winlogon'
          arch: "both"
        - key: 'HKEY_LOCAL_MACHINE\Software\Microsoft\Active Setup\Installed Components'
          arch: "both"
      windows_registry_ignore:
        - key: 'HKEY_LOCAL_MACHINE\Security\Policy\Secrets'
        - key: 'HKEY_LOCAL_MACHINE\Security\SAM\Domains\Account\Users'
        - key: '\Enum$'
          type: "sregex"

**wazuh_agent_localfiles**

  Configures the :ref:`localfile<reference_ossec_localfile>` section from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_agent_localfiles:
      debian:
        - format: 'syslog'
          location: '/var/log/auth.log'
        - format: 'syslog'
          location: '/var/log/syslog'
        - format: 'syslog'
          location: '/var/log/dpkg.log'
        - format: 'syslog'
          location: '/var/log/kern.log'
      centos:
        - format: 'syslog'
          location: '/var/log/messages'
        - format: 'syslog'
          location: '/var/log/secure'
        - format: 'syslog'
          location: '/var/log/maillog'
        - format: 'audit'
          location: '/var/log/audit/audit.log'
      linux:
        - format: 'syslog'
          location: '/var/ossec/logs/active-responses.log'
        - format: 'full_command'
          command: 'last -n 20'
          frequency: '360'
        - format: 'command'
          command: df -P
          frequency: '360'
        - format: 'full_command'
          command: netstat -tulpn | sed 's/\([[:alnum:]]\+\)\ \+[[:digit:]]\+\ \+[[:digit:]]\+\ \+\(.*\):\([[:digit:]]*\)\ \+\([0-9\.\:\*]\+\).\+\ \([[:digit:]]*\/[[:alnum:]\-]*\).*/\1 \2 == \3 == \4 \5/' | sort -k 4 -g | sed 's/ == \(.*\) ==/:\1/' | sed 1,2d
          alias: 'netstat listening ports'
          frequency: '360'
      windows:
        - format: 'eventlog'
          location: 'Application'
        - format: 'eventchannel'
          location: 'Security'
          query: 'Event/System[EventID != 5145 and EventID != 5156 and EventID != 5447 and EventID != 4656 and EventID != 4658 and EventID != 4663 and EventID != 4660 and EventID != 4670 and EventID != 4690 and EventID != 4703 and EventID != 4907]'
        - format: 'eventlog'
          location: 'System'
        - format: 'syslog'
          location: 'active-response\active-responses.log'

**wazuh_agent_labels**

  Configures the :ref:`labels<reference_ossec_labels>` section from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_agent_labels:
      enable: false
      list:
        - key: Env
          value: Production

**wazuh_agent_active_response**

  Configures the :ref:`active-response<reference_ossec_active_response>` section from ``ossec.conf``.

  *Default:*

  .. code-block:: yaml

    wazuh_agent_active_response:
      ar_disabled: 'no'
      ca_store: '/var/ossec/etc/wpk_root.pem'
      ca_store_win: 'wpk_root.pem'
      ca_verification: 'yes'

**wazuh_agent_log_format**

  Configures the :ref:`log_format<reference_ossec_logging>` section from ``ossec.conf``.

  *Default: plain*

**wazuh_agent_config:**

  Wazuh Agent related configuration. This variable is provided for backwards compatibility.
  Newer deployments should use the newly introduced variables described above.

  *Example:*

  .. code-block:: yaml

    wazuh_agent_config:
      log_format: 'plain'
      syscheck:
        frequency: 43200
        scan_on_start: 'yes'
        auto_ignore: 'no'
        alert_new_files: 'yes'
        ignore:
          - /etc/mtab
          - /etc/mnttab
          - /etc/hosts.deny
          - /etc/mail/statistics
          - /etc/random-seed
          - /etc/random.seed
          - /etc/adjtime
          - /etc/httpd/logs
          - /etc/utmpx
          - /etc/wtmpx
          - /etc/cups/certs
          - /etc/dumpdates
          - /etc/svc/volatile
        no_diff:
          - /etc/ssl/private.key
        directories:
          - dirs: /etc,/usr/bin,/usr/sbin
            checks: 'check_all="yes"'
          - dirs: /bin,/sbin
            checks: 'check_all="yes"'
        windows_registry:
          - key: 'HKEY_LOCAL_MACHINE\Software\Classes\batfile'
            arch: 'both'
          - key: 'HKEY_LOCAL_MACHINE\Software\Classes\Folder'
      rootcheck:
        frequency: 43200
      openscap:
        disable: 'yes'
        timeout: 1800
        interval: '1d'
        scan_on_start: 'yes'
      cis_cat:
        disable: 'yes'
        install_java: 'yes'
        timeout: 1800
        interval: '1d'
        scan_on_start: 'yes'
        java_path: '/usr/lib/jvm/java-1.8.0-openjdk-amd64/jre/bin'
        ciscat_path: '/var/ossec/wodles/ciscat'
        content:
          - type: 'xccdf'
            path: 'benchmarks/CIS_Ubuntu_Linux_16.04_LTS_Benchmark_v1.0.0-xccdf.xml'
            profile: 'xccdf_org.cisecurity.benchmarks_profile_Level_1_-_Server'
      localfiles:
        - format: 'syslog'
          location: '/var/log/messages'
        - format: 'syslog'
          location: '/var/log/secure'
        - format: 'command'
          command: 'df -P'
          frequency: '360'
        - format: 'full_command'
          command: 'netstat -tln | grep -v 127.0.0.1 | sort'
          frequency: '360'
        - format: 'full_command'
          command: 'last -n 20'
          frequency: '360'

  .. warning:: We recommend the use of `Ansible Vault <https://docs.ansible.com/ansible/latest/user_guide/vault.html>`_ to protect authd credentials.

**authd_pass:**

  Wazuh authd credentials for agent registration.

  *Example:*

  .. code-block:: yaml

    authd_pass: foobar