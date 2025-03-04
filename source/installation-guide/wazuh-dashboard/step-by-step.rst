.. Copyright (C) 2022 Wazuh, Inc.

.. meta:: :description: Learn how to install Wazuh dashboard, a flexible and intuitive web interface for mining and visualizing the events and archives. 

.. _wazuh_dashboard_step_by_step:

Installing the Wazuh dashboard step by step
===========================================

Install and configure the Wazuh dashboard following step-by-step instructions. The Wazuh dashboard is a web interface for mining and visualizing the Wazuh server alerts and archived events.

.. note:: Root user privileges are required to run the commands described below.

Wazuh dashboard installation
----------------------------

Installing package dependencies
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. include:: /_templates/installations/dashboard/install-dependencies.rst

Adding the Wazuh repository
^^^^^^^^^^^^^^^^^^^^^^^^^^^

  .. note::
    If you are installing the Wazuh dashboard on the same host as the Wazuh indexer or the Wazuh server, you may skip these steps as you may have added the Wazuh repository already.

  .. tabs::
  
    .. group-tab:: Yum
  
  
      .. include:: /_templates/installations/common/yum/add-repository.rst
  
  
  
    .. group-tab:: APT
  
  
      .. include:: /_templates/installations/common/deb/add-repository.rst
  
  
  

Installing the Wazuh dashboard
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

  #. Install the Wazuh dashboard package.

      .. tabs::

          .. group-tab:: Yum


              .. include:: /_templates/installations/dashboard/yum/install_dashboard.rst



          .. group-tab:: APT


              .. include:: /_templates/installations/dashboard/apt/install_dashboard.rst



Configuring the Wazuh dashboard
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

  #. Edit the ``/etc/wazuh-dashboard/opensearch_dashboards.yml`` file and replace the following values:

     #. ``server.host``: This setting specifies the host of the back end server. To allow remote users to connect, set the value to the IP address or DNS name of the Kibana server.  The value ``0.0.0.0`` will accept all the available IP addresses of the host.

     #. ``opensearch.hosts``: The URLs of the Wazuh indexer instances to use for all your queries. Wazuh dashboard can be configured to connect to multiple Wazuh indexer nodes in the same cluster. The addresses of the nodes can be separated by commas. For example,  ``["https://10.0.0.2:9200", "https://10.0.0.3:9200","https://10.0.0.4:9200"]``

        .. code-block:: yaml
          :emphasize-lines: 1,3

             server.host: 0.0.0.0
             server.port: 443
             opensearch.hosts: https://localhost:9200
             opensearch.ssl.verificationMode: certificate




Deploying certificates
^^^^^^^^^^^^^^^^^^^^^^

  .. note::
    Make sure that a copy of ``wazuh-certificates.tar``, created in the previous stage of the installation process, is placed in your working directory.

  .. include:: /_templates/installations/dashboard/deploy_certificates.rst


Starting the Wazuh dashboard service
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

  #. Enable and start the Wazuh dashboard service.

      .. include:: /_templates/installations/dashboard/enable_dashboard.rst

      
      **Only for distributed deployments**  
      
          Edit the file ``/usr/share/wazuh-dashboard/data/wazuh/config/wazuh.yml`` and replace the ``url`` value with the IP address or hostname of the Wazuh server master node.
          
            .. code-block:: yaml
            
              hosts:
                - default:
                  url: https://localhost
                  port: 55000
                  username: wazuh-wui
                  password: wazuh-wui
                  run_as: false


  #. Access the Wazuh web interface with your credentials.

      - URL: *https://<dashboard_ip>*
      - **Username**: *admin*
      - **Password**: *<admin_password>*

    When you access the Wazuh dashboard for the first time, the browser shows a warning message stating that the certificate was not issued by a trusted authority. An exception can be added in the advanced options of the web browser or, for increased security, the ``root-ca.pem`` file previously generated can be imported to the certificate manager of the browser. Alternatively, a certificate from a trusted authority can be configured. 


Next steps
----------

All the Wazuh central components are successfully installed.

.. thumbnail:: ../../images/installation/Wazuh-Installation-workflow-complete.png
    :alt: Wazuh installation workflow
    :align: center
    :width: 100%


The Wazuh environment is now ready and you can proceed with installing the Wazuh agent on the endpoints to be monitored. To perform this action, see the :ref:`Wazuh agent <installation_agents>` section.

If you want to uninstall the Wazuh dashboard, see :ref:`uninstall_dashboard`.
