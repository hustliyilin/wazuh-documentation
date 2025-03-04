.. Copyright (C) 2022 Wazuh, Inc.

.. meta::
  :description: Find the packages required for Wazuh installation on this page. Available for AIX, Linux, HP-UX, macOS, Solaris, and Windows.

.. _packages:

Packages list
=============

This download page contains packages required for the Wazuh installation:


- `Wazuh manager and Wazuh agent`_

   - `Linux`_
   - `Windows`_
   - `macOS`_
   - `Solaris`_
   - `AIX`_
   - `HP-UX`_

- `Wazuh indexer`_
- `Wazuh dashboard`_
- `Wazuh Kibana plugin`_
- `Wazuh Splunk app`_
- `Filebeat`_
- `Virtual machine`_
- `Amazon Machine Image`_
- `MSU`_

.. _Wazuh_manager_agent_packages_list:

Wazuh manager and Wazuh agent
-----------------------------

Linux
^^^^^


+-----------------------+-------------------+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Distribution          | Version           | Architecture | Package                                                                                                                                                                                                                                      |
+=======================+===================+==============+==============================================================================================================================================================================================================================================+
|                       |                   |    i386      | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386|.i386.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386|.i386.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386|.i386.rpm.sha512>`__)                                    |
+ Amazon Linux          +  1 and 2          +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86|.x86_64.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86|.x86_64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86|.x86_64.rpm.sha512>`__)                              |
+                       +                   +    x86_64    +----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_X86|.x86_64.rpm <|RPM_MANAGER|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_X86|.x86_64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_X86|.x86_64.rpm.sha512>`__)                        |
+                       +                   +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_AARCH64|.aarch64.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_AARCH64|.aarch64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_AARCH64|.aarch64.rpm.sha512>`__)                           |
+                       +                   +    aarch64   +----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_AARCH64|.aarch64.rpm <|RPM_MANAGER|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_AARCH64|.aarch64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_AARCH64|.aarch64.rpm.sha512>`__)                     |
+                       +                   +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |    armhf     | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_ARMHF|.armv7hl.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_ARMHF|.armv7hl.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_ARMHF|.armv7hl.rpm.sha512>`__)                           |
+-----------------------+-------------------+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |  7 or later       |    powerpc   | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_PPC|.ppc64le.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_PPC|.ppc64le.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_PPC|.ppc64le.rpm.sha512>`__)                           |
+ CentOS                +-------------------+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |    i386      | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386|.i386.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386|.i386.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386|.i386.rpm.sha512>`__)                                    |
+                       +  6 or later       +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86|.x86_64.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86|.x86_64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86|.x86_64.rpm.sha512>`__)                              |
+                       +                   +    x86_64    +----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_X86|.x86_64.rpm <|RPM_MANAGER|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_X86|.x86_64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_X86|.x86_64.rpm.sha512>`__)                        |
+                       +                   +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_AARCH64|.aarch64.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_AARCH64|.aarch64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_AARCH64|.aarch64.rpm.sha512>`__)                           |
+                       +                   +    aarch64   +----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_AARCH64|.aarch64.rpm <|RPM_MANAGER|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_AARCH64|.aarch64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_AARCH64|.aarch64.rpm.sha512>`__)                     |
+                       +                   +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |    armhf     | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_ARMHF|.armv7hl.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_ARMHF|.armv7hl.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_ARMHF|.armv7hl.rpm.sha512>`__)                           |
+                       +-------------------+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |    i386      | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386_EL5|.el5.i386.rpm <https://packages.wazuh.com/|CURRENT_MAJOR|/yum5/i386/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386_EL5|.el5.i386.rpm>`__ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386_EL5|.el5.i386.rpm.sha512>`__)                 |
+                       +  5                +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |    x86_64    | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86_EL5|.el5.x86_64.rpm <https://packages.wazuh.com/|CURRENT_MAJOR|/yum5/x86_64/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86_EL5|.el5.x86_64.rpm>`__ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86_EL5|.el5.x86_64.rpm.sha512>`__)         |
+-----------------------+-------------------+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |  9 or later       |    powerpc   | `wazuh-agent_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_PPC|_ppc64el.deb <|DEB_AGENT|_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_PPC|_ppc64el.deb>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_PPC|_ppc64el.deb.sha512>`__)   |
+ Debian                +-------------------+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |    i386      | `wazuh-agent_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_I386|_i386.deb <|DEB_AGENT|_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_I386|_i386.deb>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_I386|_i386.deb.sha512>`__)            |
+                       +  7 or later       +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-agent_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_X86|_amd64.deb <|DEB_AGENT|_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_X86|_amd64.deb>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_X86|_amd64.deb.sha512>`__)         |
+                       +                   +    x86_64    +----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-manager_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_MANAGER_X86|_amd64.deb <|DEB_MANAGER|_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_MANAGER_X86|_amd64.deb>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-manager_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_MANAGER_X86|_amd64.deb.sha512>`__) |
+                       +                   +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-agent_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_AARCH64|_arm64.deb <|DEB_AGENT|_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_AARCH64|_arm64.deb>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_AARCH64|_arm64.deb.sha512>`__)         |
+                       +                   +    aarch64   +----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-manager_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_MANAGER_AARCH64|_arm64.deb <|DEB_MANAGER|_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_MANAGER_AARCH64|_arm64.deb>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-manager_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_MANAGER_AARCH64|_arm64.deb.sha512>`__) |
+                       +                   +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |    armhf     | `wazuh-agent_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_ARMHF|_armhf.deb <|DEB_AGENT|_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_ARMHF|_armhf.deb>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_ARMHF|_armhf.deb.sha512>`__)         |
+-----------------------+-------------------+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |    i386      | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386|.i386.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386|.i386.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386|.i386.rpm.sha512>`__)                                    |
+ Fedora                +  22 or later      +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86|.x86_64.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86|.x86_64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86|.x86_64.rpm.sha512>`__)                              |
+                       +                   +    x86_64    +----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_X86|.x86_64.rpm <|RPM_MANAGER|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_X86|.x86_64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_X86|.x86_64.rpm.sha512>`__)                        |
+                       +                   +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_AARCH64|.aarch64.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_AARCH64|.aarch64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_AARCH64|.aarch64.rpm.sha512>`__)                           |
+                       +                   +    aarch64   +----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_AARCH64|.aarch64.rpm <|RPM_MANAGER|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_AARCH64|.aarch64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_AARCH64|.aarch64.rpm.sha512>`__)                     |
+                       +                   +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |    armhf     | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_ARMHF|.armv7hl.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_ARMHF|.armv7hl.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_ARMHF|.armv7hl.rpm.sha512>`__)                           |
+-----------------------+-------------------+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |    i386      | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386|.i386.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386|.i386.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386|.i386.rpm.sha512>`__)                                    |
+ OpenSUSE              +  42 or later      +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86|.x86_64.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86|.x86_64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86|.x86_64.rpm.sha512>`__)                              |
+                       +                   +    x86_64    +----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_X86|.x86_64.rpm <|RPM_MANAGER|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_X86|.x86_64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_X86|.x86_64.rpm.sha512>`__)                        |
+                       +                   +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_AARCH64|.aarch64.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_AARCH64|.aarch64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_AARCH64|.aarch64.rpm.sha512>`__)                           |
+                       +                   +    aarch64   +----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_AARCH64|.aarch64.rpm <|RPM_MANAGER|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_AARCH64|.aarch64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_AARCH64|.aarch64.rpm.sha512>`__)                     |
+                       +                   +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |    armhf     | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_ARMHF|.armv7hl.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_ARMHF|.armv7hl.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_ARMHF|.armv7hl.rpm.sha512>`__)                           |
+-----------------------+-------------------+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |    i386      | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386|.i386.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386|.i386.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386|.i386.rpm.sha512>`__)                                    |
+ Oracle Linux          +  6 or later       +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86|.x86_64.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86|.x86_64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86|.x86_64.rpm.sha512>`__)                              |
+                       +                   +    x86_64    +----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_X86|.x86_64.rpm <|RPM_MANAGER|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_X86|.x86_64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_X86|.x86_64.rpm.sha512>`__)                        |
+                       +                   +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_AARCH64|.aarch64.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_AARCH64|.aarch64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_AARCH64|.aarch64.rpm.sha512>`__)                           |
+                       +                   +    aarch64   +----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_AARCH64|.aarch64.rpm <|RPM_MANAGER|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_AARCH64|.aarch64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_AARCH64|.aarch64.rpm.sha512>`__)                     |
+                       +                   +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |    armhf     | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_ARMHF|.armv7hl.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_ARMHF|.armv7hl.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_ARMHF|.armv7hl.rpm.sha512>`__)                           |
+                       +-------------------+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |    i386      | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386_EL5|.el5.i386.rpm <https://packages.wazuh.com/|CURRENT_MAJOR|/yum5/i386/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386_EL5|.el5.i386.rpm>`__ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386_EL5|.el5.i386.rpm.sha512>`__)                 |
+                       +  5                +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |    x86_64    | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86_EL5|.el5.x86_64.rpm <https://packages.wazuh.com/|CURRENT_MAJOR|/yum5/x86_64/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86_EL5|.el5.x86_64.rpm>`__ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86_EL5|.el5.x86_64.rpm.sha512>`__)         |
+-----------------------+-------------------+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |    i386      | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386|.i386.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386|.i386.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386|.i386.rpm.sha512>`__)                                    |
+ Red Hat               +  6 or later       +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Enterprise Linux      |                   |              | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86|.x86_64.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86|.x86_64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86|.x86_64.rpm.sha512>`__)                              |
+                       +                   +    x86_64    +----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_X86|.x86_64.rpm <|RPM_MANAGER|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_X86|.x86_64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_X86|.x86_64.rpm.sha512>`__)                        |
+                       +                   +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_AARCH64|.aarch64.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_AARCH64|.aarch64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_AARCH64|.aarch64.rpm.sha512>`__)                           |
+                       +                   +    aarch64   +----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_AARCH64|.aarch64.rpm <|RPM_MANAGER|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_AARCH64|.aarch64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_AARCH64|.aarch64.rpm.sha512>`__)                     |
+                       +                   +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |    armhf     | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_ARMHF|.armv7hl.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_ARMHF|.armv7hl.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_ARMHF|.armv7hl.rpm.sha512>`__)                           |
+                       +-------------------+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |    i386      | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386_EL5|.el5.i386.rpm <https://packages.wazuh.com/|CURRENT_MAJOR|/yum5/i386/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386_EL5|.el5.i386.rpm>`__ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386_EL5|.el5.i386.rpm.sha512>`__)                 |
+                       +  5                +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |    x86_64    | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86_EL5|.el5.x86_64.rpm <https://packages.wazuh.com/|CURRENT_MAJOR|/yum5/x86_64/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86_EL5|.el5.x86_64.rpm>`__ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86_EL5|.el5.x86_64.rpm.sha512>`__)         |
+-----------------------+-------------------+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |    i386      | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386|.i386.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386|.i386.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386|.i386.rpm.sha512>`__)                                    |
+ SUSE                  +  12               +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86|.x86_64.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86|.x86_64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86|.x86_64.rpm.sha512>`__)                              |
+                       +                   +    x86_64    +----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_X86|.x86_64.rpm <|RPM_MANAGER|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_X86|.x86_64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_X86|.x86_64.rpm.sha512>`__)                        |
+                       +                   +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_AARCH64|.aarch64.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_AARCH64|.aarch64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_AARCH64|.aarch64.rpm.sha512>`__)                           |
+                       +                   +    aarch64   +----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_AARCH64|.aarch64.rpm <|RPM_MANAGER|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_AARCH64|.aarch64.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-manager-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_MANAGER_AARCH64|.aarch64.rpm.sha512>`__)                     |
+                       +                   +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |    armhf     | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_ARMHF|.armv7hl.rpm <|RPM_AGENT|-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_ARMHF|.armv7hl.rpm>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_ARMHF|.armv7hl.rpm.sha512>`__)                           |
+                       +-------------------+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |    i386      | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386_EL5|.el5.i386.rpm <https://packages.wazuh.com/|CURRENT_MAJOR|/yum5/i386/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386_EL5|.el5.i386.rpm>`__ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_I386_EL5|.el5.i386.rpm.sha512>`__)                 |
+                       +  11               +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |    x86_64    | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86_EL5|.el5.x86_64.rpm <https://packages.wazuh.com/|CURRENT_MAJOR|/yum5/x86_64/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86_EL5|.el5.x86_64.rpm>`__ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_YUM_AGENT_X86_EL5|.el5.x86_64.rpm.sha512>`__)         |
+-----------------------+-------------------+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |    i386      | `wazuh-agent_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_I386|_i386.deb <|DEB_AGENT|_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_I386|_i386.deb>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_I386|_i386.deb.sha512>`__)            |
+ Ubuntu                +  12 or later      +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-agent_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_X86|_amd64.deb <|DEB_AGENT|_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_X86|_amd64.deb>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_X86|_amd64.deb.sha512>`__)         |
+                       +                   +    x86_64    +----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-manager_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_MANAGER_X86|_amd64.deb <|DEB_MANAGER|_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_MANAGER_X86|_amd64.deb>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-manager_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_MANAGER_X86|_amd64.deb.sha512>`__) |
+                       +                   +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-agent_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_AARCH64|_arm64.deb <|DEB_AGENT|_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_AARCH64|_arm64.deb>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_AARCH64|_arm64.deb.sha512>`__)         |
+                       +                   +    aarch64   +----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-manager_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_MANAGER_AARCH64|_arm64.deb <|DEB_MANAGER|_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_MANAGER_AARCH64|_arm64.deb>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-manager_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_MANAGER_AARCH64|_arm64.deb.sha512>`__) |
+                       +                   +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |    armhf     | `wazuh-agent_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_ARMHF|_armhf.deb <|DEB_AGENT|_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_ARMHF|_armhf.deb>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_ARMHF|_armhf.deb.sha512>`__)         |
+-----------------------+-------------------+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-agent_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_X86|_amd64.deb <|DEB_AGENT|_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_X86|_amd64.deb>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_X86|_amd64.deb.sha512>`__)         |
+                       +                   +    x86_64    +----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-manager_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_MANAGER_X86|_amd64.deb <|DEB_MANAGER|_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_MANAGER_X86|_amd64.deb>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-manager_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_MANAGER_X86|_amd64.deb.sha512>`__) |
+ Raspbian OS           + Buster or greater +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-agent_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_AARCH64|_arm64.deb <|DEB_AGENT|_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_AARCH64|_arm64.deb>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_AARCH64|_arm64.deb.sha512>`__)         |
+                       +                   +    aarch64   +----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |              | `wazuh-manager_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_MANAGER_AARCH64|_arm64.deb <|DEB_MANAGER|_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_MANAGER_AARCH64|_arm64.deb>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-manager_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_MANAGER_AARCH64|_arm64.deb.sha512>`__) |
+                       +                   +--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                       |                   |    armhf     | `wazuh-agent_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_ARMHF|_armhf.deb <|DEB_AGENT|_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_ARMHF|_armhf.deb>`_ (`sha512 <|CHECKSUMS_URL||WAZUH_LATEST|/wazuh-agent_|WAZUH_LATEST|-|WAZUH_REVISION_DEB_AGENT_ARMHF|_armhf.deb.sha512>`__)         |
+-----------------------+-------------------+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Windows
^^^^^^^

+-----------------+--------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Version         | Architecture | Package                                                                                                                                                                                                                                     |
+=================+==============+=============================================================================================================================================================================================================================================+
|  XP or later    |   32/64bits  | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_WINDOWS|.msi <https://packages.wazuh.com/|CURRENT_MAJOR|/windows/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_WINDOWS|.msi>`_ (`sha512 <https://packages.wazuh.com/|CURRENT_MAJOR|/checksums/wazuh/|WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_WINDOWS|.msi.sha512>`__)                                              |
+-----------------+--------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

macOS
^^^^^
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Architecture | Package                                                                                                                                                                                                                                       |
+==============+===============================================================================================================================================================================================================================================+
|    64bits    | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_OSX|.pkg <https://packages.wazuh.com/|CURRENT_MAJOR|/macos/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_OSX|.pkg>`_ (`sha512 <https://packages.wazuh.com/|CURRENT_MAJOR|/checksums/wazuh/|WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_OSX|.pkg.sha512>`__)                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Solaris
^^^^^^^
+---------+--------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Version | Architecture | Package                                                                                                                                                                                                                                     |
+=========+==============+=============================================================================================================================================================================================================================================+
|         |     i386     | `wazuh-agent_v|WAZUH_LATEST|-sol10-i386.pkg <https://packages.wazuh.com/|CURRENT_MAJOR|/solaris/i386/10/wazuh-agent_v|WAZUH_LATEST|-sol10-i386.pkg>`_ (`sha512 <https://packages.wazuh.com/|CURRENT_MAJOR|/checksums/wazuh/|WAZUH_LATEST|/wazuh-agent_v|WAZUH_LATEST|-sol10-i386.pkg.sha512>`__)        |
+  10     +--------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|         |     SPARC    | `wazuh-agent_v|WAZUH_LATEST|-sol10-sparc.pkg <https://packages.wazuh.com/|CURRENT_MAJOR|/solaris/sparc/10/wazuh-agent_v|WAZUH_LATEST|-sol10-sparc.pkg>`_ (`sha512 <https://packages.wazuh.com/|CURRENT_MAJOR|/checksums/wazuh/|WAZUH_LATEST|/wazuh-agent_v|WAZUH_LATEST|-sol10-sparc.pkg.sha512>`__)    |
+---------+--------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|         |     i386     | `wazuh-agent_v|WAZUH_LATEST|-sol11-i386.p5p <https://packages.wazuh.com/|CURRENT_MAJOR|/solaris/i386/11/wazuh-agent_v|WAZUH_LATEST|-sol11-i386.p5p>`_ (`sha512 <https://packages.wazuh.com/|CURRENT_MAJOR|/checksums/wazuh/|WAZUH_LATEST|/wazuh-agent_v|WAZUH_LATEST|-sol11-i386.p5p.sha512>`__)        |
+  11     +--------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|         |     SPARC    | `wazuh-agent_v|WAZUH_LATEST|-sol11-sparc.p5p <https://packages.wazuh.com/|CURRENT_MAJOR|/solaris/sparc/11/wazuh-agent_v|WAZUH_LATEST|-sol11-sparc.p5p>`_ (`sha512 <https://packages.wazuh.com/|CURRENT_MAJOR|/checksums/wazuh/|WAZUH_LATEST|/wazuh-agent_v|WAZUH_LATEST|-sol11-sparc.p5p.sha512>`__)    |
+---------+--------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

AIX
^^^
+-----------------+--------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Version         | Architecture | Package                                                                                                                                                                                                                                     |
+=================+==============+=============================================================================================================================================================================================================================================+
| 6.1 or greater  |    PowerPC   | `wazuh-agent-|WAZUH_LATEST_AIX|-|WAZUH_REVISION_AIX|.aix.ppc.rpm <https://packages.wazuh.com/|CURRENT_MAJOR|/aix/wazuh-agent-|WAZUH_LATEST_AIX|-|WAZUH_REVISION_AIX|.aix.ppc.rpm>`_ (`sha512 <https://packages.wazuh.com/|CURRENT_MAJOR|/checksums/wazuh/|WAZUH_LATEST_AIX|/wazuh-agent-|WAZUH_LATEST_AIX|-|WAZUH_REVISION_AIX|.aix.ppc.rpm.sha512>`__)                          |
+-----------------+--------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

HP-UX
^^^^^
+-----------------+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Version         | Architecture | Package                                                                                                                                                                                                                                      |
+=================+==============+==============================================================================================================================================================================================================================================+
|  11.31          |   Itanium    | `wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_HPUX|-hpux-11v3-ia64.tar <https://packages.wazuh.com/|CURRENT_MAJOR|/hp-ux/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_HPUX|-hpux-11v3-ia64.tar>`_ (`sha512 <https://packages.wazuh.com/|CURRENT_MAJOR|/checksums/wazuh/|WAZUH_LATEST|/wazuh-agent-|WAZUH_LATEST|-|WAZUH_REVISION_HPUX|-hpux-11v3-ia64.tar.sha512>`__)    |
+-----------------+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


Wazuh indexer
-------------

.. |IndexerRPM| replace:: `wazuh-indexer-|WAZUH_INDEXER_CURRENT|-|WAZUH_INDEXER_CURRENT_REV|.|WAZUH_INDEXER_x64_RPM|.rpm <https://packages.wazuh.com/4.x/yum/wazuh-indexer-|WAZUH_INDEXER_CURRENT|-|WAZUH_INDEXER_CURRENT_REV|.|WAZUH_INDEXER_x64_RPM|.rpm>`__ (`sha512 <https://packages.wazuh.com/4.x/checksums/wazuh/|WAZUH_INDEXER_CURRENT|/wazuh-indexer-|WAZUH_INDEXER_CURRENT|-|WAZUH_INDEXER_CURRENT_REV|.|WAZUH_INDEXER_x64_RPM|.rpm.sha512>`__)

.. |IndexerDEB| replace:: `wazuh-indexer_|WAZUH_INDEXER_CURRENT|-|WAZUH_INDEXER_CURRENT_REV|_|WAZUH_INDEXER_x64_DEB|.deb <https://packages.wazuh.com/4.x/apt/pool/main/w/wazuh-indexer/wazuh-indexer_|WAZUH_INDEXER_CURRENT|-|WAZUH_INDEXER_CURRENT_REV|_|WAZUH_INDEXER_x64_DEB|.deb>`__ (`sha512 <https://packages.wazuh.com/4.x/checksums/wazuh/|WAZUH_INDEXER_CURRENT|/wazuh-indexer_|WAZUH_INDEXER_CURRENT|-|WAZUH_INDEXER_CURRENT_REV|_|WAZUH_INDEXER_x64_DEB|.deb.sha512>`__)


+--------------+------------------+
| Package type | Package          |
+==============+==================+
|     RPM      | |IndexerRPM|     |
+--------------+------------------+
|     DEB      | |IndexerDEB|     |
+--------------+------------------+


Wazuh dashboard
---------------

.. |DashboardRPM| replace:: `wazuh-dashboard-|WAZUH_DASHBOARD_CURRENT|-|WAZUH_DASHBOARD_CURRENT_REV|.|WAZUH_DASHBOARD_x64_RPM|.rpm <https://packages.wazuh.com/4.x/yum/wazuh-dashboard-|WAZUH_DASHBOARD_CURRENT|-|WAZUH_DASHBOARD_CURRENT_REV|.|WAZUH_DASHBOARD_x64_RPM|.rpm>`__ (`sha512 <https://packages.wazuh.com/4.x/checksums/wazuh/|WAZUH_DASHBOARD_CURRENT|/wazuh-dashboard-|WAZUH_DASHBOARD_CURRENT|-|WAZUH_DASHBOARD_CURRENT_REV|.|WAZUH_DASHBOARD_x64_RPM|.rpm.sha512>`__)

.. |DashboardDEB| replace:: `wazuh-dashboard_|WAZUH_DASHBOARD_CURRENT|-|WAZUH_DASHBOARD_CURRENT_REV|_|WAZUH_DASHBOARD_x64_DEB|.deb <https://packages.wazuh.com/4.x/apt/pool/main/w/wazuh-dashboard/wazuh-dashboard_|WAZUH_DASHBOARD_CURRENT|-|WAZUH_DASHBOARD_CURRENT_REV|_|WAZUH_DASHBOARD_x64_DEB|.deb>`__ (`sha512 <https://packages.wazuh.com/4.x/checksums/wazuh/|WAZUH_DASHBOARD_CURRENT|/wazuh-dashboard_|WAZUH_DASHBOARD_CURRENT|-|WAZUH_DASHBOARD_CURRENT_REV|_|WAZUH_DASHBOARD_x64_DEB|.deb.sha512>`__)

+--------------+------------------+
| Package type | Package          |
+==============+==================+
|     RPM      | |DashboardRPM|   |
+--------------+------------------+
|     DEB      | |DashboardDEB|   |
+--------------+------------------+

Wazuh Kibana plugin
-------------------

.. |WAZUH_KIBANA_ES_LATEST| replace:: `wazuh_kibana-|WAZUH_LATEST|_|ELASTICSEARCH_LATEST|.zip <https://packages.wazuh.com/|CURRENT_MAJOR|/ui/kibana/wazuh_kibana-|WAZUH_LATEST|_|ELASTICSEARCH_LATEST|-1.zip>`__ (`sha512 <https://packages.wazuh.com/|CURRENT_MAJOR|/checksums/wazuh/|WAZUH_LATEST|/wazuh_kibana-|WAZUH_LATEST|_|ELASTICSEARCH_LATEST|-1.zip.sha512>`__)

.. |WAZUH_KIBANA_7.16.3| replace:: `wazuh_kibana-|WAZUH_LATEST|_7.16.3.zip <https://packages.wazuh.com/|CURRENT_MAJOR|/ui/kibana/wazuh_kibana-|WAZUH_LATEST|_7.16.3-1.zip>`__ (`sha512 <https://packages.wazuh.com/|CURRENT_MAJOR|/checksums/wazuh/|WAZUH_LATEST|/wazuh_kibana-|WAZUH_LATEST|_7.16.3-1.zip.sha512>`__)

.. |WAZUH_KIBANA_7.17.0| replace:: `wazuh_kibana-|WAZUH_LATEST|_7.17.0.zip <https://packages.wazuh.com/|CURRENT_MAJOR|/ui/kibana/wazuh_kibana-|WAZUH_LATEST|_7.17.0-1.zip>`__ (`sha512 <https://packages.wazuh.com/|CURRENT_MAJOR|/checksums/wazuh/|WAZUH_LATEST|/wazuh_kibana-|WAZUH_LATEST|_7.17.0-1.zip.sha512>`__)

.. |var_ELASTICSEARCH_LATEST| replace:: |ELASTICSEARCH_LATEST|

.. |var_OPEN_DISTRO_LATEST| replace:: |OPEN_DISTRO_LATEST|

.. |var_WAZUH_LATEST| replace:: |WAZUH_LATEST|

+----------------------------+--------------------------+---------------------+--------------------------+
| Kibana Version             | Open Distro Version      | Wazuh version       | Package                  |
+============================+==========================+=====================+==========================+
| |var_ELASTICSEARCH_LATEST| | |var_OPEN_DISTRO_LATEST| | |var_WAZUH_LATEST|  | |WAZUH_KIBANA_ES_LATEST| |
+----------------------------+--------------------------+---------------------+--------------------------+
| 7.16.3                     |                          | |var_WAZUH_LATEST|  | |WAZUH_KIBANA_7.16.3|    |
+----------------------------+--------------------------+---------------------+--------------------------+
| 7.17.0                     |                          | |var_WAZUH_LATEST|  | |WAZUH_KIBANA_7.17.0|    |
+----------------------------+--------------------------+---------------------+--------------------------+


For a complete list of the available versions, see the `Wazuh Kibana plugin compatibility matrix <https://github.com/wazuh/wazuh-kibana-app/tree/v4.2.5-7.10.2#wazuh---kibana---open-distro-version-compatibility-matrix>`_.

Wazuh Splunk app
----------------

.. |SPLUNK_8.1.4_PKG| replace:: `wazuh_splunk-|WAZUH_SPLUNK_LATEST|_8.1.4.tar.gz <https://packages.wazuh.com/4.x/ui/splunk/wazuh_splunk-|WAZUH_SPLUNK_LATEST|_8.1.4-1.tar.gz>`__ (`sha512 <https://packages.wazuh.com/4.x/checksums/wazuh/|WAZUH_SPLUNK_LATEST|/wazuh_splunk-|WAZUH_SPLUNK_LATEST|_8.1.4-1.tar.gz.sha512>`__)

.. |SPLUNK_8.2.2_PKG| replace:: `wazuh_splunk-|WAZUH_SPLUNK_LATEST|_8.2.2.tar.gz <https://packages.wazuh.com/4.x/ui/splunk/wazuh_splunk-|WAZUH_SPLUNK_LATEST|_8.2.2-1.tar.gz>`__ (`sha512 <https://packages.wazuh.com/4.x/checksums/wazuh/|WAZUH_SPLUNK_LATEST|/wazuh_splunk-|WAZUH_SPLUNK_LATEST|_8.2.2-1.tar.gz.sha512>`__)

.. |SPLUNK_LATEST_PKG| replace:: `wazuh_splunk-|WAZUH_SPLUNK_LATEST|_|SPLUNK_LATEST|.tar.gz <https://packages.wazuh.com/4.x/ui/splunk/wazuh_splunk-|WAZUH_SPLUNK_LATEST|_|SPLUNK_LATEST|-1.tar.gz>`__ (`sha512 <https://packages.wazuh.com/|CURRENT_MAJOR|/checksums/wazuh/|WAZUH_SPLUNK_LATEST|/wazuh_splunk-|WAZUH_SPLUNK_LATEST|_|SPLUNK_LATEST|-1.tar.gz.sha512>`__)

.. |var_SPLUNK_LATEST| replace:: |SPLUNK_LATEST|

.. |var_WAZUH_SPLUNK_LATEST| replace:: |WAZUH_SPLUNK_LATEST|

+----------------------+----------------------------+---------------------+
| Splunk version       | Wazuh version              | Package             |
+======================+============================+=====================+
| 8.1.4                | |var_WAZUH_SPLUNK_LATEST|  | |SPLUNK_8.1.4_PKG|  |
+----------------------+----------------------------+---------------------+
| 8.2.2                | |var_WAZUH_SPLUNK_LATEST|  | |SPLUNK_8.2.2_PKG|  |
+----------------------+----------------------------+---------------------+
| |var_SPLUNK_LATEST|  | |var_WAZUH_SPLUNK_LATEST|  | |SPLUNK_LATEST_PKG| |
+----------------------+----------------------------+---------------------+


Filebeat
---------------

+--------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Package type | Package                                                                                                                                                                                                                                         |
+==============+=================================================================================================================================================================================================================================================+
|     RPM      | `filebeat-oss-|ELASTICSEARCH_LATEST|-x86_64.rpm <https://packages.wazuh.com/4.x/yum/filebeat-oss-|ELASTICSEARCH_LATEST|-x86_64.rpm>`_ (`sha512 <https://packages.wazuh.com/4.x/checksums/elasticsearch/|ELASTICSEARCH_LATEST|/filebeat-oss-|ELASTICSEARCH_LATEST|-x86_64.rpm.sha512>`__)                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|     DEB      | `filebeat-oss-|ELASTICSEARCH_LATEST|-amd64.deb <https://packages.wazuh.com/4.x/apt/pool/main/f/filebeat/filebeat-oss-|ELASTICSEARCH_LATEST|-amd64.deb>`_ (`sha512 <https://packages.wazuh.com/4.x/checksums/elasticsearch/|ELASTICSEARCH_LATEST|/filebeat-oss-|ELASTICSEARCH_LATEST|-amd64.deb.sha512>`__)      |
+--------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Virtual machine
---------------

+--------------+--------------+--------------+---------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Distribution | Architecture | VM Format    | Version | Package                                                                                                                                                                                            |
+==============+==============+==============+=========+====================================================================================================================================================================================================+
|   CentOS 7   |    64bits    |      OVA     |  |WAZUH_LATEST_OVA|  | `wazuh-|WAZUH_LATEST_OVA|_|OPEN_DISTRO_LATEST|.ova <https://packages.wazuh.com/|CURRENT_MAJOR|/vm/wazuh-|WAZUH_LATEST_OVA|_|OPEN_DISTRO_LATEST|.ova>`_ (`sha512 <https://packages.wazuh.com/|CURRENT_MAJOR|/checksums/wazuh/|WAZUH_LATEST_OVA|/wazuh-|WAZUH_LATEST_OVA|_|OPEN_DISTRO_LATEST|.ova.sha512>`__)             |
+--------------+--------------+--------------+---------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Amazon Machine Image
--------------------

.. |AMI_PRODUCT_PAGE| replace:: `Wazuh All-In-One Deployment <https://aws.amazon.com/marketplace/pp/prodview-eju4flv5eqmgq>`__

.. |var_WAZUH_LATEST_AMI| replace:: |WAZUH_LATEST_AMI|

+------------------+--------------+-------------+------------------------+---------------------+
| Distribution     | Architecture | VM Format   | Latest version         | Product page        |
+==================+==============+=============+========================+=====================+
| Amazon Linux 2   | 64-bit       | AWS AMI     | |var_WAZUH_LATEST_AMI| | |AMI_PRODUCT_PAGE|  |
+------------------+--------------+-------------+------------------------+---------------------+


MSU
---

+-------------------+--------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Version           | Architecture | Package                                                                                                                                                                                                                               |
+===================+==============+=======================================================================================================================================================================================================================================+
|  4.0.0 or later   |   32/64bits  | `msu-updates.json.gz <https://feed.wazuh.com/vulnerability-detector/windows/msu-updates.json.gz>`_ (`sha256 <https://feed.wazuh.com/vulnerability-detector/windows/msu-updates.meta>`__)                                              |
+-------------------+--------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
